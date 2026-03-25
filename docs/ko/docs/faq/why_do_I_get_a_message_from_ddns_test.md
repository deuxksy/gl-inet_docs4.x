# DDNS 테스트에서 메시지가 표시되는 이유는 무엇인가요?

Dynamic DNS 페이지에서 DDNS 테스트를 실행하면 아래와 같은 메시지가 표시될 수 있습니다.

**"DDNS 도메인 확인에서 얻은 IP 주소가 장치의 WAN IP와 다릅니다."**

**"Dynamic DNS를 사용하려면 인터넷 공용 IP 주소가 필요합니다."**

![ddnstest](https://static.gl.inet.com/docs/router/en/4/faq/warning_on_ddns_test/ddnstest.jpg){class="glboxshadow"}

이는 **경고** 또는 **오류** 메시지가 아니라 라우터의 네트워크 상태를 나타내는 알림입니다.

이 결과는 일반적으로 라우터의 네트워크 위치를 반영합니다. 예를 들어 GL.iNet 라우터가 가정 네트워크에서 보조 라우터로 구성된 경우 이 메시지가 표시됩니다.

기본 라우터에서 포트 포워딩을 설정하더라도 이 메시지는 사라지지 않습니다. 이는 단순히 라우터가 뒤에 NAT가 있음을 나타냅니다.

NAT를 통해 서비스를 노출해야 하는 경우(예: 원격 액세스) 추가 설정이 필요합니다.

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}을 통해 연락하세요.
