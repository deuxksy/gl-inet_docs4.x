# GL.iNet 라우터에 OpenVPN 서버 설정 방법

이 튜토리얼은 GL.iNet 라우터에 OpenVPN 서버를 설정하는 방법을 안내합니다. VPN 서버를 사용하면 집이나 사무실 네트워크에 보안 연결을 원격으로 설정할 수 있습니다. GL.iNet 라우터를 사용하면 몇 분 만에 OpenVPN 서버를 설정할 수 있습니다.

!!! note "시작하기 전에 다음 요구 사항을 충족하는지 확인하세요"

    **공용 IP 주소**

    OpenVPN 서버를 설정하려면 공용 IP 주소가 필요합니다. 공용 IP 주소가 있는지 확인하려면 [이 링크](https://docs.gl-inet.com/router/en/4/tutorials/how_to_check_if_isp_assigns_you_a_public_ip_address/)를 참조하세요.

    **포트 포워딩**

    GL.iNet 라우터가 기본 라우터 뒤에 연결된 경우 [기본 라우터에서 포트 포워딩을 설정하세요](https://docs.gl-inet.com/router/en/4/tutorials/how_to_set_up_port_forwarding/).

## 1. 라우터에 로그인하세요

웹 브라우저를 열고 라우터의 웹 관리 패널에 액세스하세요(기본 IP: 192.168.8.1). 관리자 비밀번호로 로그인하세요.

![log in](https://static.gl.inet.com/docs/router/en/4/tutorials/build_your_own_openvpn_server/router-login.jpeg){class="glboxshadow"}

## 2. Dynamic DNS 활성화 (선택 사항)

OpenVPN 서버를 설정하려면 일반적으로 **고정 공용 IP 주소**가 필요합니다. 이는 다른 장치가 VPN 서버에 액세스할 수 있는 고정된 끝점을 제공합니다.

그러나 고정 공용 IP 주소가 없고 예를 들어 동적 IP 주소가 있는 경우 GL.iNet 라우터에서 **Dynamic DNS (DDNS)**를 활성화해야 할 수 있습니다. 이를 통해 공용 IP 주소가 동적으로 변경되더라도 OpenVPN 서버에 지속적으로 연결할 수 있습니다.

다음 단계에 따라 Dynamic DNS를 활성화하세요.

1. 라우터의 웹 관리 패널에서 **APPLICATIONS** > **Dynamic DNS**로 이동하세요.
![dynamic DNS](https://static.gl.inet.com/docs/router/en/4/tutorials/build_your_own_openvpn_server/click-dynamic-dns.jpeg){class="glboxshadow"}
2. **Enable DDNS**를 토글로 켜고 **서비스 약관 및 개인정보 처리방침**을 읽고 동의한 다음 **Apply**를 클릭하세요.
![apply](https://static.gl.inet.com/docs/router/en/4/tutorials/build_your_own_openvpn_server/dynamic-dns-click-apply.png){class="glboxshadow"}

## 3. 설정 파일 다운로드

1. 라우터의 웹 관리 패널에서 **VPN** > **OpenVPN Server**로 이동하세요.
2. **Generate Configuration**을 클릭하세요.
3. 기본 설정을 그대로 유지한 다음 **Export Client Configuration**을 클릭하세요.
![click export](https://static.gl.inet.com/docs/router/en/4/tutorials/build_your_own_openvpn_server/click-export-client-configuration.jpeg){class="glboxshadow"}
4. 팝업 창에서 이전에 **Dynamic DNS**를 설정한 경우 **Use DDNS Domain** 스위치를 켭니다.
5. **Download**를 클릭한 다음 파일을 저장하세요.
6. **OpenVPN Server** 페이지 상단에서 **Start**를 클릭하세요.
![click start](https://static.gl.inet.com/docs/router/en/4/tutorials/build_your_own_openvpn_server/openvpn-server-click-start.jpeg){class="glboxshadow"}

??? "(선택 사항) VPN 서버의 로컬 네트워크에 액세스하려면 다음 설정을 활성화하세요:"

    펌웨어 v4.7 이하:

    1. 왼쪽 사이드바에서 **VPN** > **VPN Dashboard**를 클릭하세요.
    2. Options 아이콘을 클릭하세요.
    3. **Remote Access LAN** 스위치를 켭니다.
    4. **Apply**를 클릭하세요.

        ![remote access lan](https://static.gl.inet.com/docs/router/en/4/tutorials/build_your_own_openvpn_server/toggle-enable-remote-access-lan.png){class="glboxshadow"}

    펌웨어 v4.8 이상:

    1. 왼쪽 사이드바에서 **VPN** > **OpenVPN Server**를 클릭하세요.
    2. 우측 상단에서 **Options**를 클릭하세요.
    3. **Allow Remote Access the LAN Subnet** 스위치를 켭니다.
    4. **Apply**를 클릭하세요.

        ![remote access lan](https://static.gl.inet.com/docs/router/en/4/tutorials/build_your_own_openvpn_server/enable-remote-access-lan-4.8.png){class="glboxshadow"}


## 4. OpenVPN 서버에 연결

OpenVPN 서버에 연결하려면 OpenVPN 클라이언트가 필요합니다. 다음 방법 중 하나를 사용하여 설정할 수 있습니다.

??? "방법 1: 서드파티 OpenVPN 클라이언트 앱 (OpenVPN 클라이언트 설정을 지원하는 추가 라우터가 없는 경우 이 방법 사용)"

    이 튜토리얼에서는 OpenVPN Inc에서 개발한 공식 앱인 OpenVPN Connect 앱을 예로 사용합니다.

    1. 다른 장치에서 다른 Wi-Fi 네트워크에 연결하세요(모바일 장치를 사용하는 경우 셀룰러에 연결).
    2. 이전에 다운로드한 설정 파일을(예: 이메일로) 장치로 보낸 다음 파일을 다운로드하세요.
    3. 장치 운영 체제에 맞는 OpenVPN Connect를 다운로드하세요:
        * [Windows](https://openvpn.net/client/client-connect-vpn-for-windows/)
        * [Mac](https://openvpn.net/client-connect-vpn-for-mac-os/)
        * [Android](https://play.google.com/store/apps/details?id=net.openvpn.openvpn&hl=en&gl=US&pli=1)
        * [iOS](https://apps.apple.com/us/app/openvpn-connect-openvpn-app/id590379981)
        * [Linux](https://openvpn.net/openvpn-client-for-linux/)
    4. 앱에서 이용약관을 읽고 **Agree**를 선택하세요.
    5. **Upload File**을 선택하세요.
![upload file](https://static.gl.inet.com/docs/router/en/4/tutorials/build_your_own_openvpn_server/tap-upload-file.png){class="glboxshadow"}
    6. **Browse**를 선택한 다음 이전에 다운로드한 설정 파일을 선택하세요.
    7. **OK**를 선택하세요.
        ![tap ok](https://static.gl.inet.com/docs/router/en/4/tutorials/build_your_own_openvpn_server/tap-ok.png){class="glboxshadow"}
    8. **Connect** > **OK** > **Allow**를 선택하세요.

    VPN 프로필 상단에 "Connected" 단어가 표시됩니다.
    ![connected status](https://static.gl.inet.com/docs/router/en/4/tutorials/build_your_own_openvpn_server/connected-status.png){class="glboxshadow"}

??? "방법 2: OpenVPN 클라이언트 설정을 지원하는 라우터"

    OpenVPN 클라이언트 수동 설정을 지원하는 모든 라우터를 사용할 수 있습니다. 이 튜토리얼에서는 GL.iNet의 트래블 라우터 [Beryl AX (GL-MT3000)](https://www.gl-inet.com/products/gl-mt3000/)을 예로 사용합니다.

    1. 다른 장치에서 다른 Wi-Fi 네트워크에 연결하세요(모바일 장치를 사용하는 경우 셀룰러에 연결).
    2. 웹 브라우저 주소창에 라우터 관리 패널 URL을 입력하세요(예: 192.168.8.1).
    3. 비밀번호를 입력한 다음 **Login**을 클릭하세요.
    4. 왼쪽 사이드바에서 **VPN** > **OpenVPN Client**를 클릭하세요.
![click openvpn client](https://static.gl.inet.com/docs/router/en/4/tutorials/build_your_own_openvpn_server/click-openvpn-client.png){class="glboxshadow"}
    5. **Add Manually**를 클릭하세요.
![click add manually](https://static.gl.inet.com/docs/router/en/4/tutorials/build_your_own_openvpn_server/click-add-manually.png){class="glboxshadow"}
    6. 필드에 이름을 입력한 다음 확인 아이콘을 클릭하세요.
    7. 이전에 다운로드한 설정 파일을 업로드하세요.
![select a file](https://static.gl.inet.com/docs/router/en/4/tutorials/build_your_own_openvpn_server/click-select-a-file.png){class="glboxshadow"}
    8. **Apply**를 클릭하세요.
    9. 점 3개 아이콘을 클릭한 다음 **Start**를 클릭하세요.
    10. OpenVPN 클라이언트를 실행하는 라우터에 장치를 연결하세요.

## 5. VPN 연결 확인

웹 브라우저를 열고 IP 주소와 위치를 검색하세요. VPN 서버의 IP(인터넷 서비스 제공업체의 IP가 아님)와 위치와 일치하면 VPN 연결이 성공한 것입니다.

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}을 통해 연락하세요.
