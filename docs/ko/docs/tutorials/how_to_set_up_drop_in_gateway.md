# GL.iNet 라우터에서 Drop-in Gateway 설정 방법

GL.iNet은 Drop-in Gateway 기능을 제공하여 기본 라우터의 기능을 AdGuard Home, 암호화된 DNS, VPN과 같이 기본 라우터에 없을 수 있는 기능으로 향상시킵니다. 이 기능을 사용하면 추가 기능을 즐기면서 기본 라우터를 평소처럼 계속 사용할 수 있습니다.

기본 라우터에 연결된 [모든 장치](#모든-장치에-대해-drop-in-gateway-활성화) 또는 [특정 장치](#특정-장치에-대해-drop-in-gateway-활성화)에 대해 Drop-in Gateway를 활성화할 수 있습니다. 설정에 따라 해당 섹션을 따르세요.

**참고**: 펌웨어 버전이 v4.5.0 미만인 모델은 모든 장치에 대해 Drop-in Gateway 활성화만 지원합니다. Drop-in Gateway가 활성화되면 모든 클라이언트 장치가 Drop-in Gateway를 통해 네트워킹되며, 이는 연결된 모든 클라이언트의 트래픽이 이 라우터에서 먼저 처리됨을 의미합니다.

---

## 모든 장치에 대해 Drop-in Gateway 활성화

### 1. GL.iNet 라우터를 기본 라우터에 연결

이더넷 케이블을 사용하여 GL.iNet 라우터의 WAN 포트를 기본 라우터의 LAN 포트에 연결하세요.

### 2. Drop-in Gateway 활성화

Drop-in Gateway를 활성화하는 두 가지 방법이 있습니다. 라우터 관리 패널 또는 GL.iNet 모바일 앱을 통하는 방법입니다.

??? "웹 관리 패널 사용"

    1. 웹 브라우저에서 `192.168.8.1`을 입력하세요.

    2. 비밀번호를 입력한 다음 **Login**을 클릭하세요.

    3. 왼쪽 사이드바에서 **Network** > **Drop-in Gateway**를 클릭하세요.

        ![click drop-in gateway](https://static.gl.inet.com/docs/router/en/4/tutorials/how_to_set_up_drop_in_gateway/click-drop-in-gateway.jpeg){class="glboxshadow"}

    4. **Enable Drop-in Gateway Mode** 옆에서 스위치를 켜세요.

    5. **All devices are networked through drop-in gateway**를 선택하세요.

        ![click all devices](https://static.gl.inet.com/docs/router/en/4/tutorials/how_to_set_up_drop_in_gateway/select-all-devices.jpeg){class="glboxshadow"}

    6. **Apply**를 클릭하세요.

??? "GL.iNet 모바일 앱 사용"

    **참고:** 시작하기 전에 기기에 GL.iNet 모바일 앱을 설치하세요.

    1. 기본 앱 화면에서 **System** 탭 > **Drop-in Gateway**를 탭하세요.

        ![tap drop-in gateway](https://static.gl.inet.com/docs/router/en/4/tutorials/how_to_set_up_drop_in_gateway/tap-drop-in-gateway.jpeg){class="glboxshadow"}

    2. **Enable**를 탭하세요.

    3. **Devices are networked via drop-in gateway**에서 **All**을 탭하세요.

        ![tap all](https://static.gl.inet.com/docs/router/en/4/tutorials/how_to_set_up_drop_in_gateway/drop-in-gateway-tap-all.jpeg){class="glboxshadow"}

    4. **Done**을 탭하세요.

### 3. 기본 라우터에서 DHCP 서버 비활성화

기본 라우터에 로그인하여 DHCP 서버를 비활성화하세요. 라우터 제조업체에서 제공하는 지침을 참조하거나 지원팀에 문의하세요.

### 4. AdGuard, DNS, VPN 및 기타 기능 설정

GL.iNet 라우터에서 원하는 기능을 활성화하려면 이 가이드를 따르세요.

* [AdGuard Home](../interface_guide/adguardhome.md){target="_blank"}
* [암호화된 DNS](../interface_guide/dns.md){target="_blank"}
* [Parental Control](../interface_guide/parental_control.md){target="_blank"}
* [WireGuard Client](../interface_guide/wireguard_client.md){target="_blank"}
* [OpenVPN Client](../interface_guide/openvpn_client.md){target="_blank"}

---

## 특정 장치에 대해 Drop-in Gateway 활성화

### 1. GL.iNet 라우터를 기본 라우터에 연결

이더넷 케이블을 사용하여 GL.iNet 라우터의 WAN 포트를 기본 라우터의 LAN 포트에 연결하세요.

### 2. Drop-in Gateway 활성화

Drop-in Gateway를 활성화하는 두 가지 방법이 있습니다. [라우터 관리 패널](#웹-관리-패널-사용) 또는 [GL.iNet 모바일 앱](#glinet-모바일-앱-사용)을 통하는 방법입니다.

??? "웹 관리 패널 사용"

    1. 웹 브라우저에서 `192.168.8.1`을 입력하세요.

    2. 비밀번호를 입력한 다음 **Login**을 클릭하세요.

    3. 왼쪽 사이드바에서 **Network** > **Drop-in Gateway**를 클릭하세요.

        ![click drop-in gateway](https://static.gl.inet.com/docs/router/en/4/tutorials/how_to_set_up_drop_in_gateway/click-drop-in-gateway.jpeg){class="glboxshadow"}

    4. **Enable Drop-in Gateway Mode** 옆에서 스위치를 켜세요.

    5. **Some devices select their own networking gateway**를 선택하세요.

        ![click some devices](https://static.gl.inet.com/docs/router/en/4/tutorials/how_to_set_up_drop_in_gateway/select-some-devices.jpeg){class="glboxshadow"}

    6. **Apply**를 클릭하세요.

    **참고:** 이 탭을 닫지 마세요. 다음 단계에서 화면에 표시된 IP 주소를 입력해야 합니다.

??? "GL.iNet 모바일 앱 사용"

    **참고:** 시작하기 전에 기기에 GL.iNet 모바일 앱을 설치하세요.

    1. 기본 앱 화면에서 **System** 탭 > **Drop-in Gateway**를 탭하세요.

        ![tap drop-in gateway](https://static.gl.inet.com/docs/router/en/4/tutorials/how_to_set_up_drop_in_gateway/tap-drop-in-gateway.jpeg){class="glboxshadow"}

    2. **Enable**를 탭하세요.

    3. **Devices are networked via drop-in gateway**에서 **part**를 탭하세요.

        ![tap part](https://static.gl.inet.com/docs/router/en/4/tutorials/how_to_set_up_drop_in_gateway/drop-in-gateway-tap-part.jpeg){class="glboxshadow"}

    4. **Done**을 탭하세요.

    **참고:** 이 탭을 닫지 마세요. 다음 단계에서 화면에 표시된 IP 주소를 입력해야 합니다.

### 3. 특정 장치에서 게이트웨이 및 DNS 설정

??? "Windows"

    1. 장치를 기본 라우터에 연결하세요.
    2. Windows에서 **Settings** > **Network & Internet**를 열세요.
    3. 연결 방법에 따라 다음 단계를 따르세요.
        * Ethernet: **Ethernet**을 클릭하세요.
        * Wi-Fi: **Wi-Fi**를 클릭한 다음 Wi-Fi 네트워크 이름을 클릭하세요.
    4. IPv4 주소를 복사하세요. **IP assignment** 옆에서 **Edit**를 클릭하세요.
    5. **Manual**을 클릭하세요.
    6. **IPv4**를 켭니다.
    7. 다음 정보를 입력하세요.
        * **IP address:** 4단계에서 복사한 IP 주소를 붙여넣으세요.
        * **Subnet mask:** **255.255.255.0**을 입력하세요.
        * **Gateway:** **Drop-in Gateway** 페이지에 표시된 IP 주소를 입력하세요.
        * **Preferred DNS:** **Drop-in Gateway** 페이지에 표시된 IP 주소를 입력하세요.
    8. **Save**를 클릭하세요.

??? "Android"
    1. 장치를 기본 라우터에 연결하세요.
    2. Android에서 **Settings**를 열세요.
    3. **Connections** > **Wi-Fi**를 탭하세요.
    4. 연결된 네트워크 옆에 있는 **Settings** 아이콘을 탭하세요.
    5. **View more**를 탭하세요.
    6. **IP settings** > **Static**을 탭하세요.
    7. **Gateway** 및 **DNS 1**에 **Drop-in Gateway** 화면에 표시된 IP 주소를 입력하세요.
    8. **Save**를 탭하세요.

??? "iOS"
    1. 장치를 기본 라우터에 연결하세요.
    2. iOS에서 **Settings**를 여세요.
    3. **Wi-Fi**를 탭하세요.
    4. 연결된 Wi-Fi 네트워크를 탭하세요.
    5. **IPv4 Address** 아래에서 **IP Address** 및 **Subnet Mask**를 기록하세요.
    6. **Configure IP** > **Manual**을 탭하세요.
    7. 다음 정보를 입력하세요.
        * **IP Address:** 5단계에서 얻은 IP Address를 입력하세요.
        * **Subnet Mask:** 5단계에서 얻은 Subnet Mask를 입력하세요.
        * **Router:** **Drop-in Gateway** 화면에 표시된 IP 주소를 입력하세요.
    8. **Save**를 탭하세요.
    9. **Configure DNS**를 탭한 다음 **Manual**을 탭하세요.
    10. **Add Server**를 탭한 다음 **Drop-in Gateway** 화면에 표시된 IP 주소를 입력하세요.
    11. **Save**를 탭하세요.

??? "Mac"
    1. 장치를 기본 라우터에 연결하세요.
    2. Mac에서 Apple 아이콘을 클릭 > **System Settings**를 클릭하세요.
    3. 왼쪽 사이드바에서 **Network**를 클릭하세요.
    4. 연결된 네트워크 옆에서 **Details**를 클릭하세요.
    5. **TCP/IP**를 클릭하세요.
    6. **IP Address** 및 **Subnet Mask**를 기록하세요.
    7. **Configure IPv4** 옆에서 **Manually**를 클릭하세요.
    8. 다음 정보를 입력하세요.
        * **IP address:** 6단계에서 얻은 IP Address를 입력하세요.
        * **Subnet mask:** 6단계에서 얻은 IP Address를 입력하세요.
        * **Router:** **Drop-in Gateway** 페이지에 표시된 IP 주소를 입력하세요.
    9. **OK** > **OK**를 클릭하세요.

### 4. AdGuard, DNS, VPN 및 기타 기능 설정

GL.iNet 라우터에서 원하는 기능을 활성화하려면 이 가이드를 따르세요.

* [AdGuard Home](../interface_guide/adguardhome.md){target="_blank"}
* [암호화된 DNS](../interface_guide/dns.md){target="_blank"}
* [Parental Control](../interface_guide/parental_control.md){target="_blank"}
* [WireGuard Client](../interface_guide/wireguard_client.md){target="_blank"}
* [OpenVPN Client](../interface_guide/openvpn_client.md){target="_blank"}

---

관련 문서:

- [Drop-in Gateway](../interface_guide/drop-in_gateway.md)

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}을 통해 연락하세요.
