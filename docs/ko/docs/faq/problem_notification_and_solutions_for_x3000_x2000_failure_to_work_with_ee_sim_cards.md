# GL-X3000/GL-XE3000/GL-X2000에서 EE SIM 카드 작동 실패에 대한 문제 알림 및 해결 방법

친애하는 GL.iNet 고객 여러분,

최근 일부 고객이 GL-X3000/GL-XE3000/GL-X2000에서 EE SIM 카드를 사용할 때 연결 실패를 겪고 있다는 것을 발견했습니다. 추가 문제 해결을 통해 특정 EE SIM 카드는 IPv4 프로토콜만 지원한다는 것을 확인했습니다. 그러나 GL.iNet 셀룰러 라우터의 기본 설정은 IPv4와 IPv6를 동시에 활성화하며, 이로 인해 이 문제가 발생합니다.

## 솔루션 및 해결 방법

1. **펌웨어 업데이트**

    이 문제를 해결하기 위해 기본 프로토콜을 IPv4로 변경하는 새 펌웨어 업데이트를 출시했습니다. IPv6가 필요한 고객은 여전히 관리 패널에서 설정을 IPv4 & IPv6로 수정할 수 있습니다.

    | 라우터 모델                  |                       |
    | :---------------------------- | :-------------------: |
    | GL-X3000 (Spitz AX)           | [펌웨어 다운로드](https://dl.gl-inet.com/router/x3000/stable)     |
    | GL-XE3000 (Puli AX)           | [펌웨어 다운로드](https://dl.gl-inet.com/router/xe3000/stable)    |
    | GL-X2000 (Spitz Plus)         | [펌웨어 다운로드](https://dl.gl-inet.com/router/x2000/stable)   |

2. **다른 모델의 해결 방법**

    다른 모델을 사용하거나 위 펌웨어를 사용하지 않으려는 경우 셀룰러 연결을 시작한 후 AT 명령을 순차적으로 실행하세요.

    ```
    AT+CGDCONT=1,"IP","User_APN"
    AT+CFUN=0
    AT+CFUN=1
    ```

    **참고**: "User_APN"은 EE SIM 카드의 경우 일반적으로 "everywhere"입니다. 라우터를 다시 시작할 때마다 이 프로세스를 반복하세요.

    ??? note "AT 명령을 실행하는 방법?"

        1. 웹 관리 패널에서 INTERNET -> Cellular 섹션으로 이동하고, 오른쪽 상단의 세 점 아이콘을 클릭한 다음 **Modem AT Command**를 선택하세요.

            ![modem AT command](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/at_command_0.jpg){class="glboxshadow"}

            이전 펌웨어의 경우 오른쪽 상단의 도구 버튼을 클릭하여 모뎀 관리 페이지로 들어가세요.

            ![modem management](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/modem_management_button.png){class="glboxshadow"}

        2. 아래와 같이 AT 명령을 찾으세요.

            ![AT command](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/at_command_1.png){class="glboxshadow"}

추가 문제가 발생하면 [support@gl-inet.com](mailto:support@gl-inet.com)으로 지원 팀에 문의하세요.

<br>

본인,

GL.iNet 기술 지원

2025년 6월 17일
