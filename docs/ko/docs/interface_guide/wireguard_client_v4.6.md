# GL.iNet 라우터에 WireGuard 클라이언트 설정 (펌웨어 v4.6 이하)

**참고**: 이 가이드는 펌웨어 v4.6 이하에 적용됩니다. 최신 버전은 [여기](wireguard_client.md)를 참조하세요.

---

WireGuard®는 최신 암호화 기술을 활용하는 매우 간단하면서도 빠르고 현대적인 VPN입니다. IPsec보다 빠르고, 간단하고, 가볍고, 유용하면서도 대규모 두통을 피하는 것을 목표로 합니다. OpenVPN보다 상당히 뛰어난 성능이 뛰어납니다.

이미 제공업체에서 WireGuard 서비스를 구매했셨지만 설정 파일을 가져오는 방법을 모르는 경우 [WireGuard 서비스 제공업체에서 설정 파일 가져오기](../tutorials/how_to_get_configuration_files_from_wireguard_service_providers.md)를 참조하거나 지원팀에 문의하세요.

[모바일 앱](../faq/mobile_app.md) 또는 웹 관리 패널을 통해 WireGuard 클라이언트를 설정할 수 있습니다.

- 모바일 앱은 AzireVPN, Mullvad, OVPN, StrongVPN, PIA VPN 등 여러 WireGuard 서비스 제공업체와 통합되어 있습니다.

- 웹 관리 패널은 더 적은 수의 WireGuard 서비스 제공업체(예: AzireVPN, Mullvad)를 지원하지만 더 직관적이고 상세한 페이지를 제공합니다.

아래는 웹 관리 패널을 통해 설정하는 단계입니다.

---

웹 관리 패널에 로그인하고 **VPN** -> **WireGuard Client**로 이동하세요.

**AzireVPN** 또는 **Mullvad** 멤버십이 있는 경우 해당 자격 증명으로 직접 로그인할 수 있습니다. 또는 **Add Manually**를 클릭하여 WireGuard 프로필을 수동으로 업로드하세요.

![wireguard client no initialized](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client_v4.6/wireguard_client_no_initialized.png){class="glboxshadow"}

## AzireVPN 설정

