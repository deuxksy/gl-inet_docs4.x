# 브라우저 경고: 연결이 프라이빗하지 않음

GL.iNet 라우터를 처음 설정할 때 다음 브라우저 경고를 encounter할 수 있습니다: 연결이 프라이빗하지 않음.

![alert](https://static.gl.inet.com/docs/router/en/4/faq/warning_from_your_browser/alert.jpg){class="glboxshadow}

신뢰할 수 없는 SSL/TLS 인증서가 없는 웹사이트를 감지했을 때 브라우저가 발행하는 표준 보안 경고입니다.

브라우저는 일반적으로 제3자 인증 기관(CA)에서 발급한 인증서를 신뢰하도록 설계되어 있습니다. 그러나 GL.iNet 라우터는 자체 서명된 인증서를 사용하며 이는 CA에서 발급되지 않습니다. 따라서 브라우저는 이를 안전하지 않은 것으로 표시하고 이 경고를 표시합니다.

## 192.168.8.1을 탐색하는 것이 안전한가요?

네트워크 보안을 최우선으로 생각합니다. 초기 설정 중에는 인터넷 연결이 필요하지 않으며 프로세스는 완전히 로컬입니다.

설정 중에 GL.iNet 라우터의 Wi-Fi에 연결하면 **"연결됨, 인터넷 없음"**이 표시될 수 있습니다. 이는 예상적인 것으로 라우터는 구성 중 독립형 로컬 네트워크에서 작동하기 때문입니다.

![nointernet](https://static.gl.inet.com/docs/router/en/4/faq/warning_from_your_browser/nointernet.jpg){class="glboxshadow"}

마찬가지로 **192.168.8.1**은 라우터 자체에 할당된 프라이빗 로컬 IP 주소입니다. 장치의 로컬 관리 패널에 액세스하는 데 사용되며 공개 웹사이트가 아닙니다.

연결이 완전히 로컬이며 설정 중 인터넷 액세스가 필요하지 않으므로 **프라이버시 유출 위험이 없습니다**. 이는 라우터를 구성하기 위한 안전하고 격리된 환경을 보장합니다.

## 왜 여전히 경고가 표시되나요?

브라우저는 일반적으로 미리 설정된 설정 IP 주소와 일반 웹사이트를 구별하지 않으며 모든 IP 주소를 웹사이트로 처리하고 HTTPS 연결은 SSL/TLS 인증서로 보안되어야 한다고 기대합니다.

GL.iNet 라우터는 SSL/TLS 인증서를 사용하지만 자체 서명된 것이며 제3자 인증 기관(CA)에서 발급되지 않습니다. 이 IP에 액세스하는 것이 안전합니다(프라이빗 로컬 네트워크에 있기 때문)지만 브라우저에서는 여전히 "안전하지 않은" 것으로 간주되며 경고가 표시됩니다.

## 이 경고로 무엇을 할 수 있나요?

**고급**을 클릭하고 **192.168.8.1로 계속**을 클릭하세요

![continue](https://static.gl.inet.com/docs/router/en/4/faq/warning_from_your_browser/continue.jpg){class="glboxshadow}

그러면 웹 관리 패널로 리디렉션됩니다.

![setup](https://static.gl.inet.com/docs/router/en/4/faq/warning_from_your_browser/setup.jpg){class="glboxshadow"}

## 라우터에 SSL 인증서를 추가할 수 있나요?

예, GLiNet 라우터에 SSL 인증서를 추가할 수 있습니다.

[SSL 인증서 추가 방법](../faq/use_https_for_adh.md)

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}을 통해 연락하세요.
