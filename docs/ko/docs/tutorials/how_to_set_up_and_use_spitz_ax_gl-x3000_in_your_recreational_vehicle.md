# Recreational Vehicle에서 Spitz AX (GL-X3000) 설정 및 사용 방법

이 가이드는 Recreational Vehicle(RV, 캠핑카)에서 Spitz AX를 설정하고 사용하는 방법을 안내합니다. 시작하기 전에 다음 추가 장비와 서비스를 준비해야 할 수 있습니다.

- 사용하는 인터넷 연결 방법에 따라 SIM 카드 또는 USB 케이블(테더링용). SIM 카드를 사용하는 경우 통신사에 APN을 문의하세요.
- 더 나은 커버리지를 위한 루프 안테나.
- 셀룰러 커버리지가 없는 지역으로 이동하는 경우 [Starlink 구독](https://www.starlink.com/roam).

---

## 1. Spitz AX 및 기타 장비 설치

여정을 시작하기 전에 다음 단계에 따라 Spitz AX를 설정하세요.

### 1단계: Spitz AX 설치 위치 선택

최적의 커버리지를 위해 중앙에 위치하고 장애물이 없는 곳을 선택하는 것이 좋습니다. 전원 어댑터 케이블 길이인 1미터 이내에 전원원이 있는지 확인하세요.

![location](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_and_use_in_recreational_vehicle/x3000-with-power-source.jpg){class="glboxshadow"}

Spitz AX를 평평한 표면에 두거나 벽에 장착할 수 있습니다. 벽에 장착하기로 선택한 경우 다음 단계를 따르세요.

### (선택 사항) 2단계: 벽에 Spitz AX 설치

벽에 Spitz AX를 설치하는 두 가지 방법이 있습니다.
- 제공된 접착 패드 사용
- 벽 장착 브래킷 사용

벽 장착 브래킷은 패키지에 포함되어 있습니다. 벽에 Spitz AX를 장착하려면 다음 단계를 따르세요.

1. 나사를 사용하여 브래킷을 벽에 부착하세요.
2. Spitz AX를 브래킷에 끼우세요.

![wall mount](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_and_use_in_recreational_vehicle/x3000-with-screws.jpg){class="glboxshadow"}

### (선택 사항) 3단계: RV 루프 안테나 설치

![roof](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_and_use_in_recreational_vehicle/x3000-with-roof-antenna.jpg){class="glboxshadow"}

더 나은 신호를 얻으려면 Spitz AX용 루프 안테나를 사용하세요. 최적의 네트워크 신호를 제공하는 [MobileMark의 LTMG942 멀티밴드 안테나](https://www.mobilemark.com/product/ltmg942-4xlte-2xwifi-gnss/)를 사용하는 것이 좋습니다. 다른 브랜드의 루프 안테나를 사용하려는 경우 다음 요구사항을 충족하는지 확인하세요.

- 4개의 셀룰러 안테나, 수신 주파수 범위 600M~6GHz.
- 2개의 Wi-Fi 안테나, 수신 주파수 범위: 2.4G~2.5GHz, 5.15~5.84GHz

![antennas](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_and_use_in_recreational_vehicle/x3000-with-six-antennas.jpg){class="glboxshadow"}

**참고**: 7-in-1 안테나(GPS 안테나 포함)를 사용할 수 있지만 Spitz AX의 6개 안테나에만 연결하면 됩니다. Spitz AX의 DIV/GNSS 인터페이스는 GPS 신호를 지원합니다. 셀룰러 안테나(수신 주파수 600M~6GHz)가 GPS 주파수를 포함하기 때문입니다. Spitz AX는 명령줄을 사용하여 GPS 위치를 확인하는 기능을 지원하지만 현재 지도에 위치를 표시하는 기능은 지원하지 않습니다.

신호 감쇠를 방지하기 위해 루프 안테나에서 Spitz AX까지의 무선 주파수 케이블은 5미터를 초과하지 않아야 합니다. (예: MobileMark의 무선 주파수 케이블이 5미터인 경우 3000MHz에서의 신호 수신은 3dB(절반 강도) 감소합니다. 신호 주파수가 높을수록 감쇠가 커집니다.)

[Spitz AX에서 안테나 교체 방법 알아보기](https://docs.gl-inet.com/router/en/4/tutorials/how_to_change_x3000_and_xe3000_antennas/)

---

## 2. Spitz AX용 인터넷 설정

여정 중 인터넷 액세스를 보장하려면 SIM 카드를 사용하여 인터넷을 설정하세요.

Spitz AX는 내장형 5GNR 모듈이 있으며 듀얼 SIM 카드를 지원합니다. 다른 모바일 네트워크 통신사는 SIM 카드에 대해 다른 셀룰러 패키지를 제공하며 다른 APN을 사용합니다. 설정에서 APN을 입력해야 하므로 통신사에 APN이 무엇인지 확인하세요.

SIM 카드를 설정하려면 다음 단계를 따르세요.

1. SIM 카드를 삽입하세요.
![insert sim](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_and_use_in_recreational_vehicle/x3000-with-sim-card.jpg){class="glboxshadow"}
2. 전원 어댑터를 연결하고 라우터의 전원을 켜세요.

APN을 입력하려면 다음 단계를 따르세요.

1. 웹 브라우저에 `192.168.8.1`을 입력하고 로그인하세요.
2. 왼쪽 상단에 통신사 이름이 표시되어야 합니다. **Manual Setup**을 클릭하세요.
3. **APN** 옆에 APN을 입력하세요.
4. **Apply**를 클릭하세요.

두 개의 SIM 카드를 사용하는 경우 각 시간마다 하나의 SIM 카드만 작동한다는 점에 유의하세요. 매번 사용할 SIM 카드를 수동으로 선택할 수 있습니다. 또는 [Auto Switch 기능](https://docs.gl-inet.com/router/en/4/interface_guide/internet_cellular/#setup-for-dual-sim-models)을 활성화하세요. 라우터가 SIM 카드 중 하나가 인터넷에 제대로 액세스할 수 없는 것을 감지하면 자동으로 다른 SIM 카드로 전환됩니다. 전환에는 약 1분이 소요됩니다.

---

## 3. 다양한 시나리오에서 Spitz AX 사용

### 도로 위에서

![on the road](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_and_use_in_recreational_vehicle/rv-connectivity_scene_rv-antennas.png){class="glboxshadow"}

도로를 운전할 때 이전 단계에서 설정한 SIM 카드를 통해 인터넷에 연결할 수 있어야 합니다.

### 캠핑장에서

![campground](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_and_use_in_recreational_vehicle/rv-connectivity_scene_repeater.png){class="glboxshadow"}

여행 중 캠핑장에 멈추면 사이트에서 제공하는 공용 Wi-Fi 네트워크를 사용하고 셀룰러 데이터를 절약할 수 있습니다. [기존 Wi-Fi 네트워크에 연결하는 방법 알아보기](https://docs.gl-inet.com/router/en/4/interface_guide/internet_repeater/)

Wi-Fi 네트워크에 한 번 연결하면 Spitz AX가 네트워크 이름과 비밀번호를 기억할 수 있습니다. 다음번에 근처에 있을 때 자동으로 네트워크에 연결됩니다.

### 셀룰러 커버리지가 없는 지역에서

![cellular](https://static.gl.inet.com/docs/router/en/4/tutorials/set_up_and_use_in_recreational_vehicle/rv-connectivity_scene_starlink.png){class="glboxshadow"}

셀룰러 커버리지가 없는 지역(예: 인구가 희박한 사막 지역)으로 운전할 경우 위성 인터넷 서비스인 Starlink를 사용하세요. 이렇게 하면 셀룰러 커버리지가 좋은 지역에서는 Spitz AX가 수신하는 5G 신호를 사용하고, 셀룰러 커버리지가 없는 지역에서는 Starlink를 사용할 수 있습니다.

Starlink 안테나를 설정할 때 장애물이 없는지 확인하세요. 도로 양쪽의 장애물(예: 나무)은 수신에 영향을 미치므로 장애물에서 멀리 떨어진 곳에 주차하세요.

---

## 4. Failover 우선순위 설정

Spitz AX는 멀티 WAN(failover 및 로드 밸런싱)을 지원합니다. 시나리오에 따라 다른 네트워크의 failover 우선순위를 설정할 수 있습니다.

| 시나리오 | 우선순위 |
| -------- | ------- |
| 캠핑장(Repeater를 통해 Wi-Fi 네트워크에 연결됨) | <p> 셀룰러보다 Repeater에 더 높은 우선순위를 할당하세요.</p> <p>캠핑장을 떠나는 즉시 라우터가 자동으로 셀룰러로 전환됩니다.</p>|
| Starlink(이더넷) + 셀룰러 | 이더넷보다 셀룰러에 더 높은 우선순위를 할당하세요. <p>셀룰러 커버리지가 있는 지역에서는 라우터가 셀룰러 네트워크를 사용합니다.</p> <p>셀룰러 커버리지가 없는 지역에 도착하면 라우터가 자동으로 이더넷을 통해 Starlink로 전환됩니다.</p>|

Failover를 설정하려면 [Failover](https://docs.gl-inet.com/router/en/4/interface_guide/multi-wan/) 섹션을 참조하세요.

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}을 통해 문의해 주세요.
