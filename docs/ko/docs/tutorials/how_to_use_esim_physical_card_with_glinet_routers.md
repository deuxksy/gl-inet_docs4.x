# GL.iNet 라우터에서 eSIM 물리적 카드 사용 방법

이 가이드는 GL.iNet 온라인 스토어에서 구매한 eSIM 물리적 카드를 GL.iNet 라우터와 함께 사용하는 방법을 안내합니다.

![eSIM Physical Card](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_the_simpoyo_esim_physical_card_with_android_devices/simpoyo-esim-physical-card.png){class="glboxshadow"}

## 기능

eSIM 물리적 카드의 주요 기능은 다음과 같습니다:

- 안정적이고 빠른 연결을 위한 4G 및 5G 네트워크 지원
- eSIM 프로필을 쉽게 추가, 제거 또는 활성화하여 관리
- 전 세계 대부분의 eSIM 스토어에서 언제든지 선호하는 데이터 패키지를 선택하고 구매
- 대부분의 글로벌 eSIM 스토어의 eSIM 프로필과 호환
- 개인 정보를 제공하지 않고 온라인으로 eSIM 프로필을 구매하여 프라이버시 유출 위험 감소
- 미국과 유럽용 1GB 무료 데이터, 글로벌 데이터 100MB가 포함된 시드 프로필 제공, 활성화 날짜로부터 1년간 유효
- 선택된 GL.iNet 장치와 호환

## 지원되는 모델

| 라우터 모델                   | 지원   |
| :----------------------------- | :-------: |
| GL-X2000 (Spitz Plus)          | √         |
| GL-X3000 (Spitz AX)            | √         |
| GL-XE3000 (Puli AX)            | √         |
| GL-E750V2 (Mudi V2)            | √         |
| GL-E750 (Mudi)                 | ※        |
| GL-XE300 (Puli)                | ※        |
| GL-X750 (Spitz)                | ※        |
| GL-X300B (Collie)              | ※        |
| GL-E750V2 vSIM                 | X         |
| GL-E5800 (Mudi 7)              | X         |

**※ 표시된 모델의 경우**:

1. 현재 안정 펌웨어는 eSIM을 지원하지 않습니다. eSIM 기능을 사용하려면 eSIM 지원 펌웨어를 설치해야 합니다. 자세한 지침은 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 클릭하세요.

2. EP06-A 모듈이 장착된 ※ 모델을 사용하는 경우 Qualcomm 소프트웨어가 특정 AT 명령을 지원하지 않으므로 eSIM이 지원되지 않습니다.

