# GL.iNet 라우터에서 OpenVPN 서버 설정

OpenVPN은 가상 사설망 기술을 사용하여 보안 사이트 간 또는 지점 간 연결을 설정하는 오픈 소스 VPN 프로토콜입니다.

GL.iNet 라우터에서 OpenVPN 서버를 설정하려면 이 동영상을 보거나 아래 단계를 참조하세요.

<iframe width="560" height="315" src="https://www.youtube.com/embed/GSbytyaqOY0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## 공용 IP 주소가 있는지 확인하세요.

[여기](../tutorials/how_to_check_if_isp_assigns_you_a_public_ip_address.md)를 클릭하여 인터넷 서비스 제공자가 공용 IP 주소를 할당하는지 확인하세요.

**그렇지 않은 경우 라우터를 OpenVPN 서버로 설정할 수 없습니다.**

대체 방법:

1. 기본 라우터가 있는 경우 기본 라우터에 로그인하여 ISP로부터 공용 IP를 받는지 확인하세요.
2. ISP에 공용 IP 주소를 요청하세요. 추가 비용이 발생할 수 있습니다.
3. 위 두 가지 방법이 작동하지 않는 경우(예: 네트워크가 CGNAT 뒤에 있는 경우) SD-WAN 솔루션 [AstroWarp](https://www.astrowarp.net/){target="_blank"}을 시도해 볼 수 있습니다.

## 포트 포워딩이 필요한지 확인

**네트워크 토폴로지**

??? "GL.iNet이 기본 라우터인 경우"

    * GL.iNet 라우터가 네트워크의 기본 라우터인 경우 포트 포워딩이 필요하지 않습니다. [다음 단계](#setup-openvpn-server)로 이동하세요.

??? "GL.iNet이 서브 라우터인 경우"

    * 기본 라우터가 이미 사용 중이고 GL.iNet 라우터가 보조 라우터로 구성된 경우 기본 라우터에서 [포트 포워딩](../tutorials/how_to_set_up_port_forwarding.md)을 구성해야 합니다.

    * 기본 라우터가 이미 사용 중이고 GL.iNet 라우터가 기본 라우터보다 여러 수준 아래에 있는 경우 각 중간 수준에서 [포트 포워딩](../tutorials/how_to_set_up_port_forwarding.md)을 구성하세요.

## OpenVPN 서버 설정

웹 관리 패널에 로그인하고 **VPN** -> **OpenVPN Server**로 이동합니다.

1. **Generate Configuration**을 클릭합니다(vpn 서버 초기 설정에만 해당).

    ![ovpn server generate configuration](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_server/ovpnserver_generate_config.png){class="glboxshadow"}

2. 구성을 적용합니다.

    기본 구성은 대부분의 경우에 작동합니다.

    구성을 수정할 필요가 없는 경우 하단의 **Export Client Configuration**를 클릭하고 3단계로 넘어갑니다.

    구성을 수정한 경우 클라이언트 구성을 내보내기 전에 **Apply**를 클릭하세요.

    ![openvpn server configuration](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_server/ovpnserver_configuration.png){class="glboxshadow"}

    * **Device Mode:** TAP-S2S 또는 Tun. 차이점을 확인하려면 [여기](../tutorials/how_to_enable_openvpn_tap_s2s_mode_on_glinet_routers.md/#tap-s2s-vs-tun-mode)를 클릭하세요.

    * **Protocol:** UDP 또는 TCP. 차이점을 확인하려면 [여기](../faq/openvpn_tcp_udp.md)를 클릭하세요.

    * **Authentication Mode:** 클라이언트가 서버에 연결할 때 사용되는 인증 방법을 결정합니다. 세 가지 옵션이 있습니다.

        - **Certificate Only**: 선택하면 라우터가 서버 및 클라이언트 인증서 키를 자동으로 생성하고 클라이언트 구성 파일에 포함합니다. 클라이언트에 구성을 업로드할 때 추가 자격 증명이 필요하지 않습니다.

        - **Username/Password Only**: 선택하면 라우터가 인증서 키 없이 클라이언트 구성을 생성합니다. 클라이언트 구성을 내보내기 전에 Users 탭에서 사용자 이름과 비밀번호를 먼저 추가해야 합니다. 클라이언트에 구성을 업로드할 때 인증을 위해 이 자격 증명을 입력해야 합니다.

        - **Username/Password and Certificate**: 선택하면 클라이언트 구성을 내보내기 전에 Users 탭에서 사용자 이름과 비밀번호를 먼저 추가해야 합니다. 둘째, 라우터가 서버 및 클라이언트 인증서 키를 자동으로 생성하고 구성 파일에 포함합니다. 클라이언트에 구성을 업로드할 때 먼저 인증서 키가 검증된 다음 사용자 이름/비밀번호 인증이 이루어져 2단계 보안이 제공됩니다.

        사용자 생성 예시는 다음과 같습니다.

        ![openvpn server add a user](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_server/ovpnserver_add_a_user.png){class="glboxshadow"}

    * **Advanced Configuration**: 필요한 경우 더 많은 서버 설정을 수정할 수 있습니다.

        ![openvpn server advancd configuration](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_server/ovpnserver_advanced_config.png){class="glboxshadow"}

3. 클라이언트 구성 내보내기.

    Configuration 탭 하단의 **Export Client Configuration**를 클릭하거나(수정된 구성을 적용함) 아래와 같은 팝업 창이 나타납니다.

    ![openvpn server configuration](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_server/ovpnserver_export_configuration.png){class="glboxshadow"}

    - 네트워크의 공용 IP이 자주 변경되는 경우 [DDNS](ddns.md)를 활성화하여 DDNS 도메인을 서버 주소로 사용할 수 있습니다.

    - 펌웨어 v4.8부터 공용 IP, DDNS 도메인, 현재 WAN IP 중에서 서버 주소를 지정할 수 있습니다. 변경되면 구성 파일의 서버 주소가 동시에 업데이트됩니다.

    그런 다음 **Download**를 클릭하여 구성을 내보냅니다.

4. OpenVPN 서버 시작.

    OpenVPN Server 페이지의 오른쪽 상단에 있는 **Start** 버튼을 클릭하여 서버를 시작합니다. 그런 다음 [VPN Dashboard 페이지](vpn_dashboard.md)로 이동하여 상태와 기타 설정을 확인하세요.

    ![start openvpn server](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_server/start_ovpnserver.png){class="glboxshadow"}

## OpenVPN 서버가 제대로 작동하는지 확인

### 서버 상태 확인

펌웨어 v4.8부터 **OpenVPN Server** 페이지에서 서버 연결 상태를 확인할 수 있습니다.

업로드/다운로드 트래픽 통계가 표시되면 OpenVPN 서버가 실행 중인 것입니다.

![openvpn server connected v4.8](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_server/ovpnserver_status.jpg){class="glboxshadow"}

펌웨어 v4.7 및 이전 버전의 경우 **VPN Dashboard** 페이지에서 서버 연결 상태를 확인하세요.

![openvpn server connected v4.7](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_server/openserverup.jpg){class="glboxshadow"}

### 클라이언트 IP 확인

서버에 대한 연결 성공을 확인합니다: 이전에 내보낸 OpenVPN 구성을 서버와 동일한 로컬 네트워크가 아닌 다른 네트워크의 장치로 가져옵니다. 그런 다음 웹 브라우저를 열어 IP 주소와 위치를 검색합니다. VPN 서버의 IP(인터넷 서비스 제공자의 IP가 아님) 및 위치와 일치하면 VPN 연결이 성공한 것입니다.

가장 간단한 방법은 공식 [OpenVPN App](https://openvpn.net/vpn-client/){target="_blank"}이 설치된 스마트폰을 사용하는 것입니다. 먼저 스마트폰의 Wi-Fi를 비활성화하고 셀룰러 데이터(4G/5G)를 통해서만 인터넷에 연결합니다. 그런 다음 OpenVPN 앱을 열고 구성 파일을 가져온 다음 연결을 시작합니다. 스마트폰이 인터넷에 액세스할 수 있는지 그리고 IP 주소가 OpenVPN 서버의 IP와 일치하는지 확인하세요.

OpenVPN 앱에 구성 파일을 가져올 때 아래와 같은 알림이 나타날 수 있습니다. 인증서가 이미 구성 파일에 포함되어 있으므로 **CONTINUE**를 클릭하여 계속 진행하세요.

![openvpn app select certificate](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_server/select_certificate.png){class="glboxshadow" width="360"}

연결에 실패하면 몇 가지 일반적인 이유가 있습니다.

* 인터넷 서비스 제공자가 공용 IP 주소를 할당하지 않습니다. [여기](#make-sure-you-have-a-public-ip-address)를 확인하세요.
* 포트 포워딩을 설정해야 할 수 있습니다. [여기](#confirm-if-port-forwarding-is-required)를 확인하세요.
* OpenVPN 서버에서 사용하는 포트가 인터넷 서비스 제공자에 의해 차단되었습니다. 다른 포트로 변경하거나 인터넷 서비스 제공자에 문의하여 추가 지원을 받으세요.
* 일부 국가/지역에서 VPN 연결을 차단할 수 있습니다.

## 클라이언트 간 액세스

**네트워크 토폴로지**

![ptptopology](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_server/ptptopology.jpg){class="glboxshadow"}

client to client 토글을 활성화하고 클라이언트에 새 구성을 내보내면 클라이언트가 서로 액세스할 수 있습니다.

![peertopeer](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_server/peertopeer.jpg){class="glboxshadow"}

## OpenVPN 앱 설치

[OpenVPN 공식 웹사이트](https://openvpn.net/vpn-client/){target="_blank"}에서 OpenVPN 앱을 다운로드하세요.

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}을 통해 연락하세요.
