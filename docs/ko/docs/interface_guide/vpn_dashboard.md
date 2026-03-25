# VPN Dashboard

**참고**: 이 가이드는 펌웨어 v4.8을 기준으로 합니다. 이전 버전은 [여기](vpn_dashboard_v4.7.md)를 참조하세요.

---

웹 관리 패널 왼쪽에서 **VPN** -> **VPN Dashboard**로 이동합니다.

VPN 대시보드는 터널 규칙, 서버 주소, 트래픽 통계, 클라이언트 가상 IP, 연결 로그와 같은 VPN 연결 세부 정보를 표시하고 VPN Kill Switch, IP Masquerading, MTU와 같은 고급 설정을 구성할 수 있습니다.

또한 다중 터널 시나리오를 위해 여러 VPN 연결을 활성화할 수 있습니다.

## 설정 마법사

좌측 상단의 책 아이콘을 클릭하고 VPN 설정 마법사를 따라 VPN 구성을 빠르게 완료하세요.

![vpn wizard 1](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/vpn_wizard_1.png){class="glboxshadow"}

![vpn wizard 2](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/vpn_wizard_2.png){class="glboxshadow"}

**참고**: VPN 설정 마법사는 통합 VPN 서비스(AzireVPN, Hide.me, IPVanish, Mullvad, NordVPN, PIA, Surfshark)만 사용할 수 있습니다. 다른 VPN 서비스의 경우 마법사를 건너뛰고 [OpenVPN Client](openvpn_client.md){target="_blank"} 또는 [WireGuard Client](wireguard_client.md){target="_blank"}로 이동하여 수동으로 VPN을 설정하세요.

다음은 **Hide.me**를 사용한 예입니다. Hide.me 자격 증명으로 로그인합니다.

![vpn login](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/vpn_login.png){class="glboxshadow"}

VPN 서버를 선택하고 **Apply**를 클릭하세요. 이것이 이 VPN 터널을 통해 연결할 서버이며 공용 IP 주소가 선택한 서버의 위치에서 온 것으로 표시됩니다.

![select server](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/select_server.png){class="glboxshadow"}

자동으로 연결됩니다. 성공적으로 연결되면 VPN Dashboard로 이동하면 VPN 터널이 활성화된 것을 볼 수 있습니다.

![vpn connected](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/connected.png){class="glboxshadow"}

현재 사용 중인 VPN 프로토콜(예: WireGuard), 구성 파일, 서버 주소, 서버 수신 포트, 트래픽 통계, 클라이언트 가상 IP를 표시합니다. 사용자는 우측 하단에서 연결 로그를 볼 수 있습니다.

연결된 모든 클라이언트는 이 VPN 터널을 통해 인터넷에 액세스합니다.

