# GL.iNet 라우터에 WireGuard 서버 설정

WireGuard®는 최신 암호화 기술을 활용하는 매우 간단하면서도 빠르고 현대적인 VPN입니다. IPsec보다 빠르고, 간단하고, 가볍고, 유용하면서도 대규모 두통을 피하는 것을 목표로 합니다. OpenVPN보다 상당히 뛰어난 성능을 제공합니다.

GL.iNet 라우터에 WireGuard 서버를 설정하려면 이 동영상을 시청하거나 아래 단계를 참조하세요.

<iframe width="560" height="315" src="https://www.youtube.com/embed/jvc-CNmXfuM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## 공용 IP 주소가 있는지 확인하세요.

인터넷 서비스 제공업체가 공용 IP 주소를 할당하는지 확인하려면 [여기](../tutorials/how_to_check_if_isp_assigns_you_a_public_ip_address.md)를 클릭하세요.

**그렇지 않은 경우 라우터를 WireGuard 서버로 설정할 수 없습니다.**

대체 방법:

1. 기본 라우터가 있는 경우 기본 라우터에 로그인하여 ISP로부터 공용 IP를 받는지 확인하세요.
2. ISP에 공용 IP 주소를 요청하세요. 추가 비용이 발생할 수 있습니다.
3. 위의 두 방법이 작동하지 않는 경우(예: 네트워크가 CGNAT 뒤에 있는 경우) SD-WAN 솔루션인 [AstroWarp](https://www.astrowarp.net/){target="_blank"}을 시도할 수 있습니다.

## 포트 포워딩이 필요한지 확인하세요.

**네트워크 토폴로지**

??? "GL.iNet이 기본 라우터인 경우"

    * GL.iNet 라우터가 네트워크의 기본 라우터인 경우 포트 포워딩이 필요하지 않습니다. [다음 단계](#set-up-wireguard-server)로 이동하세요.

??? "GL.iNet이 서브 라우터인 경우"

    * 기본 라우터를 이미 사용 중이고 GL.iNet 라우터가 보조 라우터로 구성된 경우 기본 라우터에서 [포트 포워딩](../tutorials/how_to_set_up_port_forwarding.md)을 구성해야 합니다.

    * 기본 라우터를 이미 사용 중이고 GL.iNet 라우터가 기본 라우터보다 여러 수준 아래에 있는 경우 각 중간 수준에서 [포트 포워딩](../tutorials/how_to_set_up_port_forwarding.md)을 구성하세요.

## WireGuard 서버 설정

웹 관리 패널에 로그인하고 **VPN** -> **WireGuard Server**로 이동하세요.

1. **Generate Configuration**을 클릭하세요(VPN 서버 초기 설정에만 해당).

    ![generate configuration](https://static.gl-inet.com/docs/router/en/4/tutorials/wireguard_server/generate_configuration.png){class="glboxshadow"}

2. 설정을 확인하세요.

    대부분의 경우 아래와 같이 기본 설정이 작동합니다. 상위 라우터의 게이트웨이와 충돌하지 않는 한 IPv4 주소를 수정할 필요가 없습니다.

    ![check configuration](https://static.gl-inet.com/docs/router/en/4/tutorials/wireguard_server/check_configuration.png){class="glboxshadow"}

    (GL.iNet의 IPv6는 기본적으로 비활성화되어 있습니다. IPv6 주소를 사용하려면 라우터에서 IPv6를 활성화하세요.)

    IPv4 주소가 상위 라우터의 게이트웨이와 충돌하는 것을 발견하면 **10.1.0.1/24**와 같은 다른 주소로 수정하고 **Apply**를 클릭하세요. 연결性问题을 방지하기 위해 "/24" CIDR 표기법이 포함되어 있는지 확인하세요.

    ![modify configuration](https://static.gl-inet.com/docs/router/en/4/tutorials/wireguard_server/modify_configuration.png){class="glboxshadow"}

    예를 들어 GL.iNet 라우터의 상위에 Xfinity 라우터가 있는 경우 Xfinity 라우터의 IP는 10.0.0.1일 수 있으며, 이는 GL.iNet 라우터가 WireGuard 서버로 설정될 때 WireGuard 서버의 터널 IP와 충돌하므로 위의 변경을 수행해야 합니다.

    ![xfinity gateway](https://static.gl.inet.com/docs/router/en/4/tutorials/wireguard_server/xfinitygateway.jpg){class="glboxshadow"}

3. 프로필을 추가합니다.

    **Profiles** 탭으로 전환하고 **Add** 버튼을 클릭하여 장치의 프로필을 생성하세요.

    ![add profiles](https://static.gl.inet.com/docs/router/en/4/tutorials/wireguard_server/add_profiles.png){class="glboxshadow"}

    설명이 포함된 이름을 설정하고 **Apply**를 클릭하여 계속하세요.

    ![profile name](https://static.gl.inet.com/docs/router/en/4/tutorials/wireguard_server/add_profiles_name.png){class="glboxshadow"}

    고급 설정을 설정하려면 **Set More**를 클릭하세요. 그런 다음 **Apply**를 클릭하여 계속하세요.

    ![profile settings](https://static.gl.inet.com/docs/router/en/4/tutorials/wireguard_server/add_profiles_set_more.png){class="glboxshadow"}

    ??? "필요한 경우 경로 규칙 추가하기"

        대부분의 경우 경로 규칙을 추가할 필요가 없습니다.

        서버에서 WireGuard 클라이언트의 LAN 장치에 액세스하려면 **WireGuard Server** 페이지에서 **Route Rules** 탭으로 전환하여 경로 규칙을 설정하세요. 자세한 지침은 [여기](../tutorials/wireguard_server_access_to_client_lan_side.md)를 클릭하세요.

        ![route rules](https://static.gl.inet.com/docs/router/en/4/tutorials/wireguard_server/route_rules.png){class="glboxshadow"}

        그렇지 않은 경우 4단계로 이동하여 클라이언트 설정을 다운로드하세요.

4. 설정을 다운로드합니다.

    프로필을 추가하고 적용하면 QR 코드, 일반 텍스트, .conf 파일의 세 가지 형식으로 설정 파일이 생성됩니다. 선호하는 방법을 선택하여 설정 파일을 가져오세요.

    - **QR 코드**: WireGuard App이 설치된 최종 장치(예: 스마트폰, 태블릿, 노트북)에 적합합니다. 특정 장치를 WireGuard 클라이언트로 설정하려면 WireGuard App을 열고 QR 코드를 스캔하면 설정이 자동으로 가져옵니다.

        ![client configuration qrcode](https://static.gl.inet.com/docs/router/en/4/tutorials/wireguard_server/download_config_qrcode.png){class="glboxshadow"}

    - **일반 텍스트**: 일반 텍스트 형식으로 설정 세부 정보를 검토하고 WireGuard App 또는 GL.iNet 라우터와 같은 다른 곳에 수동으로 구성하기 위해 편리하게 복사하여 붙여넣을 수 있습니다.

        ![client configuration plain text](https://static.gl.inet.com/docs/router/en/4/tutorials/wireguard_server/download_config_text.png){class="glboxshadow"}

    - **.conf 파일**: **Download** 버튼을 클릭하여 .conf 파일을 로컬 장치에 저장하세요. WireGuard 앱 또는 GL.iNet 라우터에 직접 업로드할 수도 있어 편리합니다.

        ![client configuration file](https://static.gl.inet.com/docs/router/en/4/tutorials/wireguard_server/download_config_file.png){class="glboxshadow"}

    필요한 경우 공용 IP, DDNS 도메인, 현재 WAN IP 중에서 서버 주소를 지정할 수 있습니다. 이 기능은 펌웨어 v4.8부터 사용할 수 있습니다. 변경되면 설정 파일의 서버 주소가 동시에 업데이트됩니다.

    예를 들어 네트워크의 공용 IP가 자주 변경되는 경우 [DDNS](ddns.md)를 활성화하고 DDNS 도메인을 서버 주소로 사용하는 것이 좋습니다.

    ![change server address](https://static.gl.inet.com/docs/router/en/4/tutorials/wireguard_server/change_server_address.png){class="glboxshadow"}

5. WireGuard 서버를 시작합니다.

    오른쪽 상단의 **Start** 버튼을 클릭하여 WireGuard 서버를 시작하세요.

    ![start wireguard server](https://static.gl.inet.com/docs/router/en/4/tutorials/wireguard_server/start_wgserver.png){class="glboxshadow"}

    연결 상태가 동일한 페이지에 표시됩니다.

    ![wireguard server status](https://static.gl.inet.com/docs/router/en/4/tutorials/wireguard_server/wgserver_status.png){class="glboxshadow"}

## WireGuard 서버가 제대로 작동하는지 확인하세요.

### 서버 상태 확인

펌웨어 v4.8부터 **WireGuard Server** 페이지에서 서버 연결 상태를 확인할 수 있습니다.

업로드/다운로드 트래픽 통계와 온라인 연결된 장치가 표시되면 WireGuard 서버가 실행 중이며 연결된 WireGuard 클라이언트가 있다는 뜻입니다.

![wireguard server connected](https://static.gl.inet.com/docs/router/en/4/tutorials/wireguard_server/wgserver_status.png){class="glboxshadow"}

트래픽이 0이고 클라이언트가 0이면 연결된 WireGuard 클라이언트가 없다는 뜻입니다.

![wireguard server no client](https://static.gl.inet.com/docs/router/en/4/tutorials/wireguard_server/wgserver_status_no_client.png){class="glboxshadow"}

펌웨어 v4.7 이전 버전은 **VPN Dashboard** 페이지에서 서버 연결 상태를 확인하세요.

### 클라이언트 IP 확인

서버에 대한 연결 성공을 확인하세요: 이전에 내보낸 WireGuard 설정을 서버와 동일한 로컬 네트워크가 아닌 다른 네트워크의 장치에 가져오세요. 그런 다음 웹 브라우저를 열고 IP 주소와 위치를 검색하세요. VPN 서버의 IP(인터넷 서비스 제공업체의 IP가 아님) 및 위치와 일치하면 VPN 연결이 성공한 것입니다.

가장 간단한 방법은 공식 [WireGuard App](https://www.wireguard.com/install){target="_blank"}이 설치된 스마트폰을 사용하는 것입니다. 먼저 스마트폰의 Wi-Fi를 비활성화하고 셀룰러 데이터(4G/5G)를 통해서만 인터넷에 연결하세요. 그런 다음 WireGuard App을 열고 설정 파일을 가져온 다음 연결을 시작하세요. 스마트폰이 인터넷에 액세스할 수 있는지 IP 주소가 WireGuard 서버의 IP와 일치하는지 확인하세요.

연결 실패 시 몇 가지 일반적인 이유가 있습니다:

* 인터넷 서비스 제공업체가 공용 IP 주소를 할당하지 않습니다. [여기](#make-sure-you-have-a-public-ip-address)를 확인하세요.
* 포트 포워딩을 설정해야 할 수 있습니다. [여기](#confirm-if-port-forwarding-is-required)를 확인하세요.
* WireGuard 서버에서 사용하는 포트가 인터넷 서비스 제공업체에서 차단되었습니다. 다른 포트로 변경하거나 인터넷 서비스 제공업체에 추가 지원을 요청하세요.
* 일부 국가/지역에서는 VPN 연결을 차단할 수 있습니다.

## WireGuard App 설치

[WireGuard 공식 웹사이트](https://www.wireguard.com/install){target="_blank"}에서 WireGuard App을 다운로드하세요.

---

WireGuard®는 Jason A.Donenfeld의 등록 상표입니다.

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}을 통해 연락하세요.
