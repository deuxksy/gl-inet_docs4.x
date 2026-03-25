# GL.iNet 라우터의 WireGuard 서버가 제대로 작동하지 않음

GL.iNet 라우터에 설정한 WireGuard 서버가 제대로 작동하지 않는 데에는 여러 가지 이유가 있습니다.

문제가 발생하면 특정 상황에 따라 다음 문제 해결 단계를 따르세요.

#### 상황 1: WireGuard 서버가 시작되지만 연결할 수 없음

??? "단계 따르기"

    ![client](https://static.gl.inet.com/docs/router/en/4/faq/troubleshooting/my_wireguard_server_is_not_working/client.jpg){class="glboxshadow"}

    기본 라우터에 설정한 포트 포워딩이 제대로 작동하지 않을 수 있습니다. 2차 라우터(GL.iNet)에 연결된 기본 라우터에 설정한 포트 포워딩이 제대로 작동하는지 확인하려면 기본 라우터의 HTTPS 포트를 WireGuard 서버로 포워딩해 보세요. 다음 단계를 따르세요:

    1. 기본 라우터의 HTTPS 포트를 WireGuard 서버로 포워딩

        1. 기본 라우터의 관리 패널에 로그인하세요.
        2. 포트 포워딩 화면으로 이동하세요.
        3. 새 포트를 만들고 **HTTPS**라고 이름을 지정하세요.
        4. 다음 정보를 입력하세요:
            * **외부 포트/내부 포트:** **443**을 입력하세요.
            * **프로토콜:** **All** 또는 **UDP/TCP**를 선택하세요.
            * **내부 IP**(또는 **호스트 IP**로 표시됨): 2차 라우터의 WAN IP 주소를 입력하거나 드롭다운에서 2차 라우터를 선택하세요.
            ![DDNS1](https://static.gl.inet.com/docs/router/en/4/faq/troubleshooting/my_wireguard_server_is_not_working/ddns1.jpg){class="glboxshadow"}

    2. DDNS 및 HTTPS 원격 액세스 활성화(GL.iNet 라우터에서)

        1. 웹 브라우저에서 GL.iNet 라우터의 관리 패널 URL(예: 192.168.8.1)을 입력하고 로그인하세요.
        2. 왼쪽 사이드바에서 **응용 프로그램** > **동적 DNS**를 클릭하세요.
        3. **DDNS 활성화**를 켜기로 토글하고 **서비스 약관 및 개인정보 처리방침을 읽었으며 동의합니다** 확인란을 선택하세요.
            ![DDNS2](https://static.gl.inet.com/docs/router/en/4/faq/troubleshooting/my_wireguard_server_is_not_working/ddns2.jpg){class="glboxshadow"}
        4. 나중에 필요하므로 호스트 이름을 어딘가에 저장한 다음 **적용**을 클릭하세요.
        5. 왼쪽 사이드바에서 **시스템** > **보안**을 클릭하세요.
        6. **원격 액세스 제어**에서 **HTTPS 원격 액세스**를 켜기로 토글하세요.
            ![DDNS3](https://static.gl.inet.com/docs/router/en/4/faq/troubleshooting/my_wireguard_server_is_not_working/ddns3.jpg){class="glboxshadow"}
        7. **적용**을 클릭하세요.

    3. GL.iNet 라우터의 관리 패널에 액세스할 수 있는지 확인하세요

        1. 다른 장치(예: 노트북 또는 모바일 장치)에서 다른 Wi-Fi 네트워크 또는 셀룰러 네트워크에 연결하세요.
        2. 웹 브라우저의 주소 표시줄에 earlier에 저장한 호스트 이름(abcd123.glddns.com)을 입력하세요.
        3. **고급**을 클릭하세요.
            ![DDNS4](https://static.gl.inet.com/docs/router/en/4/faq/troubleshooting/my_wireguard_server_is_not_working/ddns4.jpg){class="glboxshadow"}
        4. **abcd123.glddns.com(안전하지 않음)으로 계속**을 클릭하세요.
            ![DDNS5](https://static.gl.inet.com/docs/router/en/4/faq/troubleshooting/my_wireguard_server_is_not_working/ddns5.jpg){class="glboxshadow"}

    GL.iNet 라우터(2차 라우터)의 로그인 화면이 표시되면 기본 라우터에 설정한 포트 포워딩이 제대로 작동하는 것입니다.

    ![DDNS6](https://static.gl.inet.com/docs/router/en/4/faq/troubleshooting/my_wireguard_server_is_not_working/ddns6.jpg){class="glboxshadow"}

    GL.iNet 라우터(2차 라우터)의 로그인 화면이 표시되지 않으면 포트 포워딩이 제대로 작동하지 않는 것입니다. 포트 포워딩을 다시 설정하거나 포트 포워딩 기능이 작동하는 라우터를 기본 라우터로 사용하세요.

#### 상황 2: WireGuard 서버에 VPN 클라이언트가 연결된 것으로 표시되지만 VPN 클라이언트가 인터넷에 액세스할 수 없음

??? "단계 따르기"

    각 가능한 원인에 대해 아래에 설명된 단계를 따르고 문제가 해결되었는지 확인하세요. 문제가 해결되면 나머지 섹션을 건너뛸 수 있습니다.

    **가능한 원인 1: 인터넷 서비스 공급자가 GL.iNet의 DNS 서버를 확인할 수 없을 수 있습니다**

    다음 단계에 따라 DNS 서버 주소를 수동으로 구성해 보세요:

    1. 웹 브라우저에서 GL.iNet 라우터의 관리 패널 URL(예: 192.168.8.1)을 입력하고 로그인하세요.
    2. 왼쪽 사이드바에서 **네트워크** > **DNS**를 클릭하세요.
    3. **모드**에서 **수동 DNS**를 선택하세요.
    4. **DNS 서버 1**에서 **Google 공개 DNS**를 선택하세요.
    5. **적용**을 클릭하세요.

    **가능한 원인 2: 기본 라우터의 게이트웨이 IP가 WireGuard 서버의 IP 주소와 충돌합니다**

    다음 단계에 따라 IPv4 주소를 변경해 보세요:

    1. 웹 브라우저에서 GL.iNet 라우터의 관리 패널 URL(예: 192.168.8.1)을 입력하고 로그인하세요.
    2. 왼쪽 사이드바에서 **VPN** > **WireGuard 서버**를 클릭하세요.
    3. **구성** 탭에서 **IPv4 주소** 필드에 새 IP 주소(예: 10.1.0.1/24)를 입력하세요.
    4. **적용**을 클릭하세요.

    **가능한 원인 3: WireGuard 서버와 WireGuard 클라이언트가 모두 GL.iNet 라우터에 설정된 경우 LAN IP 주소가 충돌합니다**

    다음 단계에 따라 두 라우터 중 하나의 LAN IP 주소를 변경하세요:

    1. 웹 브라우저에서 GL.iNet 라우터 중 하나의 관리 패널(예: 192.168.8.1)에 로그인하세요.
    2. 왼쪽 사이드바에서 **네트워크** > **LAN**을 클릭하세요.
    3. **라우터 IP 주소** 필드에 새 LAN IP 주소(예: 192.168.10.1)를 입력하세요.
    4. **적용**을 클릭하세요.

    **가능한 원인 4: WireGuard 서버의 IP 주소가 업데이트되었지만 서브넷이 누락되었습니다**

    다음 단계에 따라 WireGuard 서버 IP 주소에 서브넷을 추가하세요:

    1. 웹 브라우저에서 GL.iNet 라우터의 관리 패널 URL(예: 192.168.8.1)을 입력하고 로그인하세요.
    2. 왼쪽 사이드바에서 **VPN** > **WireGuard 서버**를 클릭하세요.
    3. **구성** 탭에서 **IPv4 주소** 필드의 **10.0.0.1** 뒤에 **/24**를 추가하세요.
    4. **적용**을 클릭하세요.

#### 상황 3: WireGuard 서버가 실행 중이지만 VPN 클라이언트를 연결할 수 없음

??? "단계 따르기"

    각 가능한 원인에 대해 아래에 설명된 단계를 따르고 문제가 해결되었는지 확인하세요. 문제가 해결되면 나머지 섹션을 건너뛸 수 있습니다.

    **가능한 원인 1: 기본 라우터에 설정한 포트 포워딩이 제대로 작동하지 않을 수 있습니다**

    포트 포워딩이 제대로 작동하는지 확인하려면 상황 1에 설명된 해결 단계에 따라 HTTPS 포트를 WireGuard 서버로 포워딩해 보세요.

    **가능한 원인 2: 공개 IP 주소가 없을 수 있습니다**

    공개 IP 주소가 있는지 확인하려면 [이 페이지](https://docs.gl-inet.com/router/en/4/tutorials/how_to_check_if_isp_assigns_you_a_public_ip_address/)를 따르세요.

    **가능한 원인 3: WireGuard 서버와 WireGuard 클라이언트가 모두 GL.iNet 라우터에 설정된 경우 LAN IP 주소가 충돌합니다**

    다음 단계에 따라 두 라우터 중 하나의 LAN IP 주소를 변경하세요:

    1. 웹 브라우저에서 GL.iNet 라우터 중 하나의 관리 패널(예: 192.168.8.1)에 로그인하세요.
    2. 왼쪽 사이드바에서 **네트워크** > **LAN**을 클릭하세요.
    3. **라우터 IP 주소** 필드에 새 LAN IP 주소(예: 192.168.10.1)를 입력하세요.
    4. **적용**을 클릭하세요.

    **가능한 원인 4: WireGuard 서버에 연결하는 데 사용하는 장치가 Wi-Fi 네트워크 또는 LAN 포트에 연결되어 있습니다**

    장치를 다른 Wi-Fi 네트워크 또는 셀룰러 네트워크에 연결하세요.

    **가능한 원인 5: 클라이언트 장치에 업로드한 구성 파일에 일부 줄이 누락되었을 수 있습니다**

    구성 정보를 다시 업로드하세요.

#### 상황 4: WireGuard 서버에 연결되었지만 연결이 안정적이지 않음

??? "단계 따르기"

    다음 단계에 따라 문제를 해결하세요. 각 단계 후 문제가 해결되었는지 확인하세요. 문제가 해결되면 나머지 단계를 건너뛸 수 있습니다.

    1. VPN 클라이언트 장치에서 MTU를 **1420**에서 더 작은 값(예: **1380**)으로 변경하세요.
    2. 기본 라우터에서 VPN passthrough 기능을 사용할 수 있다면 활성화하세요.
    3. 다음 단계에 따라 GL.iNet 라우터에서 DNS 서버를 수동으로 구성해 보세요:
        1. 웹 브라우저에서 GL.iNet 라우터의 관리 패널 URL(예: 192.168.8.1)을 입력하고 로그인하세요.
        2. 왼쪽 사이드바에서 **네트워크** > **DNS**를 클릭하세요.
        3. 모드에서 **수동 DNS**를 선택하세요.
        4. **DNS 서버 1**에서 **Google 공개 DNS**를 선택하세요.
        5. **적용**을 클릭하세요.

#### 상황 5: WireGuard 서버가 갑자기 작동을 멈춤

??? "단계 따르기"

    각 가능한 원인에 대해 아래에 설명된 단계를 따르고 문제가 해결되었는지 확인하세요. 문제가 해결되면 나머지 섹션을 건너뛸 수 있습니다.

    **가능한 원인 1: WireGuard 서버를 설정한 곳에 정전이 발생했을 수 있습니다**

    상황 1에 설명된 해결 단계에 따라 또는 [GoodCloud](https://docs.gl-inet.com/router/en/4/interface_guide/cloud/)(이전에 라우터를 연결한 경우)를 통해 WireGuard 서버가 여전히 온라인인지 확인하세요.

    **가능한 원인 2: 동적 DNS(DDNS)를 활성화하지 않았습니다**

    동적 IP 주소(대부분의 경우)를 사용하는 경우 DDNS를 활성화해야 합니다. [DDNS 활성화](https://www.youtube.com/watch?v=qLEj9zoiYRs&t=26s)하고 나머지 단계에 따라 WireGuard 서버를 다시 설정하세요.

    **가능한 원인 3: 포트 포워딩이 알 수 없는 이유로 작동을 멈추었습니다**

    다른 포트로 [포트 포워딩 설정](https://docs.gl-inet.com/router/en/4/tutorials/how_to_set_up_port_forwarding/)을 다시 하세요.

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}을 통해 연락하세요.
