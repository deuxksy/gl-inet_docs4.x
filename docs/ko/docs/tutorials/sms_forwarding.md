# SMS 전달

GL.iNet 셀룰러 라우터는 SMS 전달을 지원하여 수신 메시지를 지정된 수신자에게 자동으로 푸시할 수 있습니다.

**참고**: 이 기능은 원래 4G LTE/5G NR 모듈이 장착된 GL.iNet 셀룰러 라우터에서만 작동하며 다른 모듈이나 기타 USB 모듈에서는 지원되지 않습니다.

## 지원되는 모델

??? "지원되는 모델"
    - GL-E5800 (Mudi 7)
    - GL-X2000 (Spitz Plus)
    - GL-X3000 (Spitz AX)
    - GL-XE3000 (Puli AX)
    - GL-E750/E750V2 (Mudi)
    - GL-X750/GL-X750V2 (Spitz)
    - GL-XE300 (Puli)
    - GL-X300B (Collie)

??? "지원되지 않는 모델"
    - GL-MT5000 (Brume 3)
    - GL-MT3600BE (Beryl 7)
    - GL-BE6500 (Flint 3e)
    - GL-BE9300 (Flint 3)
    - GL-BE3600 (Slate 7)
    - GL-B3000 (Marble)
    - GL-MT6000 (Flint2)
    - GL-AX1800 (Flint)
    - GL-MT2500/GL-MT2500A (Brume 2)
    - GL-MT3000 (Beryl AX)
    - GL-AXT1800 (Slate AX)
    - GL-SFT1200 (Opal)
    - GL-A1300 (Slate Plus)
    - GL-MT1300 (Beryl)
    - GL-AR750S (Slate)
    - GL-MT300N-V2 (Mango)
    - GL-AR300M Series (Shadow)
    - GL-B1300 (Convexa-B)
    - GL-AP1300 (Cirrus)

## 설정

GL-XE3000 (Puli AX)를 예로 사용합니다.

웹 관리 패널 좌측에서 **INTERNET** -> **Cellular** 섹션으로 이동하세요.

우측 상단의 봉투 아이콘을 클릭하여 SMS 페이지로 들어가면 SMS 전달 설정을 찾을 수 있습니다.

![sms setting](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/sms.png){class="glboxshadow"}

### 이메일로 전달

![sms forwarding email](https://static.gl.inet.com/docs/router/en/4/tutorials/sms_forwarding/sms_forward_email.png){class="glboxshadow"}

- **SMTP 서버 주소**: 드롭다운 목록에서 Gmail, Outlook, iCloud, Yahoo용 사전 설정된 서버 주소를 사용할 수 있습니다. 기타 메일 제공업체의 경우 해당 문서를 참조하거나 지원팀에 문의하세요.

- **암호화 방식**: none, SSL/TLS, STARTTLS의 세 가지 옵션이 제공됩니다.

- **사용자 이름**: 여기에 이메일 주소를 입력하세요.

- **비밀번호**: 앱별 비밀번호 또는 로그인 계정 비밀번호를 사용하세요. Gmail, Outlook, iCloud, Yahoo의 경우 아래 가이드를 확인하세요.

- **제목**: 여기에 이메일 제목을 설정하세요.

??? "Gmail"

    Gmail의 경우 Google 계정에 로그인하여 **App Passwords**를 생성해야 합니다. 공식 가이드 [Sign in with App Passwords](https://support.google.com/accounts/answer/185833?hl=en){target="_blank"}을 확인하세요. App Passwords를 생성하기 전에 2단계 인증을 활성화해야 합니다.

    465 및 587 포트 모두 사용할 수 있습니다.

??? "Outlook"

    Outlook의 경우 설정 없이 비밀번호를 직접 사용할 수 있으며 587 포트를 지원합니다. 공식 가이드 [POP, IMAP, and SMTP settings for Outlook.com](https://support.microsoft.com/en-us/office/pop-imap-and-smtp-settings-for-outlook-com-d088b986-291d-42b8-9564-9c414e2aa040){target="_blank"}를 확인하세요.

??? "iCloud"

    iCloud의 경우 로그인용 앱별 비밀번호를 생성해야 하며 587 포트를 지원합니다. 공식 가이드 [iCloud Mail server settings for other email client apps](https://support.apple.com/en-hk/HT202304){target="_blank"} 및 [Generate an app-specific password](https://support.apple.com/en-gb/HT204397){target="_blank"}을 참조하세요.

??? "Yahoo"

    Yahoo의 경우 로그인용 앱 비밀번호를 설정해야 하며 465와 587 포트 모두 지원합니다. 공식 가이드 [POP access settings and instructions for Yahoo Mail](https://help.yahoo.com/kb/SLN4724.html){target="_blank"} 및 [Generate and manage third-party app passwords](https://help.yahoo.com/kb/SLN15241.html){target="_blank"}을 참조하세요.

**참고**: 각 이메일 발신자는 SMTP 전송 제한이 있을 수 있습니다(예: 일일 발신 이메일 수). 공급업체에 문의하세요.

최대 10개의 이메일 주소를 추가할 수 있습니다.

### SMS로 전달

![sms forwarding phone](https://static.gl.inet.com/docs/router/en/4/tutorials/sms_forwarding/sms_forward_phone.png){class="glboxshadow"}

국가 코드를 선택하고 전화 번호를 입력한 다음 Apply를 클릭하세요.

최대 10개의 휴대폰 번호를 추가할 수 있습니다.

---

관련 문서

- [SMS](../interface_guide/sms.md)

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}을 통해 연락하세요.
