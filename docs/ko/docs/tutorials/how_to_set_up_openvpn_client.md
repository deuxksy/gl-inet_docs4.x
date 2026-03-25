# GL.iNet 라우터에 OpenVPN 클라이언트 설정 방법

이 튜토리얼은 GL.iNet 라우터에 OpenVPN 클라이언트를 설정하는 방법을 안내합니다.

비디오를 시청하거나 아래 단계를 참조하세요.

<iframe width="560" height="315" src="https://www.youtube.com/embed/04sW3l6_rDM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

---

시작하기 전에 OpenVPN 수동 설정을 지원하는 VPN 서비스 제공업체의 활성 구독이 있는지 확인하세요. GL.iNet과 호환되는 OpenVPN 제공업체를 확인하려면 [여기](https://www.gl-inet.com/solutions/vpn/){target="_blank"}를 클릭하세요.

다음은 라우터의 웹 관리 패널을 통해 OpenVPN 클라이언트를 설정하는 단계입니다.

## 1. 라우터에 로그인하세요

웹 브라우저를 열고 라우터의 웹 관리 패널에 액세스하세요(기본 IP: 192.168.8.1). 관리자 비밀번호로 로그인하세요.

![log in](https://static.gl.inet.com/docs/router/en/4/tutorials/build_your_own_openvpn_server/router-login.jpeg){class="glboxshadow"}

## 2. VPN 클라이언트 설정

사용 중인 VPN 서비스 제공업체에 해당하는 섹션을 참조하세요.

??? "NordVPN"

    1. 라우터의 웹 관리 패널에서 **VPN** > **OpenVPN Client**로 이동하세요.

    2. **NordVPN**을 클릭하세요.

        ![nordvpn](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_openvpn_client/click-nordvpn.png){class="glboxshadow"}

    3. 서비스 자격 증명을 입력한 다음 **Save and Continue**를 클릭하세요.

        참고: 로그인 계정 이메일/비밀번호가 아니라 NordVPN 웹사이트 -> Nord Dashboard에서 얻은 서비스 자격 증명입니다.

        ![save and continue](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_openvpn_client/click-save-and-continue.png){class="glboxshadow"}

    4. 프롬프트에서 연결하려는 VPN 위치를 선택한 다음 **Apply**를 클릭하세요.

        ![apply](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_openvpn_client/nordvpn-servers-click-apply.png){class="glboxshadow"}

    5. 연결하려는 VPN 서버를 선택하고 점 3개 아이콘을 클릭한 다음 **Start**를 클릭하세요.

        ![start](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_openvpn_client/openvpn-click-start.png){class="glboxshadow"}

??? "기타 VPN 서비스 제공업체 (예: Surfshark)"

    1. 라우터의 웹 관리 패널에서 **VPN** > **OpenVPN Client**로 이동하세요.

    2. **Add Manually**를 클릭하세요.

        ![add manually](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_openvpn_client/openvpn-click-add-manually.png){class="glboxshadow"}

    3. 이름을 설정하세요. VPN 서비스 제공업체의 이름을 입력한 다음 확인 아이콘을 클릭하세요.

        ![click-check-icon](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_openvpn_client/click-check-icon.png){class="glboxshadow"}

    4. VPN 서비스 제공업체에서 제공하는 설정 파일을 다운로드했고 필요한 경우 서비스 자격 증명도 있는지 확인하세요.
    5. 다운로드한 설정 파일을 업로드하세요.

        필요한 경우 서비스 자격 증명을 입력한 다음 **Apply**를 클릭하세요.

        ![apply](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_openvpn_client/openvpn-click-apply.png){class="glboxshadow"}

    6. VPN 서버 주소 옆에서 점 3개 아이콘을 클릭하고 **Start**를 클릭하세요.

        ![start](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_openvpn_client/openvpn-manual-click-start.png){class="glboxshadow"}

## 3. VPN 연결 확인

웹 브라우저를 열고 IP 주소와 위치를 검색하세요. VPN 서버의 IP(인터넷 서비스 제공업체의 IP가 아님)와 위치와 일치하면 VPN 연결이 성공한 것입니다.

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}을 통해 연락하세요.
