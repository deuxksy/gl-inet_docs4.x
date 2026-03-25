# MAC 주소

이 가이드는 펌웨어 v4.5 이전 버전에 적용됩니다.

MAC 주소 페이지는 이전에 MAC 클론이라고 불렸으며 v4.2부터 MAC 주소로 이름이 변경되었습니다.

v4.6부터 이더넷 및 리피터 인터페이스의 MAC 주소 설정은 각각 [이더넷 포트](ethernet_port.md) 및 [리피터](internet_repeater.md)로 이동되었습니다.

---

웹 관리 패널 왼쪽에서 **NETWORK** -> **MAC Address**로 이동합니다.

라우터의 기본 MAC 주소를 찾고, 클라이언트의 MAC 주소를 복제하고, MAC 주소를 수동으로 입력하거나 무작위 MAC 주소를 생성할 수 있습니다.

장치가 여러 이더넷 포트를 WAN 포트로 사용하도록 설정하는 것을 지원하는 경우 각 포트에 대해 MAC 주소를 별도로 설정할 수 있습니다. MAC 주소 설정은 이더넷 포트가 WAN 포트로 사용될 때만 유효합니다.

![default mac address](https://static.gl-inet.com/docs/router/en/4/interface_guide/mac_address/mac_address.png){class="glboxshadow"}

* 공장 기본 MAC 주소.

    ![default mac address](https://static.gl-inet.com/docs/router/en/4/interface_guide/mac_address/factory_default.png){class="glboxshadow"}

* 클라이언트의 MAC 주소 복제.

    ![clone mac address](https://static.gl-inet.com/docs/router/en/4/interface_guide/mac_address/clone.png){class="glboxshadow"}

    **참고:** 많은 새 장치는 이제 다른 Wi-Fi에 연결하기 위해 다른 무작위 MAC 주소를 사용하므로 여기에 표시된 MAC 주소는 사용자 장치의 실제 MAC 주소가 아닐 수 있습니다. 무작위 MAC는 다른 장치에서 프라이빗 Wi-Fi 주소 또는 무작위 하드웨어 주소라고도 할 수 있습니다.

* 수동 입력 또는 무작위 MAC 주소 생성.

    ![Manual input or generate a random mac address](https://static.gl-inet.com/docs/router/en/4/interface_guide/mac_address/manual.png){class="glboxshadow"}

## 사용 시나리오

공용 핫스팟에 연결할 때 핫스팟이 실제 MAC 주소를 알지 못하게 하거나 이를 기반으로 인터넷 액세스를 제한하지 않으려면 무작위 MAC 주소를 사용하세요. 이 가이드 [캡티브 포털이 있는 핫스팟에 연결](../faq/connect_to_a_hotspot_with_captive_portal.md)을 읽어보세요.

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 통해 연락하세요.
