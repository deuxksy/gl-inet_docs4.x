# GL.iNet 라우터에서 VPN Cascading 사용 방법

## 소개

VPN Cascading은 일부 맥락에서 "Double VPN"이라고도 불리지만 GL.iNet 라우터에서는 약간 다를 수 있습니다. 핵심 개념은 아래와 같습니다.

![gl.inet vpn cascading](https://static.gl.inet.com/docs/router/en/4/tutorials/vpn_cascading/mt2500_vpn-cascading.jpg){class="glboxshadow"}

**VPN 1 (라우터를 VPN 서버로 사용)**: 라우터가 VPN 서버로 작동할 때 이 서버에 연결된 클라이언트는 기본적으로 라우터의 ISP 네트워크를 통해 인터넷에 액세스합니다.

**VPN 2 (라우터를 VPN 클라이언트로 사용)**: 라우터는 또한 제3자 VPN 서비스에 연결되는 VPN 클라이언트로도 작동합니다.

**VPN Cascading**: 라우터는 VPN 1 터널의 트래픽을 VPN 2 터널로 전달하여 VPN 1을 통해 라우터에 연결된 장치가 라우터의 ISP 네트워크 대신 제3자 VPN 서비스(VPN 2)를 통해 인터넷에 액세스할 수 있게 합니다.

## VPN Cascading 활성화

### 펌웨어 v4.7 이하

1. 먼저 라우터를 VPN 서버로 설정하세요. 더 빠른 속도를 위해 WireGuard 프로토콜을 권장합니다. [이 링크](../interface_guide/wireguard_server.md){target="_blank"}를 참조하세요.

2. 라우터에서 설정 파일을 내보내고 VPN을 통해 라우터에 연결할 클라이언트 장치에 업로드하세요.

3. 제3자 VPN 서비스에 연결되도록 라우터를 VPN 클라이언트로 설정하세요. 더 빠른 속도를 위해 WireGuard 프로토콜을 권장합니다. [이 링크](../interface_guide/wireguard_client.md){target="_blank"}를 참조하세요.

4. 연결되면 **VPN Dashboard** 페이지가 아래와 같이 표시됩니다. 라우터가 동시에 VPN 서버와 VPN 클라이언트로 설정되었습니다.

    ![vpn dashboard](https://static.gl.inet.com/docs/router/en/4/tutorials/vpn_cascading/4.7-vpn-dashboard.png){class="glboxshadow"}

    같은 페이지의 VPN Server 섹션으로 이동하고 **Global Options**를 클릭하세요.

    ![global options](https://static.gl.inet.com/docs/router/en/4/tutorials/vpn_cascading/4.7-global-options.png){class="glboxshadow"}

    **VPN Cascading**을 활성화하고 **Apply**를 클릭하세요.

    ![enable vpn cascading](https://static.gl.inet.com/docs/router/en/4/tutorials/vpn_cascading/enable_vpn_cascading.png){class="glboxshadow gl-80-desktop"}

5. VPN Cascading이 활성화되었습니다. VPN을 통해 라우터에 연결된 장치는 라우터의 ISP 네트워크 대신 제3자 VPN 서비스를 통해 인터넷에 액세스합니다.

### 펌웨어 v4.8 이상

1. 먼저 라우터를 VPN 서버로 설정하세요. 더 빠른 속도를 위해 WireGuard 프로토콜을 권장합니다. [이 링크](../interface_guide/wireguard_server.md){target="_blank"}를 참조하세요.

2. 라우터에서 설정 파일을 내보내고 VPN을 통해 라우터에 연결할 클라이언트 장치에 업로드하세요.

3. 제3자 VPN 서비스에 연결되도록 라우터를 VPN 클라이언트로 설정하세요. 더 빠른 속도를 위해 WireGuard 프로토콜을 권장합니다. [이 링크](../interface_guide/wireguard_client.md){target="_blank"}를 참조하세요.

4. 웹 관리 패널에서 **VPN Dashboard**로 이동하세요. VPN 모드에 따라 아래 지침을 따르세요.

    ??? "Global Mode"

        VPN 모드가 Global Mode인 경우 VPN 클라이언트가 활성화되면(아래와 같이) VPN Cascading이 자동으로 활성화됩니다.

        VPN을 통해 라우터에 연결된 장치는 라우터의 ISP 네트워크 대신 제3자 VPN 서비스를 통해 인터넷에 액세스합니다.

        ![vpn connected global mode](https://static.gl.inet.com/docs/router/en/4/tutorials/vpn_cascading/4.8-global-mode.png){class="glboxshadow"}

    ??? "Policy Mode"

        VPN 모드가 Policy Mode인 경우 VPN 터널 규칙을 설정해야 합니다.

        왼쪽 회색 상자를 클릭하세요.

        ![traffic from](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/traffic_from_1.png){class="glboxshadow"}

        이 규칙을 적용할 트래픽 소스를 선택하세요. VPN Cascading을 활성화하려면 **All Clients**를 선택하거나 **Specified Connection Types**를 선택한 다음 **WireGuard/OpenVPN Server**를 선택하세요.

        ![select traffic source](https://static.gl.inet.com/docs/router/en/4/tutorials/vpn_cascading/select_traffic.jpg){class="glboxshadow"}

        - **All Clients**: 모든 LAN 장치, Drop-in Gateway의 장치, 게스트 네트워크의 장치, VPN을 통해 라우터에 연결된 장치가 포함됩니다.

            모든 장치의 트래픽에 동일한 터널 규칙을 적용하려면 **All Clients**를 선택하고 **Apply**를 클릭하세요.

            ![all clients](https://static.gl.inet.com/docs/router/en/4/tutorials/vpn_cascading/all_clients.png){class="glboxshadow"}

        - **Specified Connection Types**: 특정 방법(예: VPN을 통해 연결된 장치)을 통해 라우터에 연결된 장치에 이 터널 규칙을 적용할 수 있습니다.

            라우터의 VPN 클라이언트에 다른 규칙을 적용하려면 **WireGuard/OpenVPN Server**를 선택하고 **Apply**를 클릭하세요.

            ![specified connection](https://static.gl.inet.com/docs/router/en/4/tutorials/vpn_cascading/specified_connection_types.png){class="glboxshadow"}

            이것은 Policy Mode에서의 VPN 터널 규칙 예시입니다.

            ![vpn dashboard](https://static.gl.inet.com/docs/router/en/4/tutorials/vpn_cascading/4.8-vpn-dashboard.png){class="glboxshadow"}

5. VPN Cascading이 활성화되었습니다. VPN을 통해 라우터에 연결된 장치는 라우터의 ISP 네트워크 대신 제3자 VPN 서비스를 통해 인터넷에 액세스합니다.

6. **연결 테스트**: VPN을 통해 라우터에 연결된 노트북에서 브라우저를 열고 [What Is My IP](https://whatismyipaddress.com/){target="_blank"}을 방문하여 공용 IP를 확인하세요.

    노트북의 IP 주소가 제3자 VPN 서버 지역(이 지침에서는 부에노스아이레스)에 있으면 VPN Cascading이 적용된 것입니다.

    ![vpn test](https://static.gl.inet.com/docs/router/en/4/tutorials/vpn_cascading/4.8-ipcheck.png){class="glboxshadow"}

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}을 통해 연락하세요.
