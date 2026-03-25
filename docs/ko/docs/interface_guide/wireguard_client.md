# GL.iNet 라우터에 WireGuard 클라이언트 설정

**참고**: 이 가이드는 펌웨어 v4.7 이상에 적용됩니다. 이전 버전은 [여기](wireguard_client_v4.6.md)를 참조하세요.

---

WireGuard®는 최신 암호화 기술을 활용하는 매우 간단하면서도 빠르고 현대적인 VPN입니다. IPsec보다 빠르고, 간단하고, 가볍고, 유용하면서도 대규모 두통을 피하는 것을 목표로 합니다. OpenVPN보다 상당히 뛰어난 성능을 제공합니다.

GL.iNet 라우터에 WireGuard 클라이언트를 설정하려면 이 동영상을 시청하거나 아래 단계를 참조하세요.

<iframe width="560" height="315" src="https://www.youtube.com/embed/VIRcjB9k62A" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

---

시작하기 전에 WireGuard 수동 설정을 지원하는 VPN 서비스 제공업체와 활성 구독이 있는지 확인하세요. GL.iNet과 호환되는 WireGuard 제공업체를 확인하려면 [여기](https://www.gl-inet.com/solutions/vpn/){target="_blank"}를 클릭하세요.

일반적으로 먼저 구독한 VPN 서비스 제공업체의 공식 웹사이트를 방문하여 설정 파일을 가져온 다음 라우터에 업로드하여 WireGuard 클라이언트로 설정해야 합니다. 설정 파일을 가져오는 방법을 모르는 경우 [이 링크](../tutorials/how_to_get_configuration_files_from_wireguard_service_providers.md)를 참조하거나 지원팀에 문의하세요.

[모바일 앱](../faq/mobile_app.md) 또는 웹 관리 패널을 통해 WireGuard 클라이언트를 설정할 수 있습니다.

- **모바일 앱**은 AzireVPN, Mullvad VPN, OVPN, StrongVPN, PIA VPN 등 일부 WireGuard 서비스 제공업체를 통합하므로 구독한 WireGuard 서비스의 로그인 자격 증명을 입력하기만 하면 쉽게 설정할 수 있습니다. 앱을 열고 화면의 지시에 따라 설정하세요.

- **웹 관리 패널**은 일부 WireGuard 서비스 제공업체를 통합할 뿐만 아니라 수동 설정을 위한 항목도 제공합니다. 구독한 WireGuard 서비스의 자격 증명을 입력하여 빠르게 설정하거나 설정 파일을 수동으로 업로드하여 설정을 완료할 수 있습니다.

아래는 웹 관리 패널을 통해 설정하는 단계입니다. 해당 WireGuard 서비스 제공업체를 선택하여 단계별 지침을 빠르게 찾으세요.

* [AzireVPN 설정](#set-up-azirevpn)
* [Hide.me 설정](#set-up-hideme)
* [IPVanish 설정](#set-up-ipvanish)
* [Mullvad 설정](#set-up-mullvad)
* [NordVPN 설정](#set-up-nordvpn)
* [PIA (Private Internet Access) 설정](#set-up-pia-private-internet-access)
* [PureVPN 설정](#set-up-purevpn)
* [Surfshark 설정](#set-up-surfshark)
* [Windscribe 설정](#set-up-windscribe)
* [WireGuard 클라이언트 수동 설정 (기타 제공업체)](#set-up-wireguard-client-manually-for-other-providers)

## AzireVPN 설정 {#set-up-azirevpn}

[AzireVPN](https://www.azirevpn.com/aff/9x7wisg4){target="_blank"}은 보안, 현대적이고 강력한 터널(예: WireGuard)을 제공하는 개인 정보 보호 중심의 VPN 서비스입니다.

웹 관리 패널 또는 모바일 앱을 통해 GL.iNet 라우터에 AzireVPN을 설정하려면 이 동영상을 시청하세요.

<iframe width="560" height="315" src="https://www.youtube.com/embed/Ra93wlDIekA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

또는 아래 단계에 따라 웹 관리 패널을 통해 AzireVPN을 설정하세요.

웹 관리 패널에서 **VPN** -> **WireGuard Client** -> **AzireVPN**으로 이동합니다.

1. **Username**과 **Password**를 입력한 다음 **Save and Continue**를 클릭하세요. 각 서버에 대한 설정 파일이 생성됩니다.

    ![azirevpn login](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_azirevpn/azirevpn1.png){class="glboxshadow"}

2. 연결 시작합니다.

    원하는 서버를 선택하고 오른쪽의 점 3개 아이콘을 클릭하여 연결을 시작합니다.

    ![azirevpn start](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_azirevpn/azirevpn2.png){class="glboxshadow"}

    연결되면 설정 파일 옆에 녹색 점이 나타납니다.

    ![azirevpn connected](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_azirevpn/azirevpn3.png){class="glboxshadow"}

    그리고 **VPN Dashboard**에 VPN 연결 세부 정보가 표시됩니다.

    ![azirevpn connection status](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_azirevpn/azirevpn4.png){class="glboxshadow"}

3. 서버 업데이트합니다.

    **Update Servers**를 클릭하여 최신 사용 가능한 서버 목록을 가져와 서버 유지 관리 또는 종료로 인한 연결 실패를 방지하세요.

    ![azirevpn update servers](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_azirevpn/azirevpn5.png){class="glboxshadow"}

4. 자격 증명 편집 또는 로그아웃합니다.

    기어 아이콘을 클릭하여 로그인 자격 증명을 편집하거나 로그아웃하세요.

    ![azirevpn edit credentials or logout](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_azirevpn/azirevpn6.png){class="glboxshadow"}

5. 구독 갱신합니다.

    **Go Renew**를 클릭하면 구독을 갱신하기 위해 공식 웹사이트로 리디렉션됩니다.

    ![azirevpn go renew](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_azirevpn/azirevpn7.png){class="glboxshadow"}

6. 모두 삭제합니다.

    **Delete All**을 클릭하여 클릭 한 번으로 모든 설정 파일을 삭제하고 개인 키와 공개 키를 동시에 삭제할지 선택할 수 있습니다.

    ![azirevpn delete](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_azirevpn/azirevpn8.png){class="glboxshadow"}

## Hide.me 설정 {#set-up-hideme}

[공식 웹사이트](https://www.hideipvpn.com/){target="_blank"}

웹 관리 패널에서 **VPN** -> **WireGuard Client** -> **Hide.me**로 이동합니다.

1. **Username**과 **Password**를 입력한 다음 **Save and Continue**를 클릭하세요. 각 서버에 대한 설정 파일이 생성됩니다.

    ![hideme login](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_hidemevpn/hideme1.png){class="glboxshadow"}

2. 연결 시작합니다.

    원하는 서버를 선택하고 오른쪽의 점 3개 아이콘을 클릭하여 연결을 시작합니다.

    ![hideme start](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_hidemevpn/hideme2.png){class="glboxshadow"}

    연결되면 설정 파일 옆에 녹색 점이 나타납니다.

    ![hideme connected](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_hidemevpn/hideme3.png){class="glboxshadow"}

    그리고 **VPN Dashboard**에 VPN 연결 세부 정보가 표시됩니다.

    ![hideme connection status](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_hidemevpn/hideme4.png){class="glboxshadow"}

3. 서버 업데이트합니다.

    **Update Servers**를 클릭하여 최신 사용 가능한 서버 목록을 가져와 서버 유지 관리 또는 종료로 인한 연결 실패를 방지하세요.

    ![hideme update servers](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_hidemevpn/hideme5.png){class="glboxshadow"}

4. 자격 증명 편집 또는 로그아웃합니다.

    기어 아이콘을 클릭하여 로그인 자격 증명을 편집하거나 로그아웃하세요.

    ![hideme edit credentials or logout](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_hidemevpn/hideme6.png){class="glboxshadow"}

5. 모두 삭제합니다.

    **Delete All**을 클릭하여 클릭 한 번으로 모든 설정 파일을 삭제하고 개인 키와 공개 키를 동시에 삭제할지 선택할 수 있습니다.

    ![hide.me delete](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_hidemevpn/hideme7.png){class="glboxshadow"}

## IPVanish 설정 {#set-up-ipvanish}

[공식 웹사이트](https://affiliate.ipvanish.com/aff_c?offer_id=1&aff_id=3073){target="_blank"}

웹 관리 패널에서 **VPN** -> **WireGuard Client** -> **IPVanish**로 이동합니다.

1. **Username**과 **Password**를 입력한 다음 **Save and Continue**를 클릭하세요. 각 서버에 대한 설정 파일이 생성됩니다.

    ![ipvanish login](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_ipvanish/ipvanish1.png){class="glboxshadow"}

2. 서버를 선택합니다.

    연결하려는 서버를 선택하고 **Apply**를 클릭하세요.

    ![ipvanish select servers](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_ipvanish/ipvanish2.png){class="glboxshadow"}

3. 연결 시작합니다.

    원하는 서버를 선택하고 오른쪽의 점 3개 아이콘을 클릭하여 연결을 시작합니다.

    ![ipvanish start](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_ipvanish/ipvanish3.png){class="glboxshadow"}

    연결되면 설정 파일 옆에 녹색 점이 나타납니다.

    ![ipvanish connected](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_ipvanish/ipvanish4.png){class="glboxshadow"}

    그리고 **VPN Dashboard**에 VPN 연결 세부 정보가 표시됩니다.

    ![ipvanish connection status](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_ipvanish/ipvanish5.png){class="glboxshadow"}

4. 서버 업데이트합니다.

    **Update Servers**를 클릭하여 최신 사용 가능한 서버 목록을 가져와 서버 유지 관리 또는 종료로 인한 연결 실패를 방지하세요.

    ![ipvanish update servers](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_ipvanish/ipvanish6.png){class="glboxshadow"}

5. 자격 증명 편집 또는 로그아웃합니다.

    기어 아이콘을 클릭하여 로그인 자격 증명을 편집하거나 로그아웃하세요.

    ![ipvanish edit credentials or logout](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_ipvanish/ipvanish7.png){class="glboxshadow"}

6. 모두 삭제합니다.

    **Delete All**을 클릭하여 클릭 한 번으로 모든 설정 파일을 삭제하고 개인 키와 공개 키를 동시에 삭제할지 선택할 수 있습니다.

    ![ipvanish delete](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_ipvanish/ipvanish8.png){class="glboxshadow"}

## Mullvad 설정 {#set-up-mullvad}

[Mullvad](https://mullvad.net/){target="_blank"}은 온라인 활동, 신원 및 위치를 비공개로 유지하는 데 도움이 되는 VPN 서비스입니다.

웹 관리 패널에서 **VPN** -> **WireGuard Client** -> **Mullvad**로 이동합니다.

1. **Account**를 입력한 다음 **Save and Continue**를 클릭하세요. 각 서버에 대한 설정 파일이 생성됩니다.

    ![mullvad login](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_mullvad/mullvad1.png){class="glboxshadow"}

2. 서버를 선택합니다.

    연결하려는 서버를 선택하고 **Apply**를 클릭하세요.

    ![mullvad select server](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_mullvad/mullvad2.png){class="glboxshadow"}

3. 연결 시작합니다.

    원하는 서버를 선택하고 오른쪽의 점 3개 아이콘을 클릭하여 연결을 시작합니다.

    ![mullvad start](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_mullvad/mullvad3.png){class="glboxshadow"}

    연결되면 설정 파일 옆에 녹색 점이 나타납니다.

    ![mullvad connected](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_mullvad/mullvad4.png){class="glboxshadow"}

    그리고 **VPN Dashboard**에 VPN 연결 세부 정보가 표시됩니다.

    ![mullvad connection status](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_mullvad/mullvad5.png){class="glboxshadow"}

4. 서버 업데이트합니다.

    **Update Servers**를 클릭하여 최신 사용 가능한 서버 목록을 가져와 서버 유지 관리 또는 종료로 인한 연결 실패를 방지하세요.

    ![mullvad update servers](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_mullvad/mullvad6.png){class="glboxshadow"}

5. 자격 증명 편집 또는 로그아웃합니다.

    기어 아이콘을 클릭하여 로그인 자격 증명을 편집하거나 로그아웃하세요.

    ![mullvad edit credentials or logout](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_mullvad/mullvad7.png){class="glboxshadow"}

6. 구독 갱신합니다.

    **Go Renew**를 클릭하면 구독을 갱신하기 위해 공식 웹사이트로 리디렉션됩니다.

    ![mullvad go renew](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_mullvad/mullvad8.png){class="glboxshadow"}

7. 모두 삭제합니다.

    **Delete All**을 클릭하여 클릭 한 번으로 모든 설정 파일을 삭제하고 개인 키와 공개 키를 동시에 삭제할지 선택할 수 있습니다.

    ![mullvad delete](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_mullvad/mullvad9.png){class="glboxshadow"}

## NordVPN 설정 {#set-up-nordvpn}

[NordVPN](https://go.nordvpn.net/aff_c?offer_id=15&amp;aff_id=12016&amp;url_id=902){target="_blank"}은 속도와 보안을 결합한 온라인 VPN 서비스입니다.

1. [여기](https://my.nordaccount.com/){target="_blank"}를 클릭하여 NordVPN 웹 계정으로 로그인하세요.

    ![nordvpn](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_nordvpn/nordvpn_login.png){class="glboxshadow"}

    Nord 대시보드에 로그인한 후 왼쪽에서 NordVPN을 클릭한 다음 **Set up NordVPN manually**를 클릭하세요.

    ![nordvpn](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_nordvpn/nordvpn_dashboard.png){class="glboxshadow"}

    그러면 **Access token**을 찾을 수 있습니다.

    ![nordvpn get credentials](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_nordvpn/manual_setup.png){class="glboxshadow"}

    ![nordvpn get credentials](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_nordvpn/generate_new_token.png){class="glboxshadow"}

    ![nordvpn get credentials](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_nordvpn/copy_access_token.png){class="glboxshadow"}

2. 라우터의 웹 관리 패널에 로그인하고 **VPN** -> **WireGuard Client** -> **NordVPN**으로 이동합니다.

    **Token**을 입력한 다음 **Save and Continue**를 클릭하세요. 각 서버에 대한 설정 파일이 생성됩니다.

    ![nordvpn login](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_nordvpn/nordvpn1.png){class="glboxshadow"}

3. 서버를 선택합니다.

    연결하려는 서버를 선택하고 **Apply**를 클릭하세요.

    ![nordvpn select servers](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_nordvpn/nordvpn2.png){class="glboxshadow"}

4. 연결 시작합니다.

    원하는 서버를 선택하고 오른쪽의 점 3개 아이콘을 클릭하여 연결을 시작합니다.

    ![nordvpn start](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_nordvpn/nordvpn3.png){class="glboxshadow"}

    연결되면 설정 파일 옆에 녹색 점이 나타납니다.

    ![nordvpn connected](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_nordvpn/nordvpn4.png){class="glboxshadow"}

    그리고 **VPN Dashboard**에 VPN 연결 세부 정보가 표시됩니다.

    ![nordvpn connection status](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_nordvpn/nordvpn5.png){class="glboxshadow"}

5. 서버 업데이트합니다.

    **Update Servers**를 클릭하여 최신 사용 가능한 서버 목록을 가져와 서버 유지 관리 또는 종료로 인한 연결 실패를 방지하세요.

    ![nordvpn update servers](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_nordvpn/nordvpn6.png){class="glboxshadow"}

6. 자격 증명 편집 또는 로그아웃합니다.

    기어 아이콘을 클릭하여 로그인 자격 증명을 편집하거나 로그아웃하세요.

    ![nordvpn edit credentials or logout](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_nordvpn/nordvpn7.png){class="glboxshadow"}

7. 모두 삭제합니다.

    **Delete All**을 클릭하여 클릭 한 번으로 모든 설정 파일을 삭제하고 개인 키와 공개 키를 동시에 삭제할지 선택할 수 있습니다.

    ![nordvpn delete](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_nordvpn/nordvpn8.png){class="glboxshadow"}

## PIA (Private Internet Access) 설정 {#set-up-pia-private-internet-access}

[공식 웹사이트](https://privateinternetaccess.com/offer/GLiNET_71dx4t8bl){target="_blank"}

웹 관리 패널에서 **VPN** -> **WireGuard Client** -> **PIA**로 이동합니다.

1. **Username**과 **Password**를 입력한 다음 **Save and Continue**를 클릭하세요. 각 서버에 대한 설정 파일이 생성됩니다.

    ![pia login](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_pia/pia1.png){class="glboxshadow"}

2. 서버를 선택합니다.

    연결하려는 서버를 선택하고 **Apply**를 클릭하세요.

    ![pia select servers](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_pia/pia2.png){class="glboxshadow"}

3. 연결 시작합니다.

    원하는 서버를 선택하고 오른쪽의 점 3개 아이콘을 클릭하여 연결을 시작합니다.

    ![pia start](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_pia/pia3.png){class="glboxshadow"}

    연결되면 설정 파일 옆에 녹색 점이 나타납니다.

    ![pia connected](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_pia/pia4.png){class="glboxshadow"}

    그리고 **VPN Dashboard**에 VPN 연결 세부 정보가 표시됩니다.

    ![pia connection status](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_pia/pia5.png){class="glboxshadow"}

4. 서버 업데이트합니다.

    **Update Servers**를 클릭하여 최신 사용 가능한 서버 목록을 가져와 서버 유지 관리 또는 종료로 인한 연결 실패를 방지하세요.

    ![pia update servers](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_pia/pia6.png){class="glboxshadow"}

5. 자격 증명 편집 또는 로그아웃합니다.

    기어 아이콘을 클릭하여 로그인 자격 증명을 편집하거나 로그아웃하세요.

    ![pia edit credential or logout](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_pia/pia7.png){class="glboxshadow"}

6. 모두 삭제합니다.

    **Delete All**을 클릭하여 클릭 한 번으로 모든 설정 파일을 삭제하고 개인 키와 공개 키를 동시에 삭제할지 선택할 수 있습니다.

    ![pia delete](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_pia/pia8.png){class="glboxshadow"}

## PureVPN 설정 {#set-up-purevpn}

[공식 웹사이트](https://billing.purevpn.com/aff.php?aff=35535){target="_blank"}

웹 관리 패널에서 **VPN** -> **WireGuard Client** -> **PureVPN**으로 이동합니다.

1. **Username**과 **Password**를 입력한 다음 **Save and Continue**를 클릭하세요.

    ![purevpn login](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_purevpn/purevpn1.png){class="glboxshadow"}

    사용 가능한 모든 설정 파일이 생성됩니다.

    ![purevpn config files](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_purevpn/purevpn2.png){class="glboxshadow"}

2. 연결 시작합니다.

    원하는 서버를 선택하고 오른쪽의 점 3개 아이콘을 클릭하여 연결을 시작합니다.

    ![purevpn start](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_purevpn/purevpn3.png){class="glboxshadow"}

    연결되면 설정 파일 옆에 녹색 점이 나타납니다.

    ![purevpn connected](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_purevpn/purevpn4.png){class="glboxshadow"}

    그리고 **VPN Dashboard**에 VPN 연결 세부 정보가 표시됩니다.

    ![purevpn connection status](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_purevpn/purevpn5.png){class="glboxshadow"}

4. 서버 업데이트합니다.

    **Update Servers**를 클릭하여 최신 사용 가능한 서버 목록을 가져와 서버 유지 관리 또는 종료로 인한 연결 실패를 방지하세요.

    ![purevpn update servers](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_purevpn/purevpn6.png){class="glboxshadow"}

5. 자격 증명 편집 또는 로그아웃합니다.

    기어 아이콘을 클릭하여 로그인 자격 증명을 편집하거나 로그아웃하세요.

    ![purevpn edit credential or logout](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_purevpn/purevpn7.png){class="glboxshadow"}

6. 모두 삭제합니다.

    **Delete All**을 클릭하여 클릭 한 번으로 모든 설정 파일을 삭제하고 개인 키와 공개 키를 동시에 삭제할지 선택할 수 있습니다.

    ![purevpn delete](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_purevpn/purevpn8.png){class="glboxshadow"}

## Surfshark 설정 {#set-up-surfshark}

[공식 웹사이트](https://get.surfshark.net/aff_c?offer_id=926&aff_id=1400){target="_blank"}

웹 관리 패널에서 **VPN** -> **WireGuard Client** -> **Surfshark**로 이동합니다.

1. **Username**과 **Password**를 입력한 다음 **Save and Continue**를 클릭하세요. 각 서버에 대한 설정 파일이 생성됩니다.

    ![surfshark login](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_surfshark/surfshark1.png){class="glboxshadow"}

2. 서버를 선택합니다.

    연결하려는 서버를 선택하고 **Apply**를 클릭하세요.

    ![surfshark select servers](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_surfshark/surfshark2.png){class="glboxshadow"}

3. 연결 시작합니다.

    원하는 서버를 선택하고 오른쪽의 점 3개 아이콘을 클릭하여 연결을 시작합니다.

    ![surfshark start](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_surfshark/surfshark3.png){class="glboxshadow"}

    연결되면 설정 파일 옆에 녹색 점이 나타납니다.

    ![surfshark connected](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_surfshark/surfshark4.png){class="glboxshadow"}

    그리고 **VPN Dashboard**에 VPN 연결 세부 정보가 표시됩니다.

    ![surfshark connection status](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_surfshark/surfshark5.png){class="glboxshadow"}

4. 서버 업데이트합니다.

    **Update Servers**를 클릭하여 최신 사용 가능한 서버 목록을 가져와 서버 유지 관리 또는 종료로 인한 연결 실패를 방지하세요.

    ![surfshark update servers](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_surfshark/surfshark6.png){class="glboxshadow"}

5. 자격 증명 편집 또는 로그아웃합니다.

    기어 아이콘을 클릭하여 로그인 자격 증명을 편집하거나 로그아웃하세요.

    ![surfshark edit credential or logout](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_surfshark/surfshark7.png){class="glboxshadow"}

6. 새로고침합니다.

    VPN 서버에 연결할 수 없을 때 **Refresh**를 클릭하여 공개 키를 업데이트할 수 있습니다.

    ![surfshark refresh](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_surfshark/surfshark8.png){class="glboxshadow"}

7. 모두 삭제합니다.

    **Delete All**을 클릭하여 클릭 한 번으로 모든 설정 파일을 삭제하고 개인 키와 공개 키를 동시에 삭제할지 선택할 수 있습니다.

    ![surfshark delete](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_surfshark/surfshark9.png){class="glboxshadow"}

## Windscribe 설정 {#set-up-windscribe}

[공식 웹사이트](https://windscribe.com/yo/1u2h9ndl){target="_blank"}

웹 관리 패널에서 **VPN** -> **WireGuard Client** -> **Windscribe**로 이동합니다.

1. **Username**과 **Password**를 입력한 다음 **Save and Continue**를 클릭하세요. 각 서버에 대한 설정 파일이 생성됩니다.

    ![windscribe login](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_windscribe/windscribe1.png){class="glboxshadow"}

2. 서버를 선택합니다.

    연결하려는 서버를 선택하고 **Apply**를 클릭하세요.

    ![windscribe select servers](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_windscribe/windscribe2.png){class="glboxshadow"}

    그러면 선택한 서버에 해당하는 설정 파일 목록을 얻게 됩니다.

    ![windscribe config files](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_windscribe/windscribe3.png){class="glboxshadow"}

3. 연결 시작합니다.

    원하는 서버를 선택하고 오른쪽의 점 3개 아이콘을 클릭하여 연결을 시작합니다.

    ![windscribe start](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_windscribe/windscribe4.png){class="glboxshadow"}

    연결되면 설정 파일 옆에 녹색 점이 나타납니다.

    ![windscribe connected](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_windscribe/windscribe5.png){class="glboxshadow"}

    그리고 **VPN Dashboard**에 VPN 연결 세부 정보가 표시됩니다.

    ![windscribe connection status](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_windscribe/windscribe6.png){class="glboxshadow"}

4. 서버 업데이트합니다.

    **Update Servers**를 클릭하여 최신 사용 가능한 서버 목록을 가져와 서버 유지 관리 또는 종료로 인한 연결 실패를 방지하세요.

    ![windscribe update servers](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_windscribe/windscribe7.png){class="glboxshadow"}

5. 자격 증명 편집 또는 로그아웃합니다.

    기어 아이콘을 클릭하여 로그인 자격 증명을 편집하거나 로그아웃하세요.

    ![windscribe edit credential or logout](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_windscribe/windscribe8.png){class="glboxshadow"}

6. 새로고침합니다.

    VPN 서버에 연결할 수 없을 때 **Refresh**를 클릭하여 공개 키를 업데이트할 수 있습니다.

    ![windscribe refresh](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_windscribe/windscribe9.png){class="glboxshadow"}

7. 모두 삭제합니다.

    **Delete All**을 클릭하여 클릭 한 번으로 모든 설정 파일을 삭제하고 개인 키와 공개 키를 동시에 삭제할지 선택할 수 있습니다.

    ![windscribe delete](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_windscribe/windscribe10.png){class="glboxshadow"}

## WireGuard 클라이언트 수동 설정 (기타 제공업체) {#set-up-wireguard-client-manually-for-other-providers}

다른 WireGuard 서비스 제공업체를 사용하는 경우 WireGuard 설정 파일을 다운로드하고 아래 단계에 따라 WireGuard 클라이언트를 설정할 수 있습니다. 설정 파일을 다운로드하는 방법을 모르는 경우 [이 가이드](../tutorials/how_to_get_configuration_files_from_wireguard_service_providers.md)를 참조하거나 지원팀에 문의하세요.

웹 관리 패널에서 **VPN** -> **WireGuard Client**로 이동합니다.

1. **Add Manually**를 클릭하세요.

    ![add manually](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_wireguard_client/add_manually.png){class="glboxshadow"}

2. 왼쪽 사이드바에 그룹이 생성됩니다.

    ![add a new group](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_wireguard_client/create_a_group.png){class="glboxshadow"}

3. 그룹의 설명이 포함된 이름을 설정합니다(예: azirevpn). 그런 다음 설정 파일을 업로드하거나(지원 형식: zip, tar, gz, conf, txt) 수동으로 설정 세부 정보를 추가합니다(텍스트 형식).

    ![set the new group name](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_wireguard_client/set_a_name.png){class="glboxshadow"}

    1. **설정 파일 업로드하기**.

        업로드 영역을 클릭하여 WireGuard 설정 파일을 업로드한 다음 **Apply**를 클릭하세요.

        ![upload profile](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_wireguard_client/upload_configuration_file.png){class="glboxshadow"}

        ![after upload profile](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_wireguard_client/upload_configuration_file_apply.png){class="glboxshadow"}

    2. **수동으로 설정 추가하기**.

        업로드 영역 하단의 **Manually Add Configuration**를 클릭하세요.

        ![add wireguard by text](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_wireguard_client/manually_add_configuration.png){class="glboxshadow"}

        설명이 포함된 이름을 설정하고 설정을 텍스트 상자에 붙여넣습니다. 그런 다음 **Apply**를 클릭하세요.

        ![add wireguard by text](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_wireguard_client/text_mode.png){class="glboxshadow"}
        <small>(텍스트 모드)</small>

        각 항목을 확인하려면 항목 모드로 전환하여 설정 세부 정보를 확인할 수 있습니다. 그런 다음 **Apply**를 클릭하세요.

        ![add wireguard by item mode](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_wireguard_client/item_mode.png){class="glboxshadow"}
        <small>(항목 모드)</small>

4. 오른쪽의 점 3개 아이콘을 클릭하여 연결을 시작합니다.

    ![start the profile](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_wireguard_client/start_edit_delete.png){class="glboxshadow"}

5. 연결되면 **VPN Dashboard** 페이지에서 연결 상태를 확인할 수 있습니다.

    ![vpn dashboard page](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_wireguard_client/vpn_dashboard_wireguard_status.png){class="glboxshadow"}

## GL.iNet 라우터에 WireGuard 서버 설정

제3자 VPN 서비스를 구독하지 않으시나요? GL.iNet 라우터 2대를 구매하여 한 대는 WireGuard 서버로, 다른 한 대는 WireGuard 클라이언트로 설정할 수 있습니다.

이는 특히 집 네트워크의 ISP가 공용 IP를 제공하고 집에서 멀리 떨어져 있을 때 VPN을 통해 집 네트워크에 연결하여 보안과 내부 네트워크 리소스에 액세스하려는 시나리오에 적합합니다. 이렇게 하면 상용 VPN 서비스를 지속적으로 구독해야 하는 비용과 번거로움이 eliminated됩니다.

WireGuard 서버 설정은 [여기](wireguard_server.md)를 확인하세요.

---

WireGuard®는 Jason A.Donenfeld의 등록 상표입니다.

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}을 통해 연락하세요.
