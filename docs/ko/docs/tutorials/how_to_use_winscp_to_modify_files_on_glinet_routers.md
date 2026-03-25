# WinSCP를 사용하여 GL.iNet 라우터의 파일 수정 방법

WinSCP는 라우터의 파일이나 디렉터리를 편집하고 복사 및 다운로드할 수 있는 쉬운 도구입니다. FTP, SCP, SFTP, WebDAV 또는 S3 파일 전송 프로토콜을 사용하여 로컬 컴퓨터와 라우터 간에 파일을 복사할 수 있습니다. Windows 운영 체제에서 사용할 수 있습니다.

---

1. [여기](https://winscp.net/eng/download.php){target="_blank"}에서 WinSCP를 다운로드하여 Windows에 설치하세요.

2. 라우터에 연결한 다음 WinSCP를 실행하세요.

    ![WinSCP login](https://static.gl.inet.com/docs/router/en/4/tutorials/winscp/login.png){class="glboxshadow"}

    * File protocol: 프로토콜로 `SCP`를 선택하세요.
    * Host name: 라우터 IP를 입력하세요. 라우터의 IP를 변경하지 않았다면 `192.168.8.1`입니다.
    * Port number: `22`
    * Username & Password: 사용자 이름으로 `root`를 입력하고 비밀번호를 입력하세요.

    그런 다음 `Login` 버튼을 클릭하세요.

3. 로그인하면 라우터를 완전히 제어할 수 있습니다.

    라우터에서/로 파일/디렉터리를 보고, 선택, 편집 또는 전송할 수 있습니다.

    ![WinSCP panel](https://static.gl.inet.com/docs/router/en/4/tutorials/winscp/winscp_panel_marked.png){class="glboxshadow"}

    예를 들어 방화벽配置(config)을 편집하려면 /etc/config로 이동하여 방화벽 파일을 찾고 마우스 오른쪽 버튼을 클릭한 다음 **Edit**를 선택하세요.

    ![WinSCP edit 1](https://static.gl.inet.com/docs/router/en/4/tutorials/winscp/edit_1.png){class="glboxshadow"}

    이제 파일 내용을 자유롭게 편집할 수 있습니다. 설정을 망치지 않도록 주의하세요.

    ![WinSCP edit 2](https://static.gl.inet.com/docs/router/en/4/tutorials/winscp/edit_2.png){class="glboxshadow"}

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}을 통해 연락하세요.
