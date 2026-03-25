# AstroRelay를 통해 OpenVPN 서버 설정 방법

이 튜토리얼은 GL.iNet 라우터에서 AstroRelay를 통해 OpenVPN 서버를 설정하는 단계를 소개합니다. 이는 ISP에서 공용 IP 주소를 할당받지 않지만 집이나 사무실 로컬 서비스에 원격으로 액세스해야 하는 사용자에게 이상적입니다.

[AstroRelay](https://www.astrorelay.com){target="_blank"}은 보안 역방향 프록시 터널을 제공하여 NAT 및 방화벽 뒤의 리소스에 안전하게 액세스할 수 있습니다.

1. [이 가이드](../interface_guide/openvpn_server.md)를 따라 GL.iNet 라우터에 OpenVPN 서버를 설정하세요. 공용 IP 주소가 없어도 됩니다.

    ![set up openvpnd server](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_openvpn_server_via_astrorelay/start_ovpn_server4x.jpg){class="glboxshadow"}

    그런 다음 OpenVPN 설정을 내보내세요. 설정 파일 예시입니다.

    ![openvpn config](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_openvpn_server_via_astrorelay/astroovpnpastelink.jpg){class="glboxshadow"}

2. (선택 사항) VPN 서버의 LAN에 원격으로 액세스해야 하는 경우 **Allow Remote Access LAN**을 활성화하세요. 그렇지 않으면 이 단계를 건너뛰세요.

    ??? "펌웨어 v4.7 이하"

        1. 왼쪽 사이드바에서 **VPN** > **VPN Dashboard**를 클릭하세요.
        2. Options 아이콘을 클릭하세요.
        3. **Remote Access LAN** 스위치를 켭니다.
        4. **Apply**를 클릭하세요.

            ![remote access lan](https://static.gl.inet.com/docs/router/en/4/tutorials/build_your_own_openvpn_server/toggle-enable-remote-access-lan.png){class="glboxshadow"}

    ??? "펌웨어 v4.8 이상"

        1. 왼쪽 사이드바에서 **VPN** > **OpenVPN Server**를 클릭하세요.
        2. 우측 상단에서 **Options**를 클릭하세요.
        3. **Allow Remote Access the LAN Subnet** 스위치를 켭니다.
        4. **Apply**를 클릭하세요.

            ![remote access lan](https://static.gl.inet.com/docs/router/en/4/tutorials/build_your_own_openvpn_server/enable-remote-access-lan-4.8.png){class="glboxshadow"}

3. AstroRelay 계정에 가입하고 이 [튜토리얼](https://www.astrorelay.com/tutorial.html){target="_blank"}을 따라 처음 설정을 완료하세요.

    새 도메인을 추가할 때 라우터와 가장 가까운 서버를 선택하세요.

    ![astrorelay add a new domain](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_openvpn_server_via_astrorelay/astrorelay_add_a_new_domain.png){class="glboxshadow"}

    새 링크를 추가할 때 라우터의 **LAN IP 주소**를 **Destination Host IP** 필드에 입력하고 **Destination Port** 필드에 **1194**를 입력하세요.

    ![link for openvpn server](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_openvpn_server_via_astrorelay/astroovpnaddlink.jpg){class="glboxshadow"}

    그러면 **testforx3000.arlab1.cc:37202**와 같은 링크가 생성됩니다. 클릭하여 링크를 복사하세요.

    ![astrorelay link](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_openvpn_server_via_astrorelay/astroovpncopylink.jpg){class="glboxshadow"}

4. OpenVPN 설정 파일을 열고 **Remote** 뒤의 값을 이전 단계에서 얻은 링크로 바꾸고 변경 사항을 적용하세요. 아래 예제에서 "42.200.00.00 1194"를 "testforx3000.arlab1.cc:37202" 링크로 바꿉니다. 그런 다음 콜론 ":"을 공백으로 바꾸고 변경 사항을 적용하세요.

    ![openvpn config](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_openvpn_server_via_astrorelay/astroovpnpastelink.jpg){class="glboxshadow"}

    ![replace link](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_openvpn_server_via_astrorelay/astroovpnconfig.jpg){class="glboxshadow"}

5. OpenVPN 클라이언트로 사용할 장치에 [OpenVPN Connect 앱](https://openvpn.net/client/){target="_blank"}을 설치하세요. 그런 다음 수정된 설정 파일을 앱에 업로드하고 연결을 시작하세요. 또는 다른 GL.iNet 라우터에 업로드하여 OpenVPN 클라이언트로 설정할 수도 있습니다.

    연결되면 집이나 사무실 로컬 서비스에 원격으로 액세스할 수 있습니다.

    ![openvpn up](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_openvpn_server_via_astrorelay/astroovpnup.jpg){class="glboxshadow"}

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}을 통해 연락하세요.
