# VPN 속도가 예상보다 느린 이유는 무엇인가요?

VPN 연결 속도가 이론적 최대 속도(이상적인 로컬 영역 네트워크에서 테스트됨)보다 낮은 것을 발견했다면 실제 사용에서는 이것이 정상입니다.

VPN은 보안과 프라이버시를 우선으로 설계되어 있어 속도에 영향을 미칩니다. 일반적인 네트워크 조건에서 VPN 속도가 광고된 최대 속도의 30-50% 사이인 것이 정상입니다. 이러한 차이는 성능에 영향을 미치는 여러 요인 때문이며 아래에서 설명하고 경험을 최적화하기 위한 팁도 제공합니다.

**참고**: 아래 방법은 VPN 속도를 개선하는 데 도움이 될 수 있지만 실제 성능은 여러 요인에 따라 달라지므로 광고된 속도와 일치한다고 보장할 수는 없습니다.

## 라우터 CPU 속도

VPN은 프라이버시를 보호하기 위해 데이터를 암호화하여 추가 데이터 처리를 추가합니다. 이 암호화 및 복호화는 연결을 늦추게 됩니다. VPN 속도를 높이려면 더 빠른 CPU를 가진 라우터를 선택하세요.

모든 모델의 VPN 테스트 속도는 [제품 페이지](https://www.gl-inet.com/products/)에 나열되어 있습니다. 그러나 다음 사항에 유의하세요:

* 테스트는 로컬 네트워크에서 수행됩니다. 실제 속도는 네트워크 구성에 따라 다를 수 있습니다.
* 라우터가 서버로 사용될 때 OpenVPN 및 WireGuard 속도는 느려집니다. 위 결과는 클라이언트 모드입니다.

## 서버 거리

VPN 서버가 실제 위치에서 멀리 떨어져 있으면 데이터가 더 먼 거리를 이동해야 하므로 대기 시간이 길어지고 속도가 느려집니다.

아래 예제는 같은 시간에 다른 서버 위치에 연결할 때의 클라이언트 속도를 보여줍니다.

![hk](https://static.gl.inet.com/docs/router/en/4/faq/vpn_speed/hkserver.jpg){class="glboxshadow"}

![canada](https://static.gl.inet.com/docs/router/en/4/faq/vpn_speed/canadaserver.jpg){class="glboxshadow"}

## 서버 부하

동일한 VPN 서버에 많은 사용자가 연결되면 혼잡해져 모든 사용자의 속도가 느려질 수 있습니다.

## 서버 업로드 속도

개인 VPN 터널을 사용하는 경우 서버 측 인터넷 서비스 제공업체(ISP)의 업로드 속도가 클라이언트 측의 다운로드 속도의 병목 현상이 됩니다. VPN 클라이언트는 서버를 통해 데이터를 다운로드하기 때문입니다.

![tunnel](https://static.gl.inet.com/docs/router/en/4/faq/vpn_speed/tunnel.png){class="glboxshadow"}

## 프로토콜 차이

OpenVPN 또는 WireGuard와 같은 다른 VPN 프로토콜은 보안 및 속도가 다릅니다. 일부는 암호화 방법 때문에 느릴 수 있습니다.

## ISP 스로틀링

일부 인터넷 서비스 제공업체(ISP)는 VPN을 사용하는 사용자의 속도를 제한할 수 있으며, 특히 과도한 데이터 사용을 의심하는 경우에는 더욱 그렇습니다. 이는 특히 일부 개발도상국이나 많은 사용자가 제한된 인터넷 인프라를 공유하는 소도시에서 일반적입니다.

## DNS

일부 인터넷 서비스 제공업체(ISP)는 VPN 도메인을 확인하지 못할 수 있습니다. 라우터의 네트워크 설정에서 [암호화된 DNS](../interface_guide/dns.md#dns-server-settings)를 사용해 보세요.

## MTU

일부 인터넷 서비스 제공업체(ISP), 특히 모바일 통신사는 데이터 패킷 크기를 제한할 수 있습니다. VPN 클라이언트 옵션에서 기본 MTU를 1420에서 1380 또는 1280으로 변경해 보세요.

펌웨어 v4.8 이상의 경우 [여기](../interface_guide/vpn_dashboard.md/#tunnel-options)를 참조하세요.

펌웨어 v4.7 이하의 경우 [여기](../interface_guide/vpn_dashboard_v4.7.md#vpn-client-options)를 참조하세요.

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}을 통해 연락하세요.
