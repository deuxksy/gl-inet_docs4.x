# ZeroTier

ZeroTier는 인터넷을 통해 장치 간 보안 암호화 통신을 활성화하는 소프트웨어 기반 가상 사설망(VPN)입니다. 물리적 위치나 네트워크 토폴로지에 관계없이 장치가 동일한 로컬 네트워크에 있는 것처럼 통신할 수 있는 개인용 가상 네트워크를 만듭니다. ZeroTier는 설정 및 사용이 쉽고 엔드 투엔 암호화, 네트워크 분할, 네트워크 브리징 기능과 같은 기능을 제공하도록 설계되었습니다.

GL.iNet 라우터의 ZeroTier 기능은 펌웨어 v4.2부터 사용할 수 있으며 라우터가 ZeroTier 가상 네트워크에 연결할 수 있습니다. 연결되면 WAN 및 LAN 리소스를 포함하여 라우터를 원격으로 액세스할 수 있습니다.

**참고**:

1. 다음 기능이나 서비스와 동시에 ZeroTier를 사용하면 라우팅 충돌이 발생할 수 있으므로 권장하지 않습니다: OpenVPN Client, WireGuard Client, GoodCloud Site to Site, Tailscale, AstroWarp.

2. 이 기능은 현재 베타이며 일부 버그가 있을 수 있습니다.

## 지원되는 모델

??? "지원되는 모델"
    - GL-E5800 (Mudi 7)
    - GL-MT5000 (Brume 3)
    - GL-MT3600BE (Beryl 7)
    - GL-BE6500 (Flint 3e)
    - GL-BE9300 (Flint 3)
    - GL-BE3600 (Slate 7)
    - GL-B3000 (Marble)
    - GL-MT6000 (Flint2)
    - GL-X3000 (Spitz AX)
    - GL-XE3000 (Puli AX)
    - GL-AX1800 (Flint)
    - GL-MT2500/GL-MT2500A (Brume 2)
    - GL-MT3000 (Beryl AX)
    - GL-AXT1800 (Slate AX)
    - GL-A1300 (Slate Plus)

??? "지원되지 않는 모델"
    - GL-X2000 (Spitz Plus)
    - GL-SFT1200 (Opal)
    - GL-MT1300 (Beryl)
    - GL-E750/E750V2 (Mudi)
    - GL-X750/GL-X750V2 (Spitz)
    - GL-AR750S (Slate)
    - GL-XE300 (Puli)
    - GL-MT300N-V2 (Mango)
    - GL-AR300M Series (Shadow)
    - GL-B1300 (Convexa-B)
    - GL-AP1300 (Cirrus)
    - GL-S1300 (Convexa-S)
    - GL-X300B (Collie)

## ZeroTier 네트워크 설정

ZeroTier Central의 두 가지 버전을 사용할 수 있습니다: New Central과 Legacy Central.

- **New Central**: 개선된 사용성과 새로운 기능을 갖춘은 최신 버전의 ZeroTier Central입니다. 최상의 경험과 최신 도구를 위해서 새로운 사용자에게 권장됩니다.

- **Legacy Central**: 2025년 11월 이전에 생성된 계정용입니다. Legacy Central은 기존 사용자가 네트워크를 관리할 수 있도록 계속 지원합니다.

두 버전을 병렬로 사용할 수 있지만 현재는 직접 마이그레이션 경로가 없습니다.

적절한 버전을 선택하여 진행하세요.

### New Central

다음은 GL-MT3600BE를 사용한 예입니다.