VPN 정책을 구성하려면 [Policy Mode](#policy-mode)를 참조하세요.

## VPN 모드

VPN Dashboard에서 우측 상단의 버튼을 클릭하여 VPN 모드를 전환합니다.

![vpn mode](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/vpn_mode.png){class="glboxshadow"}

두 가지 모드를 사용할 수 있습니다: **Global Mode**와 **Policy Mode**.

![vpn mode](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/global_mode.png){class="glboxshadow"}

### Global Mode

이 모드에서는 모든 트래픽이 VPN 터널을 통해 라우팅되며 하나의 VPN 클라이언트 인스턴스만 활성화할 수 있습니다.

모든 클라이언트 트래픽이 단일 VPN 서버를 통해 라우팅되는 시나리오(예: 통합 네트워크 보안 또는 지역별 콘텐츠 액세스)에 이상적입니다.

다음 예에서는 라우터가 WireGuard 프로토콜을 사용하여 호주 서버에 연결합니다. 연결된 모든 클라이언트의 트래픽이 이 VPN 터널을 통해 라우팅됩니다.

![connected global mode](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/connected-global-mode.png){class="glboxshadow"}

### Policy Mode

이 모드에서는 라우터가 여러 VPN 서버에 연결할 수 있으며 다양한 클라이언트나 트래픽 대상에 대한 라우팅 규칙을 사용자 정의할 수 있습니다.

유연한 트래픽 관리가 필요한 사용 사례(예: 여러 VPN 서버를 통해 다양한 트래픽을 다른 대상으로 라우팅)에 적합합니다.

VPN Mode를 Policy Mode로 전환하고 **Apply**를 클릭하세요.

![policy mode](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/policy_mode.png){class="glboxshadow"}

전환 후 VPN이 활성화되지 않은 경우 페이지는 아래와 같이 표시되며 세 개 섹션(Pimary Tunnel, Add Tunnel, All Other Traffic)이 포함됩니다.

![policy mode no vpn](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/policy_no_vpn_file.png){class="glboxshadow"}

해당 섹션을 클릭하여 자세한 내용을 확인하세요.

- [Primary Tunnel](#primary-tunnel)
- [Add Tunnel](#add-tunnel)
- [All Other Traffic](#all-other-traffic)

#### Primary Tunnel

기본 터널은 Policy Mode의 <u>사전 설정</u> 터널입니다. 최우선 순위를 가지며 터널이 두 개 이상인 경우 [터널 우선 순위](#tunnel-priority)를 수정할 수 있습니다.

이 터널에서는 세 가지 요소를 설정하여 터널 규칙을 사용자 정의할 수 있습니다.

1. **From**: 트래픽 소스를 나타내며, 이 터널을 통해 라우팅해야 하는 트래픽입니다.

    회색 상자를 클릭하여 트래픽 소스를 선택하세요.

    ![traffic source](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/traffic_from_1.png){class="glboxshadow"}

    ![traffic source](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/traffic_from_2.jpg){class="glboxshadow"}

    - **All Clients**: 선택하면 모든 장치의 트래픽이 이 규칙과 일치합니다.

        ![all clients](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/all_clients.jpg){class="glboxshadow"}

    - **Specified Connection Types**: 선택하면 지정된 연결 유형(예: LAN 서브넷, Drop-in Gateway, 게스트 네트워크)의 트래픽이 이 규칙과 일치합니다.

        ![specified connection](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/specified_connection_types_1.jpg){class="glboxshadow"}

        이 라우터에서 OpenVPN 서버 또는 WireGuard 서버를 활성화한 경우 Specified Connection Types 아래에 더 많은 옵션이 표시됩니다. 이는 [VPN Cascading](../tutorials/how_to_use_vpn_cascading_on_glinet_routers.md)에 유용합니다.

        ![specified connection](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/specified_connection_types_2.png){class="glboxshadow"}

    - **Specified Devices**: 선택하면 지정된 장치(MAC 주소로 식별)의 트래픽이 이 규칙과 일치합니다.

        ![specified devices](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/specified_devices.jpg){class="glboxshadow"}

    - **Exclude Specified Devices**: 선택하면 지정된 장치(MAC 주소로 식별)의 트래픽이 이 규칙과 일치하지 **않습니다**.

        ![exclude devices](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/exclude_devices.jpg){class="glboxshadow"}

2. **To**: 트래픽 대상을 나타냅니다.

    회색 상자를 클릭하여 트래픽 대상을 선택하세요.

    ![traffic destination](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/traffic_to_1.png){class="glboxshadow"}

    ![traffic destination](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/traffic_to_2.png){class="glboxshadow"}

    - **All Targets**: 선택하면 이 규칙과 일치하는 트래픽이 모든 대상으로 라우팅됩니다.

        ![all targets](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/all_targets.png){class="glboxshadow"}

    - **Specified Domain / IP List**: 선택하면 이 규칙과 일치하는 트래픽이 지정된 도메인이나 IP 주소로 라우팅됩니다. 수동으로 입력해야 합니다.

        ![specified domain/IP manual](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/specified_domain_ip_manual.png){class="glboxshadow"}

        또는 **Input Mode**를 Manual에서 Subscription URL로 전환하고 URL 링크를 입력하세요.

        ![specified domain/IP subscription](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/specified_domain_ip_subscription.png){class="glboxshadow"}

        !!! Note

            - Subscribe URL을 선택하면 URL의 도메인 이름이나 IP가 매일 자동으로 업데이트됩니다.

            - 올바른 URL을 입력하세요. URL 검색은 도메인 이름이나 IP 주소의 유효성을 검증합니다. [자세히 보기](../tutorials/how_to_configure_domain_and_ip_filtering_rules_for_glinet_routers_via_an_online_text_file.md){target="_blank"}

    - **Exclude Specified Domain / IP List**: 선택하면 이 규칙과 일치하는 트래픽이 지정된 도메인이나 IP 주소로 라우팅되지 **않습니다**. 수동으로 입력해야 합니다.

        ![exclude specified domain/IP manual](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/exclude_domain_ip_manual.png){class="glboxshadow"}

        또는 **Input Mode**를 Manual에서 Subscription URL로 전환하고 URL 링크를 입력하세요.

        ![exclude specified domain/IP subscription](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/exclude_domain_ip_subscription.png){class="glboxshadow"}

        !!! Note

            - Subscribe URL을 선택하면 URL의 도메인 이름이나 IP가 매일 자동으로 업데이트됩니다.

            - 올바른 URL을 입력하세요. URL 검색은 도메인 이름이나 IP 주소의 유효성을 검증합니다. [자세히 보기](../tutorials/how_to_configure_domain_and_ip_filtering_rules_for_glinet_routers_via_an_online_text_file.md){target="_blank"}

3. **Via**: 트래픽 라우팅 방법을 나타내며, VPN 사용 여부를 나타냅니다.

    회색 상자를 클릭하여 라우팅 방법을 선택하세요.

    ![via](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/traffic_via_1.png){class="glboxshadow"}

    ![via](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/traffic_via_2.png){class="glboxshadow"}

    - **Use VPN**: 선택하면 이 규칙과 일치하는 트래픽이 VPN을 통해 선택한 대상으로 라우팅됩니다.

        먼저 라우터를 VPN 클라이언트로 구성해야 합니다. [VPN Setup Wizard](#vpn-setup-wizard)를 사용하여 빠르게 구성을 완료하거나 왼쪽 사이드바에서 OpenVPN Client / WireGuard Client로 이동하여 수동으로 구성하세요.

        라우터를 VPN 클라이언트로 설정하면 이 터널에 대한 VPN 구성 파일을 선택하고 **Apply**를 클릭하세요.

        ![use vpn](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/use_vpn_2.png){class="glboxshadow"}

    - **Not Use VPN**: 선택하면 이 규칙과 일치하는 트래픽이 VPN 대신 로컬 WAN을 통해 선택한 대상으로 라우팅됩니다.

        ![not use vpn](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/not_use_vpn.png){class="glboxshadow"}

4. 트래픽 소스, 대상, 라우팅 방법을 선택하면 기본 터널 규칙 설정이 완료됩니다.

다음 예에서는 Primary Tunnel 규칙이 다음과 같습니다: 모든 클라이언트가 VPN을 사용하여 지정된 도메인에 액세스합니다. 트래픽은 호주 서버를 통해 라우팅되고 이 터널을 통해 선택한 인터넷 도메인으로 나갑니다.

![connected policy mode](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/connected-policy-mode.jpg){class="glboxshadow"}

**참고**: 보안을 위해 터널을 활성화하기 전에 [All Other Traffic](#all-other-traffic) 및 [Tunnel Options](#tunnel-options)로 이동하여 다른 설정을 확인하세요.

#### Add Tunnel

여러 VPN 인스턴스에 대한 추가 터널을 생성하려면 Primary Tunnel 아래의 **Add Tunnel**을 클릭하고 사용자 정의 규칙을 구성하세요.

![add tunnel](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/add_tunnel.jpg){class="glboxshadow"}

터널의 이름을 지정합니다.

![name tunnel](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/name_tunnel.png){class="glboxshadow"}

VPN Dashboard에 터널이 하나 더 표시됩니다.

![two tunnels](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/two_tunnels.png){class="glboxshadow"}

필요한 경우 더 많은 터널을 추가할 수 있습니다. 최대 5개의 터널(사전 설정된 기본 터널 포함)을 생성할 수 있습니다.

트래픽 소스, 대상, 라우팅 방법을 설정하여 터널 규칙을 사용자 정의하세요. [Primary Tunnel](#primary-tunnel)을 참조하세요.

**참고**: 보안을 위해 터널을 활성화하기 전에 [All Other Traffic](#all-other-traffic) 및 [Tunnel Options](#tunnel-options)로 이동하여 다른 설정을 확인하세요.

#### All Other Traffic

Policy Mode에서 VPN Dashboard 하단에 <u>사전 활성화된</u> 터널이 표시됩니다.

![all other traffic](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/all_other_traffic.png){class="glboxshadow"}

이 터널은 위의 VPN 터널 그룹과 일치하지 않는 트래픽이 인터넷에 액세스할 수 있는지 여부를 제어합니다. VPN을 통해 라우팅되지 않은 트래픽의 정상적인 인터넷 액세스를 보장하기 위해 기본적으로 활성화되어 있습니다.

- 활성화되면 일치하지 않는 트래픽이 여전히 인터넷에 액세스할 수 있습니다.

    ![all other traffic on](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.9/all_other_traffic_on.png){class="glboxshadow"}

- 비활성화되면 VPN을 통해 라우팅된 트래픽만 인터넷에 액세스할 수 있습니다. 모든 비-VPN 트래픽과 VPN 연결에서 장애 조치(failover)된 트래픽은 차단됩니다. 이 옵션은 각 VPN 터널의 개별 Kill Switch를 재정의하지 않습니다.

    ![all other traffic off](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.9/all_other_traffic_off.png){class="glboxshadow"}

#### Tunnel Priority

기본적으로 사전 설정된 Primary Tunnel이 최우선 순위를 가지며, 그 다음 다른 수동으로 추가된 터널(있는 경우), 그리고 로컬 네트워크 연결성(로컬 WAN 통해)을 보장하는 All Other Traffic 터널 순입니다.

터널 우선 순위를 수정하려면 상단 정보 표시줄의 **Modify Priority**를 클릭하거나 터널 좌측 상단의 **priority label**(예: Priority 1/Priority 2)을 클릭하세요.

![modify priority](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/modify_priority_1.png){class="glboxshadow"}

우측의 세 줄 아이콘을 클릭하고 길게 눌러 터널 순서를 재정렬한 다음 **Apply**를 클릭하세요.

![modify priority](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/modify_priority_2.png){class="glboxshadow"}

**여러 터널이 활성화되면 라우터는 다음 순서로 트래픽을 라우팅합니다**:

1. 트래픽은 먼저 최우선 순위 터널 규칙과 일치하는지 시도합니다. 일치하면 해당 터널을 통해 라우팅되고, 그렇지 않으면 다음 우선 순위 터널을 시도하여 "All Other Traffic" 터널과 일치할 때까지 계속됩니다.

2. VPN 터널이 예기치 않게 연결 해제되면 이 터널의 **Kill Switch**가 활성화되어 있는지에 따라 시스템에서 트래픽을 다음 우선 순위 터널로 장애 조치할지 여부를 결정합니다.

    - Kill Switch가 활성화되면 트래픽이 차단되고 다음 우선 순위 터널로 장애 조치되지 않습니다.
    - Kill Switch가 비활성화되면 트래픽이 다음 우선 순위 터널로 장애 조치되고 터널 규칙과 일치하는지 시도합니다.

3. **All Other Traffic** 터널은 VPN 터널과 일치하지 않는 트래픽이 여전히 인터넷에 액세스할 수 있도록 기본적으로 활성화되어 있습니다.

    - 활성화되면 일치하지 않거나 장애 조치된 트래픽을 로컬 WAN을 통해 라우팅합니다.
    - 비활성화되면 Kill Switch를 강화하고 IP 유출을 방지하기 위해 일반 인터넷 액세스를 차단합니다.

#### Tunnel Options

각 VPN 터널에 대한 VPN Kill Switch, IP Masquerading, MTU와 같은 고급 설정을 구성할 수 있습니다.

터널 이름 옆의 기어 아이콘을 클릭하고 **Options**를 선택하세요.

![tunnel options](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/tunnel_options_1.png){class="glboxshadow"}

![tunnel options](https://static.gl.inet.com/docs/router/en/4/interface_guide/vpn_dashboard/4.8/tunnel_options_2.png){class="glboxshadow"}

- **Kill Switch**: 활성화되면 VPN 연결이 예기치 않게 실패할 경우 이 VPN 터널과 일치하는 트래픽이 차단됩니다. 비활성화되면 해당 트래픽이 다음 우선 순위 터널이나 로컬 WAN으로 장애 조치됩니다.

- **Services from GL.iNet Use VPN**: 활성화되면 GoodCloud, DDNS, rtty 서비스가 VPN 터널을 통해 패킷을 전송합니다. 이러한 서비스는 일반적으로 장치의 실제 IP 주소가 필요하므로 기본적으로 비활성화되어 있습니다.

- **Allow Remote Access the LAN Subnet**: 활성화되면 VPN을 통해 이 라우터와 LAN 장치에 대한 원격 액세스가 허용됩니다. VPN 서버가 LAN 서브넷으로 돌아가는 경로를 알려야 합니다.

- **IP Masquerading**: 활성화되면 LAN 클라이언트의 소스 IP 주소가 라우터의 VPN 터널 IP로 다시 작성됩니다. 원격 피어가 LAN 서브넷을 알고 있는 Site-to-Site 설정에서만 비활성화하세요.

- **MTU**: 터널에 설정한 MTU 값은 구성 파일의 MTU 설정을 재정의합니다.

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}을 통해 연락하세요.