3. EP06-E 모듈이 장착된 ※ 모델을 사용하는 경우 eSIM 기능을 활성화하려면 [이 링크](https://forum.gl-inet.com/t/upgrade-ep06-e-firmware-to-support-esim/48907){target="_blank"}를 참조하여 모듈 펌웨어를 업그레이드하고 eSIM 지원 펌웨어를 설치하세요.

**X 표시된 모델의 경우**:

1. GL-E750V2 vSIM은 eSIM 기능을 지원하지 않습니다.

2. GL-E5800 (Mudi 7)에는 내장 eSIM이 있습니다. 따라서 eSIM 물리적 카드는 Mudi 7에서 eSIM 기능 없이 일반 SIM 카드로 인식됩니다.

## eSIM 물리적 카드 설정

eSIM 물리적 카드를 처음 사용하는 경우 이 설정 비디오를 시청하거나 아래 단계에 따라 GL.iNet 라우터에 설정하세요.

<iframe width="560" height="315" src="https://www.youtube.com/embed/SCex_vuvgNQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

**1단계:** eSIM 물리적 카드를 라우터에 삽입하세요. 자세한 지침은 아래 이미지를 참조하세요.

![E750V2](https://static.gl.inet.com/docs/router/en/4/tutorials/how_to_set_up_the_esim/e750v2-sim-card.jpg){class="glboxshadow"}

![X3000](https://static.gl.inet.com/docs/router/en/4/tutorials/how_to_set_up_the_esim/x3000-sim-card.jpg){class="glboxshadow"}

![XE3000](https://static.gl.inet.com/docs/router/en/4/tutorials/how_to_set_up_the_esim/xe3000-sim-card.jpg){class="glboxshadow"}

**2단계:** 브라우저를 열고 주소창에 "192.168.8.1"을 입력하여 GL.iNet 관리 패널에 로그인하세요.

![log in to the GL.iNet Admin Panel](https://static.gl.inet.com/docs/router/en/4/tutorials/how_to_set_up_the_esim/login-admin-panel.jpg){class="glboxshadow"}

**3단계:** 장치를 인터넷에 연결하세요.

**INTERNET**으로 이동한 다음 **Connect**(또는 하위 펌웨어 버전의 **Auto Setup**)를 클릭하여 Cellular를 통해 인터넷에 연결하세요.

*이 eSIM 물리적 카드에는 미국과 유럽용 1GB 무료 데이터와 글로벌 데이터 100MB가 포함된 시드 프로필이 제공되며, 활성화 날짜로부터 1년간 유효합니다. 이 데이터는 eSIM 프로필을 구매하고 다운로드하는 용도로만 제공되며 일반 인터넷 액세스용이 아닙니다.*

![initial setup connect](https://static.gl.inet.com/docs/router/en/4/tutorials/how_to_set_up_the_esim/initial-setup-connect.jpg){class="glboxshadow"}

인터넷 연결에 성공하면 화면이 다음과 같이 표시됩니다.

![initial setup connected](https://static.gl.inet.com/docs/router/en/4/tutorials/how_to_set_up_the_esim/initial-setup-connected.jpg){class="glboxshadow"}

## eSIM 프로필 관리

**1단계:** GL.iNet 장치에 최신 펌웨어가 설치되어 있는지 확인하세요.

Version이 4.0 이상이고 Firmware Type 번호가 0319 이상인지 확인하세요.

![auto setup successfully](https://static.gl.inet.com/docs/router/en/4/tutorials/how_to_set_up_the_esim/latest-firmware.png){class="glboxshadow"}

펌웨어가 최신이 **아닌 경우** 자동으로 또는 수동으로 업그레이드할 수 있습니다.

<옵션 1>: 온라인 펌웨어 업그레이드

1. 장치가 인터넷에 연결되어 있는지 확인하세요.

2. 웹 관리 패널에서 **SYSTEM** > **Upgrade** > **Online Upgrade**로 이동한 다음 **Install** 버튼을 클릭하여 최신 펌웨어로 자동 업데이트하세요.

    ![online upgrade](https://static.gl.inet.com/docs/router/en/4/tutorials/how_to_set_up_the_esim/online-upgrade.png){class="glboxshadow"}

<옵션 2>: 수동 펌웨어 업데이트

1. [여기](https://dl.gl-inet.com/){target="_blank"}에서 eSIM 기능을 지원하는 해당 모델의 펌웨어를 다운로드하세요.

2. 웹 관리 패널에서 **SYSTEM** > **Upgrade** > **Local Upgrade**로 이동하세요. 펌웨어 파일을 선택하거나 지정된 영역으로 드래그하여 최신 버전으로 업그레이드하세요.

    ![local upgrade](https://static.gl.inet.com/docs/router/en/4/tutorials/how_to_set_up_the_esim/local-upgrade.png){class="glboxshadow"}

!!! Note

    1. Mudi (GL-E750), Puli (GL-XE300), Spitz (GL-X750)와 같은 일부 모델은 Quectel EP06-A 모듈이 장착된 경우 Qualcomm 소프트웨어가 특정 AT 명령을 지원하지 않으므로 eSIM을 지원하지 않습니다.

    2. EP06-E 모듈이 장착된 경우 eSIM 기능을 위해 [이 링크](https://forum.gl-inet.com/t/48907){target="_blank"}를 참조하여 모듈을 최신 소프트웨어로 업그레이드하세요.

**2단계:** eSIM 관리로 이동하세요.

펌웨어 업데이트 후 장치가 재부팅될 때까지 기다린 다음 GL.iNet 관리 패널에 로그인하세요.

**APPLICATIONS** > **eSIM Management**로 이동하세요. 여기서 eSIM 현재 상태를 볼 수 있습니다.

![eSIM manage](https://static.gl.inet.com/docs/router/en/4/tutorials/how_to_set_up_the_esim/esim-manage-status.jpg){class="glboxshadow"}

한 번에 하나의 eSIM 프로필만 활성화할 수 있습니다. 녹색 점은 선택한 eSIM 프로필이 현재 활성화되어 있음을 나타냅니다.

## eSIM 관리 가이드

![eSIM manage](https://static.gl.inet.com/docs/router/en/4/tutorials/how_to_set_up_the_esim/esim-management-interface-guide.jpg){class="glboxshadow"}

**A. 현재 eSIM 상태:**

이 섹션에는 eSIM의 기본 정보와 현재 활성화된 프로필의 세부 정보가 표시됩니다.

- **EID:** eUICC(eSIM 칩)의 전역 고유 식별자로 식별 및 프로필 제어에 사용됩니다.
- **ICCID:** 현재 활성화된 eSIM 프로필의 통합 회로 카드 식별자입니다.
- **IMSI:** 현재 활성화된 eSIM 프로필의 국제 모바일 가입자 식별자입니다.
- **eSIM OS Version:** eUICC의 운영 체제 버전으로 호환성 및 기능을 정의합니다.
- **eSIM Storage (remain/total):** eSIM 프로필 저장을 위한 eUICC의 사용 가능 및 총 저장 용량입니다.
- **eSIM Profile Number:** 현재 eUICC에 저장된 eSIM 프로필 수입니다.

**B. 시드 프로필:**

이 섹션에는 시드 프로필에 대한 세부 정보가 표시됩니다. 시드 프로필에는 미국과 유럽용 1GB 무료 데이터와 글로벌 데이터 100MB가 포함되어 있으며 활성화 날짜로부터 1년간 유효합니다. 이 데이터를 사용하여 전 세계적으로 다른 프로필을 다운로드할 수 있습니다. 시드 프로필의 사용량(남은 데이터, 총 데이터, 만료 날짜 포함)도 모니터링할 수 있습니다.

**C. 일반 프로필:**

이 섹션에는 일반 프로필에 대한 정보가 표시됩니다. 온라인 스토어에서 eSIM 프로필을 구매하고 **Add eSIM Profile (QR Code Install)** 기능을 사용하여 eSIM QR 코드를 업로드하면 업로드 완료 후 프로필이 여기에 표시됩니다.

**D. eSIM 프로필 추가 (QR 코드 설치):**

이것은 eSIM 프로필을 업로드하고 설치하는 핵심 기능입니다. 온라인 스토어에서 eSIM 프로필을 구매하면 QR 코드를 받게 됩니다. 이 버튼을 클릭하여 QR 코드를 업로드하면 eSIM 프로필을 다운로드하여 라우터에 설치합니다.

**E. 지원용 로그 내보내기:**

이 섹션에서 eSIM 작업과 관련된 모든 로그를 볼 수 있습니다. 문제가 발생하고 기술 지원이 필요한 경우 이러한 로그를 내보내고 support@gl-inet.com 이메일을 통해 지원팀과 공유하세요.

**F. 충전:**

GL.iNet에서 제공하는 무료 및 사전 로드된 데이터를 모두 사용했거나 데이터가 만료되어 서비스를 계속 사용하려는 경우 **Top-up** 버튼을 클릭하여 QR 코드를 스캔하고 추가 데이터를 구매하세요.

**G. 추천 eSIM 프로필 스토어:**

GL.iNet은 편의를 위해 두 개의 파트너 eSIM 스토어인 EIOTCLUB과 Tuge를 추천합니다. QR 코드를 스캔하거나 링크([EIOTCLUB eSIM 스토어](https://www.eiotclub.com/pages/esim){target="_blank"} 또는 [Tuge eSIM 스토어](https://esim_store.gl-inet.com/){target="_blank"})를 클릭하여 필요에 따라 구매할 수 있습니다. 다른 타사 제공업체에서 eSIM 패키지를 구매할 수도 있습니다.

**H. 작업:**

이 섹션에서 eSIM 프로필을 쉽게 관리할 수 있습니다. 활성화, 전환 또는 삭제가 포함됩니다.

## eSIM 시드 프로필 충전

초기 설정 또는 eSIM 프로필 구매를 위해 GL.iNet은 사전 로드된 데이터를 제공합니다: 글로벌용 100MB와 유럽 및 미국용 1GB입니다. 이 요금제는 더 비싸게 설계되었으며 인터넷 액세스 없는 위치에 도착했을 때 새 eSIM 프로필을 다운로드해야 하는 상황을 위해 설계되었습니다.

eSIM 시드 프로필을 충전하려면 **Top-up** 버튼을 클릭하여 QR 코드를 스캔하고 지침을 따르세요.

![eSIM manage](https://static.gl.inet.com/docs/router/en/4/tutorials/how_to_set_up_the_esim/esim_top-up.jpg){class="glboxshadow"}

## eSIM 프로필 구매 및 설치

라우터 설정 후 다음 단계에 따라 eSIM 프로필을 구매하고 활성화하세요.

**1단계:** eSIM 스토어에서 eSIM 프로필을 구매하세요.

<옵션 1>: 추천 스토어인 [EIOTCLUB eSIM 스토어](https://www.eiotclub.com/pages/esim){target="_blank"} 또는 [Tuge eSIM 스토어](https://esim_store.gl-inet.com/){target="_blank"}에서 eSIM 프로필을 구매하세요. 직접 스토어 링크는 아래 이미지를 참조하세요.


*이 두 스토어에서 구매한 모든 eSIM 프로필 패키지는 우리 라우터와 완전히 호환됩니다. 질문이 있으시면 support@gl-inet.com으로 지원팀에 문의하세요.*

![eSIM recommend store](https://static.gl.inet.com/docs/router/en/4/tutorials/how_to_set_up_the_esim/esim-profile-recommend-store-1.jpg){class="glboxshadow"}

![eSIM recommend store](https://static.gl.inet.com/docs/router/en/4/tutorials/how_to_set_up_the_esim/esim-profile-recommend-store-2.jpg){class="glboxshadow"}

<옵션 2>: [이 링크](https://forum.gl-inet.com/t/carriers-supported-by-gl-inet-physical-esim/54164){target="_blank"}를 참조하여 GL.iNet에서 테스트한 스토어 목록을 가져오세요. 이 스토어의 모든 패키지가 GL.iNet 라우터와 완전히 호환된다는 보장은 없습니다.

*GL.iNet은 이 스토어와 파트너십을 맺고 있지 않으므로 이 패키지와 관련된 판매 지원 또는 환불을 도와드릴 수 없습니다.*

<옵션 3>: 선택한 다른 타사 제공업체에서 eSIM 프로필을 구매하세요.

**2단계**: eSIM 프로필 설치

eSIM 프로필을 구매하면 QR 코드를 받게 됩니다. 이 QR 코드를 컴퓨터에 저장하세요. 그런 다음 **Add eSIM Profile (QR Code Install)** 버튼을 클릭하여 구매한 eSIM 프로필을 업로드하고 설치하세요.

![add eSIM profile](https://static.gl.inet.com/docs/router/en/4/tutorials/how_to_set_up_the_esim/add-esim-profile-1.jpg){class="glboxshadow"}

![add eSIM profile](https://static.gl.inet.com/docs/router/en/4/tutorials/how_to_set_up_the_esim/add-esim-profile-2.jpg){class="glboxshadow"}

**참고:** 위 이미지의 녹색 화살표와 같이 올바른 형식의 QR 코드는 **LPA:**로 시작하는 활성화 코드를 표시합니다.

*그러나 일부 비표준 QR 코드는 LPA 접두사 없이 원시 활성화 코드만 생성할 수 있습니다.
이 경우 Download & Install 버튼을 클릭하기 전에 코드 앞에 "LPA:"를 수동으로 추가하세요.*

**3단계:** 새 프로필 활성화

QR 코드를 성공적으로 업로드하면 **Normal Profile** 아래에 새 eSIM 프로필이 표시됩니다. **Enable**를 클릭하여 새 eSIM 프로필을 활성화하세요.

![enable your new profile](https://static.gl.inet.com/docs/router/en/4/tutorials/how_to_set_up_the_esim/enable-your-new-profile.jpg){class="glboxshadow"}

**4단계:** 새 eSIM 프로필 적용 및 인터넷 연결

eSIM 프로필을 활성화한 후 **INTERNET**로 이동하고 **Connect**를 클릭하여 eSIM 프로필을 적용하고 인터넷에 연결하세요.

![connect to internet](https://static.gl.inet.com/docs/router/en/4/tutorials/how_to_set_up_the_esim/enable-your-new-profile-connect.jpg){class="glboxshadow"}

*참고: 일부 eSIM 프로필은 APN, PIN 또는 TTL과 같은 추가 설정이 필요할 수 있습니다. 필요한 경우 **Manual Setup** 또는 **SIM Card Settings**를 클릭하여 이 설정을 구성하세요. 경우에 따라 인터넷 연결을 설정하려면 장치를 재부팅해야 할 수도 있습니다.*

eSIM 프로필이 성공적으로 설정되면 화면이 다음과 같이 표시됩니다:

![eSIM profile is successfully set up](https://static.gl.inet.com/docs/router/en/4/tutorials/how_to_set_up_the_esim/enable-your-new-profile-successfully.jpg){class="glboxshadow"}

**5단계:** eSIM 프로필 쉽게 전환 또는 삭제

활성화하려는 프로필 옆의 **Enable**를 클릭하여 eSIM 프로필 간에 쉽게 전환할 수 있습니다. eSIM 프로필을 제거하려면 **Delete**를 클릭하세요.

![eSIM profile is successfully set up](https://static.gl.inet.com/docs/router/en/4/tutorials/how_to_set_up_the_esim/switch-or-delete-esim-profile.jpg){class="glboxshadow"}

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}을 통해 연락하세요.
