# 셀룰러를 통해 인터넷에 연결 (펌웨어 v4.7 및 이전)

**참고**: 이 가이드는 펌웨어 v4.7 및 이전 버전을 기준으로 합니다. 최신 버전은 [여기](internet_cellular.md)를 참조하세요.

---

대부분의 GL.iNet 라우터는 셀룰러 연결을 지원합니다. 이 가이드에서는 세 가지 유형의 모델을 다룹니다.

1. **내장형 4G 단일 SIM 모델**

    일부 모델은 단일 SIM 카드 슬롯이 있는 내장형 4G 모듈을 포함합니다(예: GL-XE300 (Puli)). [단일 SIM 모델 설정](#setup-for-single-sim-models)을 참조하세요.

2. **USB 모뎀 호환 모델**

    일부 모델은 USB 포트가 있으며 USB 모뎀을 통해 셀룰러 연결을 지원합니다(예: GL-AXT1800 (Slate AX)). 설정 단계는 내장형 4G 단일 SIM 모델과 유사합니다. [단일 SIM 모델 설정](#setup-for-single-sim-models)을 참조하세요.

3. **내장형 5G 듀얼 SIM 모델**

    일부 모델은 듀얼 SIM 카드 슬롯이 있는 내장형 5G 모듈을 포함합니다(예: GL-X3000 (Spitz AX)). 웹 관리 패널의 셀룰러 설정은 약간 다를 수 있습니다. [듀얼 SIM 모델 설정](#setup-for-dual-sim-models)을 참조하세요.

**참고:** 일부 SIM 카드는 처음 사용하기 전에 활성화가 필요할 수 있습니다. 호환성을 보장하기 위해 라우터에 삽입하기 전에 스마트폰에서 SIM 카드를 활성화하세요.

## 단일 SIM 모델 설정

다음 단계는 내장형 셀룰러 모뎸과 단일 SIM 카드 슬롯이 있는 모델(예: GL-XE300 Puli) 또는 외부 USB 모뎀 연결을 위한 USB 포트가 있는 모델(예: GL-AXT1800 Slate AX)에 적용됩니다.

여기서는 외부 USB 모뎀이 있는 **GL-AXT1800 (Slate AX)**을 예로 들겠습니다.

먼저 라우터의 전원을 끄는 것이 좋습니다. 미리 활성화된 SIM 카드를 USB 모뎸에 삽입한 다음 모뎸을 라우터의 USB 포트에 꽂습니다. 그런 다음 라우터의 전원을 켭니다.

라우터가 부팅된 후 USB 모뎸을 꽂으면 웹 관리 패널이 자동으로 업데이트되지 않을 수 있습니다. 이 경우 페이지를 새로고침하거나 라우터를 다시 시작하세요.

### 자동 설정

라우터의 웹 관리 패널에 로그인하고 **INTERNET** -> **Cellular**로 이동합니다.

1. 처음 액세스하면 자동으로 연결되지 않을 수 있지만 왼쪽 상단에 통신사 이름과 IMEI가 표시되어야 합니다. **Auto Setup**를 클릭하세요.

    *호환되지 않는 모뎸* 경고는 무시하세요.

    ![usb modem auto setup](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/usb_modem_auto_setup.png){class="glboxshadow"}

2. 연결을 시작합니다.

    **참고:** 일부 SIM 카드에는 특정 APN이 필요한 등 특별한 사용 제한이 있을 수 있습니다. SIM 카드가 등록되지 않으면 통신사에 문의하여 특별한 제한이 있는지 확인하세요.

    ![usb modem connecting](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/usb_modem_connecting.png){class="glboxshadow"}

3. 연결되면 페이지에 연결 성공을 나타내는 녹색 점과 함께 네트워크 세부 정보가 표시됩니다.

    ![usb modem connected](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/usb_modem_connected.png){class="glboxshadow"}

    **참고:** 초기 설정 후 USB 모뎸이 꽂힌 상태로 라우터를 다시 시작하거나 모뎸을 다시 꽂으면 USB 모뎸이 자동으로 인식되며 Auto Setup 버튼을 다시 클릭하지 않아도 네트워크 연결이 설정됩니다.

Auto Setup이 실패하면 [수동 설정](#manual-setup)을 시도하세요.

### 수동 설정

Cellular 섹션에서 **Manual Setup**를 클릭하여 현재 SIM 카드의 셀룰러 설정을 보거나 수정합니다.

**참고**: 일부 SIM 카드에는 특정 APN이 필요할 수 있습니다. SIM 카드가 등록되지 않으면 통신사에 문의하여 제한 사항이 있는지 확인하세요. 필요한 경우 라우터에서 올바른 APN을 구성하세요.

변경 사항을 적용하면 재연결이 트리거됩니다.

![4g modem manual setup](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/cellular_settings.png){class="glboxshadow"}

- **Protocol**: 셀룰러 통신 프로토콜(예: 3G, QMI 또는 QCM). 일반적으로 자동 감지되며 모뎸과 통신사 요구 사항에 맞게 변경할 수 있습니다.

- **Port**: 셀룰러 모뎸과 통신하는 데 사용되는 직렬 포트. 일반적으로 자동 감지되며 수동 조정이 필요하지 않습니다.

- **APN**: APN(Access Point Name)은 셀룰러 네트워크 연결에 필요한 게이트웨이 매개변수입니다. 라우터가 모바일 통신사가 제공하는 인터넷에 연결할 수 있도록 합니다. 기본 APN을 사용하거나 통신사가 제공하는 사용자 정의 APN을 설정할 수 있습니다.

- **PIN**: SIM 카드가 PIN 코드로 보호되어 있는 경우 여기에 입력하세요. PIN이 설정되지 않은 경우 이 필드는 선택 사항입니다.

- **TTL**: TTL(Time To Live)은 패킷이 네트워크에서 존재할 수 있는 최대 시간을 정의합니다. 기본적으로 라우터는 클라이언트 장치에서 들어오는 패킷의 TTL을 1씩 줄인 후 포워딩합니다. 재정의해야 하는 경우 여기에 고정 값을 설정할 수 있습니다. TTL 설정은 IPv4에만 유효합니다.

- **Service**: 모뎸이 사용할 네트워크 기술을 정의하는 셀룰러 서비스 유형을 선택하세요.

- **Dial Number**: 통신사가 제공하는 전화 걸기 번호를 입력하세요. 대부분의 최신 네트워크에서는 미리 구성되어 있으며 비워둘 수 있습니다.

- **Authentication**: 통신사가 요구하는 인증 방법(예: NONE, PAP, CHAP)을 선택하세요. 자격 증명이 필요하지 않은 경우 일반적으로 NONE으로 설정됩니다.

### 호환 모뎸

이전에 테스트한 지원 모뎸 목록입니다.

| Model                                  | 3G/4G | Tested | Tested by       | Comments* |
| -------------------------------------- | ----- | ------ | --------------- | --------- |
| Quectel EC20-E, EC20-A, EC20-C         | 4G    | Yes    | GL.iNet         |           |
| Quectel EC25-E, EC25-A, EC25-V, EC25-C | 4G    | Yes    | GL.iNet         |           |
| Quectel EC200A series                  | 4G    | Yes    | akw2312         | Host-less |
| Quectel EP06-E, EP06-A                 | 4G    | Yes    | akw2312         |           |
| Quectel EM060K-GL, EM120K-GL           | 4G    | Yes    | akw2312         |           |
| Quectel EM120R-GL, EM160R-GL           | 4G    | Yes    | akw2312         |           |
| Quectel RM520N-GL                      | 5G    | Yes    | akw2312         |           |
| Quectel UC20-E                         | 3G    | Yes    | GL.iNet         |           |
| ZTE ME909s-821                         | 4G    | Yes    | GL.iNet         |           |
| Huawei E1550                           | 3G    | Yes    | GL.iNet         |           |
| Huawei E3276                           | 4G    | Yes    | GL.iNet         |           |
| TP-Link MA260                          | 3G    | Yes    | GL.iNet         |           |
| ZTE M823                               | 4G    | Yes    | Arnas Risqianto |           |
| ZTE MF190                              | 3G    | Yes    | Arnas Risqianto |           |
| Huawei E3372                           | 4G    | Yes    | anonymous       |           |
| Pantech UML290VW (Verizon)             | 4G    | Yes    | GL.iNet/steven  | QMI       |
| Pantech UML295 (Verizon)               | 4G    | Yes    | GL.iNet/steven  | Host-less |
| Novatel USB551L (Verizon)              | 4G    | Yes    | GL.iNet/steven  | QMI       |
| Verizon U620L (Verizon)                | 4G    | Yes    | anonymous       | Host-less |
| Huawei E3372h-320 (Ukraine)            | 4G    | Yes    | anonymous       | Host-less |

- **QMI**: 이 모뎸은 QMI 모드를 지원합니다. 프로토콜로 QMI를 선택하고 직렬 포트로 **/dev/cdc-wdm0**를 선택하세요.

- **Host-less**: 이 모뎸은 테더링 모드를 지원합니다. Cellular 인터페이스 대신 라우터의 Tethering 인터페이스를 통해 연결을 관리하세요.

## 듀얼 SIM 모델 설정

다음 단계는 듀얼 SIM 카드를 지원하는 내장형 셀룰러 모뎸이 있는 모델에 적용됩니다. 웹 관리 패널은 단일 SIM 모델과 약간 다를 수 있습니다.

여기서는 **GL-X3000 (Spitz AX)**을 예로 들겠습니다. Dual SIM, Single Standby를 지원합니다. 즉, 셀룰러 액세스를 위해 두 개의 SIM 카드를 장착할 수 있지만 한 번에 하나의 SIM 카드만 활성화할 수 있습니다. 두 SIM 카드 간에 수동으로 전환할 수 있습니다.

먼저 라우터의 전원을 끈 다음 미리 활성화된 SIM 카드를 슬롯에 삽입하고 전원을 켭니다. 라우터가 부팅된 후 SIM 카드를 삽입하면 웹 관리 패널이 자동으로 업데이트되지 않을 수 있습니다. 이 경우 페이지를 새로고침하거나 라우터를 다시 시작하세요.

### 자동 설정

라우터의 웹 관리 패널에 로그인하고 **INTERNET** -> **Cellular**로 이동합니다.

1. SIM 카드가 삽입되지 않은 경우 페이지는 다음과 같이 표시됩니다.

    ![dual-sim, no sim](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/dual_sim/no_sim.png){class="glboxshadow"}

2. SIM 카드가 삽입되면 라우터가 자동으로 연결을 시작합니다.

    연결에 성공하면 페이지는 다음과 같이 표시됩니다.

    ![dual-sim, 5g sim](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/dual_sim/5g_sim.png){class="glboxshadow"}

자동으로 연결되지 않으면 **Auto Setup**를 클릭하고 라우터가 연결될 때까지 기다리거나 **Manual Setup**을 시도하세요.

### 수동 설정

Cellular 섹션에서 **Manual Setup**를 클릭하여 Cellular Settings로 들어갑니다.

![cellular settings](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/dual_sim/manual_setup/cellular_settings.png){class="glboxshadow gl-90-desktop"}

현재 SIM 카드의 셀룰러 설정을 보거나 수정할 수 있습니다. 사전 구성된 일부 프로필도 저장하며 "Saved Settings"에 구성을 수동으로 추가할 수 있습니다.

### SIM 카드 슬롯 설정

Cellular 섹션에서 **Current SIM Card**를 클릭합니다.

![dual-sim, current sim card](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/dual_sim/current_sim_card.png){class="glboxshadow"}

**SIM Card Slot Settings**으로 들어갑니다.

![dual-sim, sim card slot settings](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/dual_sim/sim_card_slot_settings.png){class="glboxshadow"}

두 SIM 카드가 모두 삽입된 경우 **Auto Switch**를 활성화할 수 있습니다.

![dual-sim, auto switch](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/dual_sim/auto_switch.png){class="glboxshadow"}

- **Auto Switch**: SIM 1과 SIM 2 간의 자동 전환을 활성화합니다. SIM Auto Switch의 네트워크 감지 방법은 Multi-WAN 페이지에서 구성한 방법과 동일합니다.

- **Preferred SIM Card Slot**: 선호 SIM 카드를 SIM 1 또는 SIM 2로 설정하세요.

- **Failover Interval**: 5분에서 24시간까지 값을 사용할 수 있습니다.

    장애 조치 후에도 인터넷 연결을 사용할 수 없으면 장치가 선호 SIM 슬롯으로 다시 전환하고 이 간격 동안 기다린 후 장애 조치를 재시도합니다.

    이 옵션은 선호 SIM 카드와 백업 SIM 카드 모두 신호가 없는 경우에 적용됩니다. 장치는 SIM 카드 간에 전환하여 둘 중 하나가 유효한 신호를 얻을 때까지 전환합니다.

    ![failover interval](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/sim_failover_interval.png){class="glboxshadow"}

- **Checking Preferred Slot Status Scheduled**

    활성화하면 장치는 구성된 시간에 매일 선호 SIM 슬롯을 확인하고 선호 SIM이 인터넷 액세스를 다시 얻으면 전환을 시도합니다.

    이렇게 하면 백업 SIM이 과도한 데이터를 소비하는 것을 방지할 수 있습니다. 선호 SIM에 여전히 신호가 없으면 장치는 백업 SIM을 계속 사용합니다.

    ![checking preferred slot status scheduled](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/check_preferred_slot_status.png){class="glboxshadow"}

**참고**: Auto Switch 기능은 즉시 다른 SIM 카드로 전환하지 않습니다. 첫째, 장치가 현재 SIM이 인터넷에 액세스할 수 없다는 것을 확인하는 데 시간이 필요합니다. 둘째, 다른 SIM은 대기 모드가 아니며 활성화하는 데 시간이 필요합니다.

## 트래픽 통계

Cellular 섹션에서 **Traffic Statistics**를 클릭합니다.

![traffic statistics](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/dual_sim/traffic_statistics_option.png){class="glboxshadow gl-90-desktop"}

트래픽 통계 페이지로 들어갑니다.

![traffic statistics](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/dual_sim/traffic_statistics.png){class="glboxshadow gl-90-desktop"}

## SMS

[SMS 자습서](sms.md)를 참조하세요.

## SMS 전달

[SMS 전달 자습서](../tutorials/sms_forwarding.md)를 참조하세요.

## 모뎸 관리

Cellular 섹션에서 오른쪽 상단의 **Tool** 버튼을 클릭하여 Modem Management 페이지로 들어갑니다.

![modem management button](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/modem_management_button.png){class="glboxshadow"}

**Modem Info**와 **AT Command**의 두 섹션이 포함되어 있습니다.

![modem management](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/modem_management.png){class="glboxshadow"}

AT 명령은 셀룰러 모뎸과 통신하는 데 사용되는 표준 명령어입니다.

Shortcut이 **Manual command**로 설정되어 있으면 AT Command 필드에 원하는 명령을 입력하여 모뎸 상태를 확인하세요.

Shortcut 드롭다운을 클릭하여 **사전 설정 명령어** 목록에서 선택할 수도 있습니다.

![shortcut](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/at_command_2.png){class="glboxshadow"}

사전 설정으로 사용할 수 있는 명령은 다음과 같습니다.

* Request IMEI
* Request QCCID
* Request IMSI
* Check Signal Quality
* Reset modem
* Operator Names
* Request SIM card status

예로서 여기서는 "Request IMEI" 바로가기를 선택했습니다. "Send"를 클릭하면 아래와 같은 결과를 얻을 수 있습니다.

![shortcut example](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/at_command_3.png){class="glboxshadow"}

## 통신사 프로필

동일하거나 다른 통신사에 대해 다른 프로필을 저장할 수 있습니다.

Cellular 섹션에서 오른쪽 상단의 **Profile** 버튼을 클릭하여 프로필을 관리합니다.

![manageprofile](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/carrier_profile/manage_profile.jpg){class="glboxshadow"}

새 프로필을 추가하거나 현재 프로필을 저장하세요.

![addprofile](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/carrier_profile/add_profile.jpg){class="glboxshadow"}

통신사 요구 사항에 따라 자신만의 프로필을 만드세요.

![createprofile](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/carrier_profile/create_profile.jpg){class="glboxshadow"}

다음에 저장된 프로필을 선택할 수 있습니다.

![selectprofile](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/carrier_profile/select_profile.jpg){class="glboxshadow"}

필요한 프로필을 선택하세요.

![chooseprofile](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/carrier_profile/choose_profile.jpg){class="glboxshadow"}

## 기지국 고정

이 기능은 GL-X3000, GL-XE3000 및 GL-X2000(펌웨어 ver.4.7 이상)에서만 사용할 수 있습니다.

고품질 신호를 받고 안정적인 셀룰러 연결을 보장하려면 기지국 고정을 시도해 볼 수 있습니다.

**참고:** 고정된 기지국은 통신사와 장치가 지원하는 주파수 대역과 일치해야 합니다. 그렇지 않으면 연결이 실패할 수 있습니다.

Cellular 섹션에서 오른쪽 상단의 **Tower** 아이콘을 클릭합니다.

![signal_tower_lock](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/signal_tower_lock_1.jpg){class="glboxshadow"}

사용 가능한 기지국이 표시됩니다.

![signal_tower_lock1](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/signal_tower_lock_2.jpg){class="glboxshadow"}

기지국을 클릭하여 세부 정보를 보고 고정하세요.

![signal_tower_lock2](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/signal_tower_lock_3.jpg){class="glboxshadow"}

기지국 상태(예: Locked/Unlocked)가 상단에 표시됩니다.

![signal_tower_lock3](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/signal_tower_lock_4.jpg){class="glboxshadow"}

**참고**:

1. Cellular 인터페이스가 활성화되어 있으면 장치가 모든 기지국을 스캔하지 못할 수 있습니다.

2. 고정된 기지국이 셀룰러 설정의 대역 마스킹 또는 APN 매개변수와 일치하지 않으면 라우터가 셀룰러 네트워크에 연결할 수 없습니다.

3. 기지국을 고정한 후 라우터를 다른 위치로 이동하면 다시 부팅한 후에도 고정된 기지국에 다시 연결을 시도합니다. 이렇게 하면 라우터가 새 위치에서 자동으로 셀룰러 네트워크에 연결되지 않을 수 있습니다. 이 경우 현재 기지국 고정을 해제하거나 새 기지국에 수동으로 고정해야 합니다.

## 과거 신호 기록

Cellular 섹션에서 오른쪽 상단의 **Signal** 아이콘을 클릭하여 과거 신호 강도를 확인하세요.

![historical_signal_record](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/historical_signal_record_1.jpg){class="glboxshadow"}

이렇게 하면 셀룰러 연결 품질을 파악하는 데 도움이 됩니다. 신호가 약하면 더 나은 신호를 위해 기지국을 전환해 보세요.

다른 시간 프레임을 선택하여 셀룰러 신호 강도 기록을 볼 수 있습니다.

![historical_signal_record1](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/historical_signal_record_2.jpg){class="glboxshadow"}

## 대역 마스킹

Cellular 섹션에서 **View More**를 클릭하고 **Cells Info**를 선택하여 셀 세부 정보를 확인하세요.

사용 중인 현재 대역과 신호 상태를 볼 수 있습니다.

![cellinfo](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/band_masking/cell_info.jpg){class="glboxshadow"}

신호가 약하면 Band Masking을 활성화하여 특정 대역을 차단할 수 있습니다. 또는 신호가 좋으면 라우터가 특정 셀룰러 대역만 사용하도록 할 수 있습니다.

**Manual Setup**를 클릭하여 Cellular Settings 페이지로 들어간 다음 **Band Masking**을 활성화합니다.

![bandmasking](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/band_masking/band_masking.jpg){class="glboxshadow"}

**Masking Mode**(Block 또는 Open)를 선택한 다음 LTE Bands, 5G NSA Bands 및 5G SA Bands를 선택하세요.

## 문제 해결

셀룰러 연결 설정에 실패한 경우 아래 오류 메시지를 클릭하여 관련 솔루션을 확인하세요.

??? note "SIM 카드 없음 / SIM 카드가 감지되지 않았습니다"

    1. 페이지를 새로고침하고 몇 분 기다려 SIM 카드가 감지되는지 확인하세요.

    2. SIM 카드가 올바르게 설치되어 있는지 확인하세요. SIM 카드의 홈을 카드 슬롯의 해당 마크와 정렬하여 올바른 삽입 방향을 확인하세요.

    3. 라우터의 전원을 끄고 SIM 카드를 제거한 다음 다시 삽입한 후 라우터의 전원을 다시 켜세요.

    4. 가능한 경우 다른 SIM 카드를 사용해 보세요.

    문제가 지속되면 로그를 다운로드하여 [support@gl-inet.com](mailto:support@gl-inet.com)으로 보내세요.

??? note "SIM 카드가 등록되지 않음 / 인터페이스는 연결되었지만 인터넷에 액세스할 수 없음"

    1. 페이지를 새로고침하고 몇 분 기다려 오류가 사라지는지 확인하세요.

    2. **Disconnect**/**Abort**를 클릭한 다음 **Connect**를 클릭하여 다시 연결해 보세요.

    3. 라우터를 다시 시작하세요.

    4. SIM 카드 상태를 확인하고 활성화되어 있는지 확인하세요. 스마트폰에 SIM 카드를 삽입하여 활성화된 모바일 데이터 플랜으로 정상적으로 인터넷에 액세스할 수 있는지 확인하거나 네트워크 통신사에 문의하여 확인하세요.

    5. 일부 네트워크 통신사는 네트워크 연결에 3G 프로토콜을 요구할 수 있습니다. **Manual Setup** -> **Cellular Settings** -> **Protocol**로 이동하여 **3G**를 선택한 다음 **Apply**를 클릭하세요.

        ![manual setup, sim protocol](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/cellular_settings.png){class="glboxshadow"}

        장치가 자동으로 다시 연결됩니다. 연결이 성공적인지 확인하기 위해 몇 분 기다리세요.

    6. 일부 SIM 카드에는 특정 APN이 필요한 등 특별한 사용 제한이 있을 수 있습니다. SIM 카드가 등록되지 않으면 통신사에 문의하여 제한 사항이 있는지 확인하세요.

        필요한 경우 **Manual Setup** -> **Cellular Settings** -> **APN**로 이동하여 라우터에서 올바른 APN을 구성한 다음 **Apply**를 클릭하세요.

    7. **View More**를 클릭하고 **Cells Info**를 선택하여 셀룰러 신호 강도를 확인하세요. 신호가 약하면 안테나가 올바르게 설치되어 있는지 확인하세요. 더 나은 신호 수신을 위해 라우터를 열리고 장애물이 없는 곳으로 이동하세요.

    8. **Band Masking** 또는 **Lock Tower**가 활성화되어 있는지 확인하세요. 활성화된 경우 기능을 비활성화하고 다시 연결해 보세요.

    문제가 지속되면 로그를 다운로드하여 [support@gl-inet.com](mailto:support@gl-inet.com)으로 보내세요.

## IoT 인증

### AT&T 인증

링크 [att device certification](https://iotdevices.att.com/certified-devices.aspx#)를 클릭하고 장치 이름을 입력하면 찾을 수 있습니다.

![bandmasking](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/certification/at&t_certification.png){class="glboxshadow"}

![bandmasking](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/certification/at&t_certification_2.png){class="glboxshadow"}

### T-Mobile 인증

링크 [t-mobile device certification](https://www.t-mobile.com/business/solutions/iot/device-certification)를 클릭하고 **Filter**에서 5G를 선택하면 찾을 수 있습니다.

![bandmasking](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/certification/t-mobile_certification.png){class="glboxshadow"}


---

관련 문서

- [인터넷 페이지](internet.md)
- [각 인터넷 액세스 방법의 우선 순위를 설정하는 방법](multi-wan.md)
- [여러 인터넷 액세스 방법을 동시에 사용할 때 로드 밸런스를 설정하는 방법](multi-wan.md)

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}을 통해 연락하세요.