1. [ZeroTier 공식 웹사이트](https://www.zerotier.com/){target="_blank"}를 방문하여 계정으로 로그인하세요.

    ![create organization](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/new_central/zerotier_login.jpg){class="glboxshadow"}

2. 조직을 생성합니다.

    ![create organization](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/new_central/create_org.png){class="glboxshadow"}

3. 플랜을 선택합니다. 여기서는 Personal 플랜을 예로 듭니다. 이 플랜은 10개의 장치, 1명의 네트워크 관리자, 1개의 네트워크를 포함합니다. 더 많은 네트워크를 생성하거나 더 많은 장치를 추가하거나 사용자 정의 경로와 DNS를 추가하려면 Essential 또는 Scale 플랜을 선택하세요.

    ![select plan](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/new_central/select_plan.png){class="glboxshadow"}

4. 이제 ZeroTier 네트워크가 생성되었습니다. 우측 상단의 **Network ID**를 기록해 두세요. 16자 영숫자 조합으로 나중에 다른 장치를 연결할 때 필요합니다.

    ![network id](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/new_central/zt_network_id.png){class="glboxshadow"}

5. GL.iNet 라우터에서 ZeroTier를 활성화합니다.

    라우터의 웹 관리 패널에 로그인하고 **APPLICATIONS** -> **ZeroTier**로 이동합니다.

    ZeroTier를 활성화하고 동일한 페이지에 Network ID를 입력한 다음 **Apply**를 클릭하세요.

    ![enable zerotier](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/new_central/enable_zerotier.png){class="glboxshadow"}

    잠시 후 인터페이스에 승인이 필요하다고 표시됩니다. **ZeroTier Central** 하이퍼링크를 클릭하여 ZeroTier Central로 리디렉션합니다.

    ![authorize 1](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/new_central/authorize1.png){class="glboxshadow"}

6. ZeroTier Central에서 장치를 승인합니다.

    ZeroTier Central에서 보류 중인 장치를 찾아 승인하세요.

    ![authorize 2](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/new_central/authorize2.png){class="glboxshadow"}

    승인되면 페이지가 아래와 같이 표시됩니다.

    ![authorized 1](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/new_central/authorized1.png){class="glboxshadow"}

7. [이 가이드](https://docs.zerotier.com/platforms/){target="_blank"}를 따라 동일한 ZeroTier 네트워크에 다른 장치(예: 컴퓨터 또는 스마트폰)를 추가합니다.

    다음은 Windows 10 Pro 노트북을 사용한 예입니다.

    1. [여기](https://www.zerotier.com/download/){target="_blank"}에서 노트북에 ZeroTier를 설치합니다.

    2. ZeroTier를 실행합니다. 바탕화 우측 하단 시스템 트레이에 ZeroTier 아이콘이 나타납니다.

    3. 아이콘을 마우스 오른쪽 버튼으로 클릭하고 **Join New Network**를 선택한 다음 팝업 창에서 4단계에서 얻은 **Network ID**를 입력합니다.

        ![laptop join network](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/new_central/laptop_join_network.png){class="glboxshadow"}

        그런 다음 ZeroTier Central로 이동하여 보류 중인 장치를 찾아 승인합니다.

        ![authorize 3](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/new_central/authorize3.png){class="glboxshadow"}

    4. 승인되면 페이지가 아래와 같이 표시됩니다. **Device ID**, **Name**, **Status**, **Managed IP**, **Public IP** 등 구성원 장치의 세부 정보를 볼 수 있습니다.

        ![authorized 2](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/new_central/authorized2.png){class="glboxshadow"}

        **팁**: 오른쪽의 점 3개 아이콘을 클릭하여 장치 이름, Managed IP, 고급 설정 등 구성원 장치 설정을 편집할 수 있습니다.

8. 라우터의 **Managed IP**를 클릭하여 복사합니다. 그런 다음 동일한 ZeroTier 네트워크에 있는 노트북에서 이 Managed IP를 사용하여 라우터에 액세스할 수 있습니다.

    ![zerotier virtual ip](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/new_central/zerotier_virtual_ip.png){class="glboxshadow"}

9. 연결성을 테스트합니다.

    동일한 ZeroTier 네트워크에 연결된 노트북에서 웹 브라우저를 열고 이전 단계에서 얻은 라우터의 Managed IP를 입력합니다.

    라우터의 웹 관리 패널에 액세스할 수 있으면 ZeroTier 연결이 성공한 것입니다.

    ![web admin panel](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/new_central/connectivity_test1.png){class="glboxshadow"}

    노트북에서 라우터의 Managed IP로 `ping`을 수행하여 연결성을 테스트할 수도 있습니다. 성공적인 응답을 받으면 ZeroTier 연결이 성공적으로 설정된 것입니다.

    ![ping test](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/new_central/connectivity_test2.png){class="glboxshadow"}

### Legacy Central

다음은 GL-MT2500를 사용한 예입니다.

1. 첫 번째 ZeroTier 네트워크를 생성합니다.

    ZeroTier 공식 [시작 가이드](https://docs.zerotier.com/getting-started/getting-started/){target="_blank"}를 참조하여 ZeroTier 계정과 네트워크를 생성하세요. 나중에 다른 장치를 연결할 때 필요하므로 Network ID(16자 영숫자 조합)를 기록해 두세요.

    ![zerotier network id](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/zerotier_network_id.png){class="glboxshadow"}

2. GL.iNet 라우터에서 ZeroTier를 활성화합니다.

    라우터의 웹 관리 패널에 로그인하고 **APPLICATIONS** -> **ZeroTier**로 이동합니다.

    ZeroTier를 활성화하고 동일한 페이지에 Network ID를 입력한 다음 **Apply**를 클릭하세요.

    ![enable zerotier](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/zerotier_enable.png){class="glboxshadow"}

    잠시 후 인터페이스에 승인이 필요하다고 표시됩니다.

    **ZeroTier Central** 하이퍼링크를 클릭하여 ZeroTier Central로 리디렉션하세요.

    ![zerotier central](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/zerotier_central.png){class="glboxshadow"}

3. ZeroTier Central에서 장치를 승인합니다.

    ZeroTier Central에서 **Members** 섹션으로 이동합니다. 새 장치를 찾아 **Auth** 체크박스를 클릭하여 승인합니다. 원하는 경우 장치 이름을 사용자 정의할 수 있습니다.

    ![zerotier members, auth](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/zerotier_members_auth.png){class="glboxshadow"}

    잠시 후 ZeroTier가 장치에 **Managed IP**를 할당합니다. 테스트 단계에서 사용할 IP 주소를 기록해 두세요.

    ![zerotier managed ip](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/managed_ip.png){class="glboxshadow"}

4. [이 가이드](https://docs.zerotier.com/platforms/){target="_blank"}를 따라 동일한 ZeroTier 네트워크에 다른 장치(예: 컴퓨터 또는 스마트폰)를 추가합니다.

5. 연결성을 테스트합니다.

    동일한 ZeroTier 네트워크에 연결된 다른 장치에서 웹 브라우저를 열고 이전 단계에서 얻은 라우터의 ZeroTier Managed IP를 입력합니다.

    라우터의 웹 관리 패널에 액세스할 수 있습니다.

    ![web admin panel](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/web_admin_panel.png)

    연결성을 테스트하기 위해 `ping` 명령을 사용할 수도 있습니다. ZeroTier [Quickstart Guide](https://docs.zerotier.com/quickstart/#6-test-your-connection){target="_blank"}를 참조하세요.

## 원격 액세스 WAN 허용

이 옵션을 활성화하면 장치의 WAN 측 리소스를 ZeroTier 가상 네트워크를 통해 액세스할 수 있습니다.

예를 들어 아래 토폴로지와 같이 이 기능을 활성화하면 `leo-phone`에서 `GL-AXT1800`의 IP 주소(`192.168.29.1`)를 통해 액세스할 수 있습니다. 이는 `GL-AXT1800`가 `GL-MT2500`의 상위 장치이며 후자가 leo-phone과 동일한 ZeroTier 네트워크에 연결되어 있기 때문입니다.

![remote access wan topology](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/zerotier_access_wan_topology.png){class="glboxshadow"}

**참고**: 이 기능이 적용되려면 ZeroTier 네트워크에 경로 규칙을 추가해야 합니다. Legacy Central에서는 무료로 맞춤 사용자 정의 경로를 하나 추가할 수 있지만 New Central에서는 Essential 플랜 이상에서만 사용자 정의 경로를 구성할 수 있습니다. 자세한 내용은 [여기](https://www.zerotier.com/pricing/)를 클릭하세요.

다음 단계는 Legacy Central을 예로 사용합니다.

1. 라우터의 웹 관리 패널에 로그인하고 **APPLICATIONS** -> **ZeroTier**로 이동합니다.

    **Allow Remote Access WAN**을 활성화하고 **Apply**를 클릭하세요.

    ![enable allow remote access wan](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/enable_allow_remote_access_wan_1.png){class="glboxshadow"}

    경로 규칙을 구성하라는 메시지가 표시됩니다. 이 웹페이지를 열어 두거나 경로 세부 정보(Destination 및 Via)를 기록해 두세요. 다음 단계에서 필요합니다.

    ![enable allow remote access wan](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/enable_allow_remote_access_wan_2.png){class="glboxshadow"}

2. **ZeroTier Central**로 이동하여 **Advanced** 섹션을 찾습니다.

    이전 단계에서 얻은 경로 세부 정보(Destination 및 Via)를 입력하고 **Submit**를 클릭하세요.

    ![add route](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/add_routes_1.png){class="glboxshadow"}

    경로가 추가되면 **Managed Routes** 섹션이 아래와 같이 표시됩니다.

    ![add route](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/add_routes_2.png){class="glboxshadow"}

3. 이제 다른 장치에서 `GL-AXT1800`의 IP 주소(`192.168.29.1`)를 통해 액세스할 수 있습니다. 실제로는 `192.168.29.0/24` 서브넷 내의 모든 장치에 액세스할 수 있습니다.

    ![access axt1800](https://static.gl.inet.com/docs/router/en/4/tutorials/tailscale/tailscale_access_axt1800.jpg){class="glboxshadow gl-50-desktop"}

## 원격 액세스 LAN 허용

이 옵션을 활성화하면 장치의 LAN 측 리소스를 ZeroTier 가상 네트워크를 통해 액세스할 수 있습니다.

예를 들어 아래 토폴로지와 같이 이 기능을 활성화하면 `leo-phone`에서 `Ubuntu`의 IP 주소(`192.168.8.110`)를 통해 SSH 로그인할 수 있습니다. 이는 `Ubuntu`가 `GL-MT2500`의 하위 장치이며 후자가 leo-phone과 동일한 ZeroTier 네트워크에 연결되어 있기 때문입니다.

![remote access lan topology](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/zerotier_access_lan_topology.png){class="glboxshadow"}

**참고**: 이 기능이 적용되려면 ZeroTier 네트워크에 경로 규칙을 추가해야 합니다. Legacy Central에서는 무료로 맞춤 사용자 정의 경로를 하나 추가할 수 있지만 New Central에서는 Essential 플랜 이상에서만 사용자 정의 경로를 구성할 수 있습니다. 자세한 내용은 [여기](https://www.zerotier.com/pricing/)를 클릭하세요.

다음 단계는 Legacy Central을 예로 사용합니다.

1. 라우터의 웹 관리 패널에 로그인하고 **APPLICATIONS** -> **ZeroTier**로 이동합니다.

    **Allow Remote Access LAN**을 활성화하고 **Apply**를 클릭하세요.

    ![enable allow remote access lan](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/enable_allow_remote_access_lan_1.png){class="glboxshadow"}

    경로 규칙을 구성하라는 메시지가 표시됩니다. 이 웹페이지를 열어 두거나 경로 세부 정보(Destination 및 Via)를 기록해 두세요. 다음 단계에서 필요합니다.

    ![enable allow remote access lan](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/enable_allow_remote_access_lan_2.png){class="glboxshadow"}

2. **ZeroTier Central**로 이동하여 **Advanced** 섹션을 찾습니다.

    이전 단계에서 얻은 경로 세부 정보(Destination 및 Via)를 입력하고 **Submit**를 클릭하세요.

    ![add route](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/add_routes_3.png){class="glboxshadow"}

    경로가 추가되면 **Managed Routes** 섹션이 아래와 같이 표시됩니다.

    ![add route](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/add_routes_4.png){class="glboxshadow"}

3. 이제 다른 장치에서 `Ubuntu`의 IP 주소(`192.168.8.110`)를 통해 ping하거나 SSH 로그인할 수 있습니다. 실제로는 `192.168.8.0/24` 서브넷 내의 모든 장치에 액세스할 수 있습니다.

    ![access ubuntu](https://static.gl.inet.com/docs/router/en/4/tutorials/zerotier/zerotier_access_ubuntu.jpg){class="glboxshadow gl-80-desktop"}

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}을 통해 연락하세요.
