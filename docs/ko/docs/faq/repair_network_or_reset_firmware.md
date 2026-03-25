# 네트워크 복구 또는 공장 초기화 방법

모든 GL.iNet 라우터는 물리적 재설정 메커니즘(재설정 버튼 또는 핀홀)이 장착되어 있습니다. 버튼을 누르거나 핀을 누르는 것은 동일한 효과를 가집니다: 네트워크 연결을 복구하거나 라우터를 공장 기본값으로 재설정합니다.

핀홀 모델의 경우 핀, 펴 클립 또는 유사한 도구를 사용하여 작업을 수행하세요.

재설정을 수행하기 전에 라우터가 완전히 부팅되었는지 확인하세요. 라우터가 부팅된 직후 재설정 버튼을 누르지 **마세요**. 그렇지 않으면 U-Boot failsafe 모드가 트리거될 수 있습니다.

## 네트워크 복구

재설정 버튼을 **4초**간 눌른 후 놓아 소프트 리셋을 수행하여 네트워크를 복구할 수 있습니다.

이 작업은 네트워크 인터페이스를 재부팅하고 인터넷 인터페이스를 기본 설정으로 복원하지만 Wi-Fi 설정, VPN 설정, 시스템 설정 등은 보존됩니다.

**참고**:

1. Wi-Fi가 비활성화된 경우 소프트 리셋은 Wi-Fi를 기본 활성화된 상태로 복원합니다.

2. 소프트 리셋은 라우터 모드에서 비 라우터 모드로 빠르게 전환하는 데 사용할 수도 있습니다.

## 공장 초기화

이 비디오를 시청하거나 아래 단계를 따르세요.

<iframe width="560" height="315" src="https://www.youtube.com/embed/jguDqBWP-Fw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

펌웨어를 초기화하는 방법은 두 가지가 있습니다.

1. 물리적 재설정 메커니즘(버튼 또는 핀) 사용

    재설정 버튼(또는 핀에 핀을 넣음)을 **10초**간 누른 후 놓아 라우터를 공장 설정으로 재설정합니다. 모든 사용자 데이터가 삭제됩니다.

    **참고:** 공장 초기화가 작동하지 않으면 [Uboot 튜토리얼](debrick.md)을 따라 라우터의 벽돌을 해제해야 할 수도 있습니다.

2. 웹 관리 패널에서 펌웨어 초기화

    라우터의 웹 관리 패널에 로그인하고 SYSTEM -> Reset Firmware로 이동한 다음 버튼을 클릭하여 펌웨어를 초기화하세요.

    **참고:** 현재 모든 설정과 데이터가 손실됩니다. 프로세스는 약 2분 정도 소요됩니다. 이 과정 중 라우터의 전원을 끄지 마세요.

    ![glinet reset firmware](https://static.gl.inet.com/docs/router/en/4/tutorials/reset_firmware/reset_firmware_4.8.png){class="glboxshadow"}

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}을 통해 연락하세요.
