# LAN

웹 관리 패널 왼쪽에서 **NETWORK** -> **LAN**으로 이동합니다.

LAN은 장치가 주요 Wi-Fi 또는 이더넷 케이블을 통해 연결될 때 연결되는 네트워크입니다.

기본 설정, DHCP 서버 설정 및 주소 예약이 포함됩니다.

## 기본 설정

IPv4 프라이빗 주소 범위 내에서 서브넷을 설정할 수 있습니다: `192.168.0.0/16`, `172.16.0.0/12`, `10.0.0.0/8`

![lan basic settings](https://static.gl-inet.com/docs/router/en/4/interface_guide/lan/basic_settings.jpg){class="glboxshadow"}

- **라우터 IP 주소**

    브라우저 주소 표시줄에 입력하여 라우터 관리 페이지에 액세스하는 주소입니다.

    기본값은 **192.168.8.1**입니다. 네트워크와 충돌하는 경우 변경할 수 있습니다.

- **서브넷 마스크**

    기본값은 **255.255.255.0**입니다. 더 많은 IP 주소가 필요한 더 큰 서브넷이 필요한 경우 **255.255.0.0**을 선택할 수도 있습니다.

- **AP 격리**

    클라이언트 장치를 별도의 네트워크 세그먼트로 격리할 수 있습니다. 이러한 장치는 동일한 네트워크의 다른 장치와 통신할 수 없게 됩니다.

## DHCP 서버

**DHCP 서버**는 기본적으로 활성화되어 있습니다. DHCP 서버는 각 클라이언트 장치에 IP 주소 및 기타 통신 매개변수를 자동으로 할당합니다.

DHCP 서버를 비활성화하면 클라이언트 장치의 네트워크 설정을 수동으로 구성해야 합니다. 수동으로 고정 IP를 구성하는 방법을 알아보려면 [여기](../tutorials/manually_configure_static_ip.md)를 클릭하세요.

네트워크 확장 또는 축소, IP 주소 충돌 발생, 서브넷 마스크 범위 수정 등 필요에 따라 시작 및 종료 IP 주소를 변경할 수 있습니다.

![dhcp simple settings](https://static.gl-inet.com/docs/router/en/4/interface_guide/lan/dhcp_server.png){class="glboxshadow"}

필요한 경우 **Advanced**를 클릭하여 추가 구성을 진행하세요.

![dhcp advanced settings 1](https://static.gl-inet.com/docs/router/en/4/interface_guide/lan/dhcp_advanced_1.png){class="glboxshadow"}

![dhcp advanced settings 2](https://static.gl-inet.com/docs/router/en/4/interface_guide/lan/dhcp_advanced_2.png){class="glboxshadow"}

- **임대 시간**: DHCP가 할당한 IP 주소가 장치에 대해 유효한 기간입니다.

- **게이트웨이**: LAN과 인터넷과 같은 외부 네트워크 간의 트래픽을 라우팅하는 장치입니다.

- **DNS 서버 1**: 도메인 이름을 IP 주소로 변환하는 기본 서버입니다.

- **DNS 서버 2**: 기본 DNS 서버를 사용할 수 없을 때 도메인 이름 확인을 위해 사용되는 보조 서버입니다.

- **LPR 서버**: (Line Printer Remote Server) 인쇄 작업을 관리하고 네트워크 장치가 원격 프린터로 인쇄 요청을 보낼 수 있도록 하는 서비스입니다. 여러 LPR 프린터 포트를 구성할 수 있습니다.

## 주소 예약

LAN 내 클라이언트를 위해 예약된 IP 주소를 지정하면 클라이언트가 라우터의 DHCP 서버에 액세스할 때마다 항상 동일한 IP 주소를 받습니다. 영구적인 IP 설정이 필요한 컴퓨터나 서버에 예약된 IP 주소를 할당할 수 있습니다.

**참고:** 구성된 클라이언트는 활성화하기 위해 라우터에 다시 연결해야 합니다.

**추가**를 클릭하여 IP를 예약합니다.

![Address Reservation 1](https://static.gl-inet.com/docs/router/en/4/interface_guide/lan/address_reservation_1.png){class="glboxshadow"}

팝업 창이 나타납니다.

![Address Reservation 2](https://static.gl-inet.com/docs/router/en/4/interface_guide/lan/address_reservation_2.png){class="glboxshadow"}

드롭다운 목록에서 **MAC**를 선택하면 선택된 MAC에 해당하는 **IP**가 자동으로 채워집니다. 설명이 포함된 이름을 지정합니다. 그런 다음 **제출**을 클릭합니다.

![Address Reservation 3](https://static.gl-inet.com/docs/router/en/4/interface_guide/lan/address_reservation_3.png){class="glboxshadow"}

새 IP 주소 예약을 추가한 후 아래와 같은 페이지가 표시되며, 성공적으로 설정된 것입니다.

![Address Reservation 4](https://static.gl-inet.com/docs/router/en/4/interface_guide/lan/address_reservation_4.jpg){class="glboxshadow"}

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 통해 연락하세요.
