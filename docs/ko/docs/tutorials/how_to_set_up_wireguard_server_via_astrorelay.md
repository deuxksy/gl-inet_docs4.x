# AstroRelay를 통해 WireGuard 서버 설정 방법

이 튜토리얼은 GL.iNet 라우터에서 AstroRelay를 통해 WireGuard 서버를 설정하는 단계를 소개합니다. 이는 ISP에서 공용 IP 주소를 할당받지 않지만 집이나 사무실 로컬 서비스에 원격으로 액세스해야 하는 사용자에게 이상적입니다.

[AstroRelay](https://www.astrorelay.com){target="_blank"}은 보안 역방향 프록시 터널을 제공하여 NAT 및 방화벽 뒤의 리소스에 안전하게 액세스할 수 있습니다.

1. [이 가이드](../interface_guide/wireguard_server.md)를 따라 GL.iNet 라우터에 WireGuard 서버를 설정하세요. 공용 IP 주소가 없어도 됩니다.

    ![set up wireguard server](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_wireguard_server_via_astrorelay/start_wg_server4x.jpg){class="glboxshadow"}

    그런 다음 **Profiles**를 클릭하여 WireGuard 설정을 내보내세요. 설정 파일 예시입니다.

    ![wireguard config](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_wireguard_server_via_astrorelay/wireguard_config.png){class="glboxshadow"}

2. (선택 사항) VPN 서버의 LAN에 원격으로 액세스해야 하는 경우 **Allow Remote Access LAN**을 활성화하세요. 그렇지 않으면 이 단계를 건너뛰세요.

    ??? "펌웨어 v4.7 이하"

        서버의 웹 관리 패널에서 **VPN** -> **VPN Dashboard** -> **VPN Server** 섹션으로 이동하세요. WireGuard 서버 우측의 기어 아이콘을 클릭하세요.

        ![server options 4.7](https://static.gl.inet.com/docs/router/en/4/tutorials/access_server_lan_via_domain_names/server_options_4.7.png){class="glboxshadow gl-90-desktop"}

        **Remote Access LAN**을 활성화하고 **Apply**를 클릭하세요.

        ![server allow access lan 4.7](https://static.gl.inet.com/docs/router/en/4/tutorials/access_server_lan_via_domain_names/server-allow-access-lan-4.7.png){class="glboxshadow"}

        **활성화되면 이 라우터와 LAN 장치에 VPN을 통해 원격으로 액세스할 수 있습니다.**

    ??? "펌웨어 v4.8 이상"

        서버의 웹 관리 패널에서 **VPN** -> **WireGuard Server**로 이동하세요. 우측 상단에서 **Options**를 클릭하세요.

        ![server options 4.8](https://static.gl.inet.com/docs/router/en/4/tutorials/access_server_lan_via_domain_names/server_options_4.8.png){class="glboxshadow gl-90-desktop"}

        **Allow Remote Access the LAN Subnet**을 활성화하고 **Apply**를 클릭하세요.

        ![server allow access lan 4.8](https://static.gl.inet.com/docs/router/en/4/tutorials/access_server_lan_via_domain_names/server-allow-access-lan-4.8.png){class="glboxshadow"}

        **활성화되면 이 라우터와 LAN 장치에 VPN을 통해 원격으로 액세스할 수 있습니다.**

3. AstroRelay 계정에 가입하고 이 [튜토리얼](https://www.astrorelay.com/tutorial.html){target="_blank"}을 따라 처음 설정을 완료하세요.

    새 도메인을 추가할 때 라우터와 가장 가까운 서버를 선택하세요.

    ![astrorelay add a new domain](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_wireguard_server_via_astrorelay/astrorelay_add_a_new_domain.png){class="glboxshadow"}

    새 링크를 추가할 때 라우터의 **LAN IP 주소**를 **Destination Host IP** 필드에 입력하고 **Destination Port** 필드에 **51820**을 입력하세요.

    ![link for wireguard server](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_wireguard_server_via_astrorelay/astrorelay_wg_server.png){class="glboxshadow"}

    그러면 **wg_server_test.arlab1.cc:33331**과 같은 링크가 생성됩니다. 클릭하여 링크를 복사하세요.

    ![astrorelay link](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_wireguard_server_via_astrorelay/astrorelay_link.png){class="glboxshadow"}

4. WireGuard 설정 파일을 열고 **Endpoint** 뒤의 값을 이전 단계에서 얻은 링크로 바꾸고 변경 사항을 적용하세요.

    ![replace link in wireguard config](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_wireguard_server_via_astrorelay/replace_endpoint_in_wireguard_config.png){class="glboxshadow"}

5. WireGuard 클라이언트로 사용할 장치에 [WireGuard 앱](https://www.wireguard.com/install/){target="_blank"}을 설치하세요. 그런 다음 수정된 설정 파일을 앱에 업로드하고 연결을 시작하세요. 또는 다른 GL.iNet 라우터에 업로드하여 WireGuard 클라이언트로 설정할 수도 있습니다.

    연결되면 집이나 사무실 로컬 서비스에 원격으로 액세스할 수 있습니다.

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}을 통해 연락하세요.
