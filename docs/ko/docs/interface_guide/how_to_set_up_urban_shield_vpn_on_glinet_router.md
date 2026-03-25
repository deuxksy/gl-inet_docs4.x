# GL.iNet 라우터에서 Urban Shield VPN 설정

[Urban Shield VPN](https://urbanshieldvpn.com/)은 전 세계 사용자에게 높은 보안과 성능을 제공하는 VPN 솔루션을 전문으로 제공하는 VPN 제공업체입니다. 사전 구성된 GL.iNet VPN 라우터와 유연한 구독 플랜을 제공하여 안전하고 개인적인 브라우징을 보장합니다. 라우터에서 Urban Shield VPN을 활성화하기만 하면 글로벌 서버에 액세스할 수 있으며 마음 편하게 브라우징하고 스트리밍할 수 있습니다.

## 설정 가이드

GL-B3000을 예로 들어 WireGuard 클라이언트로 설정하여 Urban Shield VPN을 활성화하는 방법을 설명합니다.

### 1. Urban Shield VPN 가입

[Urban Shield VPN 공식 웹사이트](https://urbanshieldvpn.com/){class="_blank"}를 방문하거나 [여기](https://payment.urbanshieldvpn.com/sign-up)를 클릭하여 Urban Shield VPN 계정에 가입하세요.

![Urban Shield VPN signup](https://static.gl.inet.com/docs/router/en/4/interface_guide/setup_urban_shield_vpn/sign_in.png){class="glboxshadow"}

### 2. 전원 켜기 및 연결

라우터의 전원을 켭니다. 이더넷 케이블 또는 Wi-Fi를 통해 기기를 라우터에 연결합니다.

### 3. 웹 관리 패널 액세스

아래 단계에 따라 웹 관리 패널에 액세스하세요. 이미 로그인한 경우 [다음 부분](#4-network-setup)으로 이동하세요.

웹 브라우저(Chrome, Edge 또는 Safari 권장)를 열고 [192.168.8.1](http://192.168.8.1){target="_blank"}을 방문하세요. 아래와 같이 웹 관리 패널의 초기 설정으로 이동합니다. 관리자 비밀번호를 설정하고 **Next**를 클릭하여 계속합니다.

![set up admin password](https://static.gl.inet.com/docs/router/en/4/interface_guide/setup_urban_shield_vpn/web_panel_signup.png){class="glboxshadow"}

Wi-Fi 네트워크를 설정합니다. 이 페이지는 Wi-Fi 이름(SSID)과 비밀번호를 포함한 공장 Wi-Fi 세부 정보를 표시하며 변경하거나 그대로 유지할 수 있습니다. Wi-Fi 세부 정보를 변경한 경우 기기를 업데이트된 Wi-Fi에 다시 연결하세요.

![set up wifi](https://static.gl.inet.com/docs/router/en/4/interface_guide/setup_urban_shield_vpn/set_up_wifi.png){class="glboxshadow"}

그런 다음 **Next**를 클릭하고 관리자 비밀번호로 로그인하세요.

### 4. 네트워크 설정

오른쪽 상단에 **네트워크 설정 마법사**가 있습니다(펌웨어 v4.7 이상에서 사용 가능). VPN을 설정하기 전에 마법사를 따라 인터넷 액세스를 위해 라우터를 구성하세요.

![network setup](https://static.gl.inet.com/docs/router/en/4/interface_guide/setup_urban_shield_vpn/network_setup_wizard.jpg){class="glboxshadow"}

### 5. Urban Shield VPN 활성화

왼쪽 메뉴에서 **VPN** -> **WireGuard Client**를 선택합니다. 내장형 Urban Shield VPN 로그인 페이지가 표시됩니다.

![log in 1](https://static.gl.inet.com/docs/router/en/4/interface_guide/setup_urban_shield_vpn/urban_shield_login_1.png){class="glboxshadow"}

**Email**과 **Password**를 입력한 다음 **Save And Continue**를 클릭합니다. 각 서버에 대한 구성 파일이 생성됩니다.

![log in 2](https://static.gl.inet.com/docs/router/en/4/interface_guide/setup_urban_shield_vpn/urban_shield_login_2.png){class="glboxshadow"}

선호하는 서버를 선택하고 **Apply**를 클릭하세요.

![select server](https://static.gl.inet.com/docs/router/en/4/interface_guide/setup_urban_shield_vpn/select_server.png){class="glboxshadow"}

사용 가능한 서버가 목록에 표시됩니다.

![get server](https://static.gl.inet.com/docs/router/en/4/interface_guide/setup_urban_shield_vpn/get_servers.png){class="glboxshadow"}

세 점 아이콘을 클릭하여 연결을 시작합니다.

![start server](https://static.gl.inet.com/docs/router/en/4/interface_guide/setup_urban_shield_vpn/start_server.jpg){class="glboxshadow"}

연결되면 연결 성공을 나타내는 파란 점이 나타납니다.

![server started](https://static.gl.inet.com/docs/router/en/4/interface_guide/setup_urban_shield_vpn/server_started.jpg){class="glboxshadow"}

VPN 대시보드에서 연결 상태를 확인할 수도 있습니다.

![vpn dashboard](https://static.gl.inet.com/docs/router/en/4/interface_guide/setup_urban_shield_vpn/vpn_dashboard.png){class="glboxshadow"}

## 계정 정보 편집 또는 로그아웃

기어 아이콘을 클릭하여 계정 정보를 편집하거나 로그아웃하세요.

![edit account or logout 1](https://static.gl.inet.com/docs/router/en/4/interface_guide/setup_urban_shield_vpn/edit_account_or_logout_1.jpg){class="glboxshadow"}

![edit account or logout 2](https://static.gl.inet.com/docs/router/en/4/interface_guide/setup_urban_shield_vpn/edit_account_or_logout_2.jpg){class="glboxshadow"}

## 구독 갱신

**Go Renew**를 클릭하면 구독을 갱신하기 위해 공식 웹사이트로 이동합니다.

![go renew](https://static.gl.inet.com/docs/router/en/4/interface_guide/setup_urban_shield_vpn/go_renew.jpg){class="glboxshadow"}

## 삭제

클릭 한 번으로 모든 구성 파일과 개인 키 및 공개 키를 삭제할 수 있습니다.

![delete](https://static.gl.inet.com/docs/router/en/4/interface_guide/setup_urban_shield_vpn/delete_all.jpg){class="glboxshadow"}

---
