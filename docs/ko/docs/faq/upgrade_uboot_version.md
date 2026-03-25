# Uboot 버전 업그레이드

## 경고

**Uboot 업그레이드는 매우 위험하며 일반적으로 권장하지 않습니다. 한 번 실패하면 장치가 벽돌(bricked)되며 복구할 방법이 없습니다. 필요한 경우 또는 GL.iNet 지원팀의 지시가 있을 때만 수행하세요.**

**업그레이드 과정에서 전원을 끄지 마세요. 그렇지 않으면 업그레이드가 실패하고 장치가 벽돌될 수 있습니다.**

## 준비

- 이더넷 포트가 있는 컴퓨터. 없는 경우 추가 USB 이더넷 어댑터를 준비하세요.
- 이더넷 케이블.
- GL-iNet 지원팀의 지시에 따라 Uboot 파일을 다운로드하세요. 올바른 uboot 파일을 사용하는지 확인하세요. Uboot 파일 다운로드 방법을 모르는 경우 support@gl-inet.com으로 이메일을 보내 문의하세요.

## 업그레이드 단계

아래 절차에 따라 U-Boot 업그레이드 페이지에 액세스하세요.

1. 라우터의 전원을 제거하세요. 컴퓨터를 라우터의 **이더넷 LAN 포트**에 연결하세요. 다른 모든 포트는 **연결하지 마세요**.

    !!! note

        일부 모델에서는 개별 LAN 포트와 WAN 포트가 상호 교체 가능합니다. 이 LAN 포트를 사용하지 마세요. 예를 들어 GL-MT6000 (Flint 2)에서는 LAN 1을 사용하지 마세요. 대신 LAN 2, LAN 3 또는 LAN 4를 사용하세요.

2. Reset 버튼을 단단히 누른 상태에서 동시에 라우터의 전원을 켜세요. 라우터에 전원 버튼이 없는 경우 전원을 연결하면 자동으로 켜집니다.

    그러면 LED가 몇 번 정기적인 순서로 깜빡이게 됩니다. 순서가 바뀔 때 손가락을 놓으세요.

3. 컴퓨터의 IP 주소를 **192.168.1.2**로 수동 설정하세요. 다른 운영체제에 대한 단계별 가이드는 아래와 같습니다:

    ??? "Windows 7 / Windows 10"

        1. **Control Panel** -> **Network and Internet** -> **Network and Sharing Center** -> **Change adapter settings**로 이동하세요.

        2. **Local Area Connection** -> **Properties**를 마우스 오른쪽 버튼으로 클릭하세요.

        3. **Internet Protocol Version 4 (TCP/IPv4)** -> **Properties**를 클릭하세요.

        4. **IP adress**를 `192.168.1.2`로 수동 설정하세요.

        5. **Subnet mask**를 `255.255.255.0`으로 설정하세요.

            ![ipv4 properties](https://static.gl.inet.com/docs/router/en/2/troubleshooting/src/debrick/set_ip.jpg){class="glboxshadow"}

        6. **OK** 버튼을 클릭하세요.

    ??? "Windows 11"

        7. Settings를 엽니다.

        8. **Network & Internet**을 클릭합니다.

        9. **Ethernet** 탭을 클릭합니다.

            ![windows 11 ethernet](https://static.gl.inet.com/docs/router/en/4/tutorials/debrick/windwos11_ethernet.png){class="glboxshadow"}

        10. "IP assignment" 섹션에서 **Edit** 버튼을 클릭합니다.

            ![windows 11 ethernet edit](https://static.gl.inet.com/docs/router/en/4/tutorials/debrick/windows11_ethernet_ip_assignment_edit.png){class="glboxshadow"}

        11. **Manual** 옵션을 선택합니다.

            ![windows 11 ethernet edit](https://static.gl.inet.com/docs/router/en/4/tutorials/debrick/windows11_ethernet_edit_ip_settings.png){class="glboxshadow"}

        12. **IPv4 토글** 스위치를 켭니다.

        13. static **IP address**를 **192.168.1.2**로 설정합니다.

            ![windows 11 ethernet edit](https://static.gl.inet.com/docs/router/en/4/tutorials/debrick/windows11_ethernet_edit_ip_settings_2.png){class="glboxshadow"}

        14. **Subnet mask**를 **255.255.255.0**로 지정합니다.

        15. **Save** 버튼을 클릭합니다.

    ??? "macOS"

        16. 화면 왼쪽 상단의 **Apple** 아이콘을 클릭하고 **System Preferences**를 선택합니다.

            ![macos system preferences](https://static.gl.inet.com/docs/router/en/4/tutorials/debrick/macos_system_preferences.png){class="glboxshadow"}

        17. **Network**를 클릭합니다.

            ![macos system preferences network](https://static.gl.inet.com/docs/router/en/4/tutorials/debrick/macos_system_preferences_network.png){class="glboxshadow"}

        18. 왼쪽에서 **Ethernet**을 클릭한 후 **Configure IPv4** 옆의 드롭다운 상자를 클릭하고 **Manually**를 선택합니다. USB Ethernet Adapter를 사용하는 경우 Ethernet을 찾을 수 없고 USB Ethernet Adapter의 이름으로 표시될 수 있습니다.

            ![macos ip manually](https://static.gl.inet.com/docs/router/en/4/tutorials/debrick/macos_ip_manually_1.png){class="glboxshadow"}

        19. **IPv4 Address**를 `192.168.1.2`, **Subnet Mask**를 `255.255.255.0`, **Router**를 `192.168.1.1`로 입력한 후 우측 하단의 Apply 버튼을 클릭합니다.

            ![macos ip manually](https://static.gl.inet.com/docs/router/en/4/tutorials/debrick/macos_ip_manually_2.png){class="glboxshadow"}

4. **Google Chrome/Microsoft Edge를 사용하여 `http://192.168.1.1/uboot.html`을 방문하세요**

    **Mozilla/Firefox는 사용하지 마세요. 라우터가 벽돌될 수 있습니다.**

    ![gl-ar750s u-boot update page](https://static.gl.inet.com/docs/router/en/4/tutorials/debrick/u-boot_update.png){class="glboxshadow" width="700"}

5. **Choose file** 버튼을 클릭하고 다운로드한 Uboot 파일을 선택하세요.

6. **Update U-Boot** 버튼을 클릭하세요. 업그레이드 과정 중에는 전원을 끄지 마세요. 업그레이드하는 데 몇 분 정도 걸립니다.

7. 업그레이드가 성공하면 라우터가 재부팅됩니다. 이때 3단계에서 변경한 IP 설정을 되돌리고 **192.168.8.1**을 통해 웹 관리 패널에 액세스해 보세요. 정상적으로 액세스할 수 있으면 라우터가 재부팅된 것입니다.

    **참고:** 라우터에 액세스하려면 시크릿 모드를 사용하거나 브라우저 캐시와 쿠키를 삭제해야 할 수도 있습니다.

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}을 통해 연락하세요.