[AzireVPN](https://www.azirevpn.com/aff/9x7wisg4){target="_blank"}은 보안, 현대적이고 강력한 터널(예: WireGuard)을 제공하는 개인 정보 보호 중심의 VPN 서비스입니다.

![azirevpn](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client_v4.6/azirevpn.png){class="glboxshadow"}

1. **Username**과 **Password**를 입력한 다음 **Save Credentials & Get Servers**를 클릭하세요. 각 서버에 대한 설정 파일이 생성됩니다.

    ![azirevpn profiles](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client_v4.6/azirevpn_generated_profiles.png){class="glboxshadow"}

2. VPN Dashboard로 이동하여 연결을 활성화합니다.

    ![vpn dashboard azirevpn](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client_v4.6/vpn_dashboard_azirevpn.png){class="glboxshadow"}

    연결되면 사용자 IP 주소와 송수신/수신 바이트 수를 볼 수 있습니다.

    ![vpn dashboard azirevpn connected](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client_v4.6/vpn_dashboard_azirevpn_connected.png){class="glboxshadow"}

3. 서버 업데이트

    AzireVPN이 일부 서버를 유지 관리하거나 종료할 수 있으며 연결 실패를 초래할 수 있습니다. **Update Servers**를 클릭하여 최신 사용 가능한 서버를 가져오세요.

    ![azirevpn update servers](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client_v4.6/azirevpn_update_servers.png){class="glboxshadow"}

4. 자격 증명 편집

    기어 아이콘을 클릭하여 자격 증명을 편집하세요.

    ![azirevpn edit credential](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client_v4.6/azirevpn_edit_credential.png){class="glboxshadow"}

## Mullvad 설정

[Mullvad](https://mullvad.net/){target="_blank"}은 온라인 활동, 신원 및 위치를 비공개로 유지하는 데 도움이 되는 VPN 서비스입니다.

펌웨어 4.x는 Mullvad WireGuard 서비스를 통합했습니다.

![mullvad vpn](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client_v4.6/mullvad.png){class="glboxshadow"}

1. **Account**를 입력한 다음 **Save Credentials & Get Servers**를 클릭하세요.

    Mullvad 계정 번호는 "1000 0000 0000 0000"에서 "9999 9999 9999 9999" 범위의 16자리 10진수입니다.

    위치를 선택하라는 대화 상자가 나타납니다.

    ![mullvad vpn](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client_v4.6/mullvad_select_servers.png){class="glboxshadow"}

    그런 다음 선택한 위치 서버의 설정 파일이 생성됩니다.

    **Public Key**는 Mullvad 서버로 보낼 WireGuard 공개 키입니다. 동시에 최대 5개의 키를 사용할 수 있으며 [Mullvad 페이지](https://mullvad.net/en/account/#/ports){target="_blank"}에서 WireGuard 키를 관리할 수 있습니다.

    ![mullvad vpn](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client_v4.6/mullvad_generated_profiles.png){class="glboxshadow"}

2. VPN Dashboard로 이동하여 연결을 활성화합니다.

    ![mullvad vpn](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client_v4.6/vpn_dashboard_mullvadvpn.png){class="glboxshadow"}

    연결되면 사용자 IP 주소와 송수신/수신 바이트 수를 볼 수 있습니다.

    ![vpn dashboard mullvad connected](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client_v4.6/vpn_dashboard_mullvad_connected.png){class="glboxshadow"}

3. 서버 업데이트

    Mullvad가 일부 서버를 유지 관리하거나 종료할 수 있으며 연결 실패를 초래할 수 있습니다. **Update Servers**를 클릭하여 최신 사용 가능한 서버를 가져오세요.

    ![mullvad vpn](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client_v4.6/mullvad_update_servers.png){class="glboxshadow"}

4. 자격 증명 편집

    ![mullvad vpn](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client_v4.6/mullvad_edit_credential.png){class="glboxshadow"}

5. 계정 정보 삭제

    **Delete**를 클릭하면 라우터 **내의** 계정 자격 증명, 개인 키, 공개 키 및 설정 파일이 삭제됩니다.

    ![mullvad vpn](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client_v4.6/wgclient_delete_all.png){class="glboxshadow"}

6. 삭제

    클릭 한 번으로 모든 설정 파일을 삭제하고 개인 키와 공개 키도 삭제할지 묻는 메시지를 제공합니다.

    ![mullvad vpn](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client_v4.6/wgclient_delete_all_configuration_file.png){class="glboxshadow"}

## WireGuard 클라이언트 설정

펌웨어 4.0부터 그룹화를 도입하여 WireGuard 프로필을 관리합니다.

1. **Add Manually**를 클릭하세요.

    ![add manually](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client_v4.6/set_up_wireguard_client/wireguard_client_add_manually.png){class="glboxshadow"}

2. 그룹이 생성됩니다.

    ![add a new group](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client_v4.6/set_up_wireguard_client/add_a_new_group.png){class="glboxshadow"}

3. 그룹에 설명이 포함된 이름을 지정합니다(예: azirevpn). 그런 다음 설정 파일을 업로드하거나 수동으로 설정을 추가할 수 있습니다.

    ![set the new group name](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client_v4.6/set_up_wireguard_client/set_new_group_name.png){class="glboxshadow"}

    1. **설정 파일 업로드하기**

        WireGuard 설정 파일을 업로드하고 **Apply**를 클릭하세요.

        ![upload profile](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client_v4.6/set_up_wireguard_client/upload_profile.png){class="glboxshadow"}

        ![after upload profile](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client_v4.6/set_up_wireguard_client/after_upload_profile.png){class="glboxshadow"}

    2. **수동으로 설정 추가하기**, WireGuard 설정을 붙여넣거나 각� 항목을 채우려는 경우입니다.

        ![add wireguard by text](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client_v4.6/set_up_wireguard_client/manually_add_configuration.png){class="glboxshadow"}

        설명이 포함된 이름을 지정하고 설정을 붙여넣은 다음 **Apply**를 클릭하여 계속합니다.

        ![add wireguard by text](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client_v4.6/set_up_wireguard_client/add_wg_by_text.png){class="glboxshadow"}

        또는 각� 항목을 채워 설정을 추가할 수 있습니다. **Item Mode**를 클릭하세요.

        ![add wireguard by item mode](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client_v4.6/set_up_wireguard_client/add_wg_item_mode_1.png){class="glboxshadow"}

        ![add wireguard by item mode](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client_v4.6/set_up_wireguard_client/add_wg_item_mode_2.png){class="glboxshadow"}

4. 점 3개 아이콘을 클릭하여 프로필을 시작/편집/삭제합니다.

    ![start the profile](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client_v4.6/set_up_wireguard_client/start_the_profile.png){class="glboxshadow"}

5. [VPN Dashboard](vpn_dashboard_v4.7.md) 페이지로 이동하여 연결 상태를 확인하세요.

    ![vpn dashboard page](https://static.gl.inet.com/docs/router/en/4/interface_guide/wireguard_client_v4.6/set_up_wireguard_client/vpn_dashboard_wireguard_status.png){class="glboxshadow"}

---

WireGuard®는 Jason A.Donenfeld의 등록 상표입니다.

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}을 통해 연락하세요.
