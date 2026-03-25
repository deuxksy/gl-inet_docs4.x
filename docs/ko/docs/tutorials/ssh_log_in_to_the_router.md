# 라우터에 SSH 로그인

Secure Shell (SSH)는 보안되지 않은 네트워크에서 네트워크 서비스를 안전하게 운영하기 위한 암호화 네트워크 프로토콜입니다. 가장 잘 알려진 예는 애플리케이션 사용자가 컴퓨터 시스템에 원격 로그인하는 것입니다. 기본 도구가 필요할 때 서버에 SSH로 로그인해야 하는 경우가 있습니다. 이 가이드는 GL.iNet 라우터에 SSH 로그인하는 방법을 안내합니다.

---

## Windows 사용자

Windows Cmd, PowerShell, Bitvise 또는 PuTTY 등을 통해 라우터 터미널에 액세스하는 방법이 있습니다.

### Windows Cmd 사용

1. 명령 프롬프트 열기

    **Win** + **R** 키(Windows 키 + R 키)를 눌러 실행 상자를 엽니다. **cmd**를 입력하고 Enter를 누르세요.

    ![cmd](https://static.gl.inet.com/docs/router/en/4/tutorials/ssh_log_in_to_the_router/cmd_1.png){class="glboxshadow gl-60-desktop"}

    검은 명령 프롬프트 창이 나타납니다.

    ![cmd](https://static.gl.inet.com/docs/router/en/4/tutorials/ssh_log_in_to_the_router/cmd_2.jpg){class="glboxshadow"}

2. 라우터에 로그인하세요

    명령 프롬프트 창에서 `ssh root@192.168.8.1`을 입력하고 Enter를 누르세요.

    ![cmd ssh root](https://static.gl.inet.com/docs/router/en/4/tutorials/ssh_log_in_to_the_router/cmd_ssh_root.jpg){class="glboxshadow"}

    **참고**: 192.168.8.1은 라우터의 기본 IP 주소입니다. 이전에 변경한 경우 사용자 정의 IP를 사용하세요.

    다음으로 라우터의 관리자 비밀번호를 입력하고 Enter를 누르세요. **보안을 위해 비밀번호가 화면에 표시되지 않습니다.**

    ![cmd psw](https://static.gl.inet.com/docs/router/en/4/tutorials/ssh_log_in_to_the_router/cmd_psw.jpg){class="glboxshadow"}

    비밀번호가 올바르면 라우터에 성공적으로 로그인됩니다.

    ![cmd login](https://static.gl.inet.com/docs/router/en/4/tutorials/ssh_log_in_to_the_router/cmd_login.png){class="glboxshadow"}

??? "문제 해결"

    1. **Error: Connection timed out**

        장치(예: 랩톱)가 라우터에 연결되어 있는지 확인하세요. 라우터의 Wi-Fi나 LAN 포트에 다시 연결하고 다시 시도해 보세요.

    2. **Error: Permission denied**

        올바른 관리자 비밀번호를 입력했는지 확인하세요. 비밀번호를 잊어버린 경우 RESET 버튼을 10초간 눌러 라우터를 재설정하세요.

### PowerShell 사용

1. Windows PowerShell 열기

    작업 표시줄에서 검색 아이콘을 클릭하고 **PowerShell**을 입력한 다음 **Windows PowerShell**을 선택하고 **관리자 권한으로 실행**하세요.

    ![run powershell](https://static.gl.inet.com/docs/router/en/4/tutorials/ssh_log_in_to_the_router/run_as_administrator.png){class="glboxshadow gl-90-desktop"}

2. 라우터에 로그인

    PowerShell 창에서 `ssh root@192.168.8.1`을 입력하고 Enter를 누르세요.

    ![powershell ssh root](https://static.gl.inet.com/docs/router/en/4/tutorials/ssh_log_in_to_the_router/powershell_ssh_root.jpg){class="glboxshadow gl-90-desktop"}

    **참고**: 192.168.8.1은 라우터의 기본 IP 주소입니다. 이전에 변경한 경우 사용자 정의 IP를 사용하세요.

    시스템에서 연결을 확인하라는 메시지가 표시됩니다. `yes`를 입력하고 Enter를 누르세요.

    ![powershell confirm](https://static.gl.inet.com/docs/router/en/4/tutorials/ssh_log_in_to_the_router/powershell_confirm.png){class="glboxshadow gl-90-desktop"}

    라우터의 관리자 비밀번호를 입력하라는 프롬프트가 표시됩니다. 올바른 관리자 비밀번호를 입력하고 Enter를 누르세요. **보안을 위해 비밀번호가 화면에 표시되지 않습니다.**

    ![powershell psw](https://static.gl.inet.com/docs/router/en/4/tutorials/ssh_log_in_to_the_router/powershell_psw.png){class="glboxshadow gl-90-desktop"}

    그러면 라우터 터미널에 성공적으로 로그인됩니다.

    ![powershell login](https://static.gl.inet.com/docs/router/en/4/tutorials/ssh_log_in_to_the_router/powershell_login.png){class="glboxshadow gl-90-desktop"}

??? "문제 해결"

    1. **WARNING: REMOTE HOST IDENTIFICATION HAS CHANGED!** / **Host key verification failed**

        이는 라우터의 보안 키가 변경된 경우(예: 공장 초기화 또는 펌웨어 업그레이드 후) 또는 이전에 다른 라우터에 연결한 적이 있어 호스트 키 확인이 실패한 경우에 발생합니다.

        ![warning](https://static.gl.inet.com/docs/router/en/4/tutorials/ssh_log_in_to_the_router/powershell_warning.jpg){class="glboxshadow gl-90-desktop"}

        해결하려면 파일 탐색기를 열고 `C:\Users\Administrator\.ssh`로 이동하여 **known_hosts**라는 파일을 찾으세요.

        ![known hosts](https://static.gl.inet.com/docs/router/en/4/tutorials/ssh_log_in_to_the_router/known_hosts.png){class="glboxshadow gl-90-desktop"}

        known_hosts 파일을 두 번 클릭하고 메모장으로 엽니다.

        ![open with notepad](https://static.gl.inet.com/docs/router/en/4/tutorials/ssh_log_in_to_the_router/open_notepad.png){class="glboxshadow"}

        라우터 IP 주소(예: 192.168.8.1)와 관련된 항목을 삭제하고 파일을 저장합니다. 파일 탐색기를 종료하세요.

        ![delete known hosts](https://static.gl.inet.com/docs/router/en/4/tutorials/ssh_log_in_to_the_router/delete_known_hosts.png){class="glboxshadow gl-90-desktop"}

        PowerShell로 돌아가서 `ssh root@192.168.8.1` 명령을 사용하여 라우터에 다시 연결하세요. 연결을 확인하라는 메시지가 표시되면 `yes`를 입력하고 enter를 누른 다음 라우터 로그인 비밀번호를 입력합니다. 그러면 라우터 터미널에 성공적으로 로그인됩니다.

    2. **라우터의 SSH 포트를 변경한 경우 어떻게 해야 하나요?**

        라우터의 SSH 포트를 변경한 경우 ssh 명령 사용 시 "-p" 매개변수를 통해 포트를 지정해야 합니다. 예를 들어:

        ``ssh -p [새 포트 번호] [사용자 이름]@[라우터 IP 주소]```

### Bitvise 사용

비디오를 시청하여 Bitvise를 통해 라우터에 로그인하세요.

<iframe width="560" height="315" src="https://www.youtube.com/embed/7yVd5UkKJ74" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### PuTTY 사용

1. PuTTY 다운로드

    [여기](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html){target="_blank"}에서 최신 PuTTY 버전을 다운로드하세요.

2. PuTTY 설치

    ![Putty Install 1](https://static.gl.inet.com/docs/router/en/4/tutorials/ssh_log_in_to_the_router/putty_install_1.png){class="glboxshadow"}

    ![Putty Install 2](https://static.gl.inet.com/docs/router/en/4/tutorials/ssh_log_in_to_the_router/putty_install_2.png){class="glboxshadow"}

    ![Putty Install 3](https://static.gl.inet.com/docs/router/en/4/tutorials/ssh_log_in_to_the_router/putty_install_3.png){class="glboxshadow"}

    ![Putty Install 4](https://static.gl.inet.com/docs/router/en/4/tutorials/ssh_log_in_to_the_router/putty_install_4.png){class="glboxshadow"}

3. PuTTY 시작

    시작 메뉴에서 **PuTTY**를 클릭하세요.

    ![Launch Putty](https://static.gl.inet.com/docs/router/en/4/tutorials/ssh_log_in_to_the_router/launch_putty.png){class="glboxshadow"}

    다음 구성 창이 표시됩니다.

    ![Setup Putty 1](https://static.gl.inet.com/docs/router/en/4/tutorials/ssh_log_in_to_the_router/setup_putty_1.png){class="glboxshadow"}

    Host Name (또는 IP 주소)에 `192.168.8.1`을 입력하고 Port는 기본값인 `22`로 유지하세요. 연결 유형을 `SSH`로 선택합니다.

    저장 세션에 `Your Session`을 입력하고 내용을 **Save**하세요.

    그런 다음 하단의 `Open`을 클릭하세요.

    ![Setup Putty 2](https://static.gl.inet.com/docs/router/en/4/tutorials/ssh_log_in_to_the_router/setup_putty_2.png){class="glboxshadow"}

    아래와 같은 보안 경고가 팝업되며 `Yes`를 클릭하세요.

    ![Setup Putty 3](https://static.gl.inet.com/docs/router/en/4/tutorials/ssh_log_in_to_the_router/setup_putty_3.png){class="glboxshadow"}

    로그인: `root`

    그런 다음 관리자 비밀번호를 입력하세요. **보안을 위해 비밀번호가 화면에 표시되지 않습니다.**

    ![SSH login successfully](https://static.gl.inet.com/docs/router/en/4/tutorials/ssh_log_in_to_the_router/ar750s_ssh_successfully.jpg){class="glboxshadow"}

    위와 같은 화면이 표시되면 라우터에 SSH로 성공적으로 로그인된 것입니다.

---

## Linux/Mac 사용자

Linux 및 Mac OS의 프로세스는 일반적으로 동일합니다. 여기서는 Ubuntu를 예로 사용합니다.

### Ubuntu 사용

1. 터미널 시작

    Ubuntu를 실행하고 터미널 아이콘을 두 번 클릭하여 터미널을 시작하세요.

    ![Run Ubuntu](https://static.gl.inet.com/docs/router/en/4/tutorials/ssh_log_in_to_the_router/ubuntu_login.png){class="glboxshadow"}

2. 라우터에 로그인

    SSH 로그인 명령을 입력하세요: `ssh root@192.168.8.1`

    ![Ubuntu sshin router 1](https://static.gl.inet.com/docs/router/en/4/tutorials/ssh_log_in_to_the_router/ubuntu_sshin_router_1.png){class="glboxshadow"}

    시스템에서 연결을 확인하라는 메시지가 표시됩니다. "yes"를 입력하고 Enter를 누르세요.

    ![Ubuntu sshin router 2](https://static.gl.inet.com/docs/router/en/4/tutorials/ssh_log_in_to_the_router/ubuntu_sshin_router_2.png){class="glboxshadow"}

    그런 다음 라우터의 관리자 비밀번호를 입력하세요. **보안을 위해 비밀번호가 화면에 표시되지 않습니다.**

    ![Ubuntu sshin router 3](https://static.gl.inet.com/docs/router/en/4/tutorials/ssh_log_in_to_the_router/ubuntu_sshin_router_3.png){class="glboxshadow"}

    위와 같은 화면이 표시되면 라우터에 성공적으로 로그인된 것입니다.

??? "문제 해결"

    1. **WARNING: REMOTE HOST IDENTIFICATION HAS CHANGED!** / **Host key verification failed**

        이는 라우터의 보안 키가 변경된 경우(예: 공장 초기화 또는 펌웨어 업그레이드 후) 또는 이전에 다른 라우터에 연결한 적이 있어 호스트 키 확인이 실패한 경우에 발생합니다.

        ![remove_ssh_keygen](https://static.gl.inet.com/docs/router/en/4/tutorials/ssh_log_in_to_the_router/remove_ssh_keygen.png){class="glboxshadow gl-90-desktop"}

        이 문제가 발생하면 빨간 상자의 명령을 실행하세요. 터미널에 표시되는 정확한 명령을 복사하세요.

        `ssh-keygen -f "~/.ssh/known_hosts" -R "192.168.8.1"`

        ![removed_host_keygen](https://static.gl.inet.com/docs/router/en/4/tutorials/ssh_log_in_to_the_router/removed_host_keygen.png){class="glboxshadow gl-90-desktop"}

        그런 다음 다시 연결해 보세요.

    2. **Unable to negotiate with 10.0.0.1 port 22: no matching host key type found. Their offer: ssh-rsa**

        연결할 때 이 오류가 발생할 수 있습니다. 이 오류는 Openssh 패키지가 버전 8.8에서 변경되어 발생합니다. 해결하려면 **~/.ssh/config** 파일을 텍스트 편집기(Nano 또는 Vim 등 사용)로 열고 다음 줄을 추가하세요:

            host 192.168.8.1
                HostkeyAlgorithms +ssh-rsa
                PubkeyAcceptedAlgorithms +ssh-rsa

        기본 IP가 아닌 경우 호스트 IP를 변경하세요.

        이 문제에 대한 더 자세한 논의는 [여기](https://forum.gl-inet.com/t/can-no-longer-ssh-into-router-no-matching-host-key-type-found-their-offer-ssh-rsa/20915){target="_blank"}을 참조하세요.

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}을 통해 연락하세요.
