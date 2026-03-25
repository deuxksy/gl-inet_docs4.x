# HTTPS를 사용하여 GL.iNet 라우터 및 Adguard Home에 접속하는 방법

HTTPS를 사용하여 GL.iNet 라우터 및 Adguard Home에 접속하려면 다음 단계를 따르세요.

## 1. GL.iNet 라우터에서 인증서 및 키 업데이트

먼저 SSL 인증서를 신청하거나 자체 서명된 SSL 인증서를 사용하세요.

그런 다음 GL.iNet 라우터에 SSH로 접속하거나 WinSCP를 사용하여 업데이트된 인증서와 키를 업로드하세요. 경로는 다음과 같습니다:

`/etc/nginx/nginx.cer`

`/etc/nginx/nginx.key`

## 2. AdGuard Home 활성화

GL.inet 웹 관리 패널에 로그인 -> APPLICATIONS -> AdGuard Home으로 이동하여 AdGuard Home을 활성화하세요.

![enableadh](https://static.gl.inet.com/docs/router/en/4/faq/SSL/enableadh.jpg){class="glboxshadow}

그런 다음 이 페이지 상단의 **Settings Page**를 클릭하면 Adguard Home 설정 페이지로 리디렉션됩니다.

![gosettings](https://static.gl.inet.com/docs/router/en/4/faq/SSL/gosettings.jpg){class="glboxshadow"}

## 3. 암호화 설정 편집

Adguard Home 설정 페이지에서 Settings -> Encryption 설정으로 이동하세요.

![encryption](https://static.gl.inet.com/docs/router/en/4/faq/SSL/encryption.jpg){class="glboxshadow"}

왼쪽 상단의 Enable Encryption 확인란을 체크하고 HTTPS 포트에 3001을 입력하세요.

![3001](https://static.gl.inet.com/docs/router/en/4/faq/SSL/3001.jpg){class="glboxshadow}

업데이트된 인증서와 키의 경로를 추가하고 저장을 클릭하세요.

![addcertpath](https://static.gl.inet.com/docs/router/en/4/faq/SSL/addcertpath.jpg){class="glboxshadow}

그러면 HTTPS를 사용하여 **192.168.8.1** 또는 **192.168.8.1:3001**에 방문할 수 있습니다.

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}을 통해 연락하세요.
