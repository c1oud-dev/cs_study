---
layout: default
title: "네트워크 면접 대비 — 완전 정리"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>네트워크 면접 대비 — 기본·심화 Q&A + 개념 요약</h2>
  <p>구성: ① 기본 면접 Q&A → ② 심화 면접 Q&A → ③ 추가 예상 질문 Q&A → ④ 네트워크 개념 요약 노트</p>
</section>

<!-- ① 기본 면접 Q&A -->
<details open>
  <summary><span class="accordion-title">📋 기본 면접 Q&A</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <details>
    <summary style="font-size:1rem;"><b>Q1. OSI 7계층 모델을 설명하고 각 계층의 역할을 말해주세요.</b></summary>
    <div class="accordion-content">
      <p>OSI 7계층은 네트워크 통신을 7개의 논리적 계층으로 나눈 참조 모델입니다. 물리 계층은 실제 전기적 신호 전송을 담당하고, 데이터 링크 계층은 인접한 노드 간 신뢰성 있는 전송을 보장합니다. 네트워크 계층은 IP 주소를 이용한 라우팅을 수행하고, 전송 계층은 TCP/UDP를 통해 종단 간 연결을 관리합니다. 세션 계층은 대화 관리, 표현 계층은 데이터 암호화와 압축, 응용 계층은 사용자에게 네트워크 서비스를 제공합니다. 각 계층은 독립적으로 동작하며 하위 계층의 서비스를 이용합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q2. TCP와 UDP의 차이점을 상세히 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>TCP는 연결 지향 프로토콜로 3-way handshake를 통해 연결을 설정하고, 신뢰성 있는 데이터 전송을 보장합니다. 순서 보장, 오류 검출 및 재전송, 흐름 제어, 혼잡 제어 기능을 제공하여 데이터 손실 없이 정확한 전송이 가능하지만 오버헤드가 큽니다. UDP는 비연결형 프로토콜로 연결 설정 과정 없이 바로 데이터를 전송합니다. 빠르고 간단하지만 신뢰성을 보장하지 않으며, 순서가 바뀌거나 데이터가 손실될 수 있습니다. 실시간 스트리밍이나 DNS 조회 같은 빠른 응답이 중요한 서비스에 적합합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q3. HTTP와 HTTPS의 차이점과 HTTPS의 동작 원리를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>HTTP는 웹에서 데이터를 주고받는 프로토콜이지만 데이터가 평문으로 전송되어 보안에 취약합니다. HTTPS는 HTTP에 SSL/TLS 암호화를 추가한 보안 프로토콜입니다. 클라이언트가 서버에 연결 요청을 하면, 서버는 인증서를 전송하고 클라이언트는 이를 검증합니다. 그 다음 대칭키를 안전하게 교환하고, 이후 모든 통신은 이 대칭키로 암호화됩니다. 공개키 암호화로 초기 키 교환을 하고, 실제 데이터는 대칭키 암호화로 처리하여 보안과 성능을 모두 확보합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q4. IP 주소와 서브넷 마스크의 개념을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>IP 주소는 네트워크에서 각 장치를 식별하는 고유한 논리적 주소입니다. IPv4는 32비트로 구성되며 점으로 구분된 4개의 10진수로 표현합니다. 서브넷 마스크는 IP 주소에서 네트워크 부분과 호스트 부분을 구분하는 역할을 합니다. 예를 들어 192.168.1.10/24에서 /24는 앞의 24비트가 네트워크 주소임을 의미합니다. 서브네팅을 통해 큰 네트워크를 작은 단위로 나누어 관리할 수 있고, 브로드캐스트 도메인을 분리하여 네트워크 효율성을 높일 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q5. DNS의 동작 원리와 레코드 타입들을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>DNS는 도메인 이름을 IP 주소로 변환하는 시스템입니다. 사용자가 도메인을 입력하면 로컬 DNS 서버에 먼저 질의하고, 캐시에 없으면 루트 DNS 서버부터 시작해서 TLD 서버, 권한 있는 DNS 서버 순으로 재귀적 또는 반복적 질의를 수행합니다. 주요 레코드 타입으로는 A 레코드(IPv4 주소), AAAA 레코드(IPv6 주소), CNAME 레코드(별칭), MX 레코드(메일 서버), NS 레코드(네임서버), TXT 레코드(텍스트 정보) 등이 있습니다. DNS 캐싱을 통해 응답 시간을 단축하고 서버 부하를 줄입니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q6. 라우팅과 스위칭의 차이점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>스위칭은 2계층(데이터 링크 계층)에서 MAC 주소를 기반으로 같은 네트워크 내에서 프레임을 전달하는 과정입니다. 스위치는 MAC 주소 테이블을 학습하여 유니캐스트 트래픽을 해당 포트로만 전송하고, 브로드캐스트는 모든 포트로 전송합니다. 라우팅은 3계층(네트워크 계층)에서 IP 주소를 기반으로 서로 다른 네트워크 간에 패킷을 전달하는 과정입니다. 라우터는 라우팅 테이블을 참조하여 최적 경로를 선택하고, 정적 라우팅 또는 동적 라우팅 프로토콜을 사용합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q7. ARP(Address Resolution Protocol)의 동작 과정을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>ARP는 IP 주소를 MAC 주소로 변환하는 프로토콜입니다. 호스트가 같은 서브넷의 다른 호스트와 통신하려고 할 때, 목적지 IP 주소의 MAC 주소를 알아야 합니다. 먼저 ARP 캐시 테이블을 확인하고, 없으면 ARP Request를 브로드캐스트로 전송합니다. 해당 IP를 가진 호스트가 자신의 MAC 주소를 담은 ARP Reply를 유니캐스트로 응답합니다. 받은 정보를 ARP 캐시에 저장하여 일정 시간 동안 재사용합니다. 이를 통해 IP 패킷을 이더넷 프레임으로 캡슐화할 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q8. DHCP의 동작 과정을 4단계로 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>DHCP는 네트워크 장치에 자동으로 IP 주소와 네트워크 설정을 할당하는 프로토콜입니다. 첫 번째 단계인 Discover에서 클라이언트가 DHCP 서버를 찾기 위해 브로드캐스트로 요청을 보냅니다. 두 번째 Offer 단계에서 DHCP 서버가 사용 가능한 IP 주소와 설정 정보를 제안합니다. 세 번째 Request 단계에서 클라이언트가 제안받은 설정을 사용하겠다고 요청합니다. 마지막 ACK 단계에서 서버가 확인 응답을 보내면 클라이언트는 해당 IP 주소와 설정을 사용하기 시작합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q9. NAT(Network Address Translation)의 종류와 동작 원리를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>NAT는 사설 IP 주소를 공인 IP 주소로 변환하는 기술입니다. Static NAT는 사설 IP와 공인 IP를 1:1로 고정 매핑하고, Dynamic NAT는 사설 IP를 공인 IP 풀에서 동적으로 할당합니다. PAT(Port Address Translation)는 포트 번호를 이용하여 하나의 공인 IP로 여러 사설 IP를 지원합니다. 내부에서 외부로 패킷이 나갈 때 소스 IP와 포트를 변환하고 NAT 테이블에 기록합니다. 외부에서 응답이 오면 NAT 테이블을 참조하여 원래 내부 IP와 포트로 변환하여 전달합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q10. 로드 밸런싱의 종류와 알고리즘들을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>로드 밸런싱은 여러 서버에 트래픽을 분산하여 가용성과 성능을 향상시키는 기술입니다. L4 로드 밸런서는 IP와 포트 정보를 기반으로 분산하고, L7 로드 밸런서는 HTTP 헤더나 쿠키 같은 응용 계층 정보를 활용합니다. 주요 알고리즘으로는 Round Robin(순차 분배), Weighted Round Robin(가중치 기반 분배), Least Connections(최소 연결 수 기준), IP Hash(클라이언트 IP 해시 기반) 등이 있습니다. 헬스 체크 기능으로 장애 서버를 자동으로 제외하고, 세션 지속성을 통해 같은 클라이언트를 동일 서버로 연결할 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q11. VLAN의 개념과 장점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>VLAN(Virtual LAN)은 물리적으로 연결된 네트워크를 논리적으로 분할하는 기술입니다. 스위치 포트를 그룹화하여 각 그룹이 독립된 브로드캐스트 도메인을 형성합니다. Tag VLAN은 이더넷 헤더에 VLAN ID를 추가하여 여러 VLAN 트래픽을 하나의 링크로 전송할 수 있게 합니다. 주요 장점으로는 브로드캐스트 트래픽 감소, 보안 향상, 네트워크 관리 유연성 증가, 물리적 제약 없는 그룹 구성이 있습니다. 트렁크 포트를 통해 여러 VLAN 간 통신이 가능하며, 라우터나 L3 스위치로 VLAN 간 라우팅을 수행합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q12. 방화벽의 종류와 동작 방식을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>방화벽은 네트워크 보안을 위해 트래픽을 제어하는 시스템입니다. 패킷 필터링 방화벽은 IP 헤더 정보(소스/목적지 IP, 포트)로 패킷을 차단하거나 허용합니다. 상태 추적 방화벽은 연결 상태를 기억하여 동적으로 규칙을 적용하고, 응용 계층 게이트웨이는 특정 프로토콜의 내용까지 분석합니다. 차세대 방화벽은 DPI(Deep Packet Inspection), IPS 기능, 사용자 인증 등을 통합 제공합니다. 방화벽 정책은 기본적으로 deny-all 원칙을 따르고, 필요한 트래픽만 명시적으로 허용하는 화이트리스트 방식을 사용합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q13. VPN의 종류와 터널링 기술을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>VPN은 공중망을 통해 안전한 사설망 연결을 제공하는 기술입니다. Site-to-Site VPN은 지사 간 연결에 사용하고, Remote Access VPN은 개별 사용자의 원격 접속에 활용합니다. 터널링 프로토콜로는 PPTP(간단하지만 보안 취약), L2TP/IPSec(강력한 보안), SSL VPN(웹 브라우저 기반 접근), OpenVPN(오픈소스 솔루션) 등이 있습니다. 터널링은 원본 패킷을 암호화하고 새로운 IP 헤더로 감싸서 전송하며, 목적지에서 복호화하여 원본 패킷을 복원합니다. 인증, 암호화, 무결성 검증을 통해 보안을 보장합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q14. QoS(Quality of Service)의 개념과 구현 방법을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>QoS는 네트워크에서 특정 트래픽에 우선순위를 부여하여 서비스 품질을 보장하는 기술입니다. 대역폭, 지연시간, 지터, 패킷 손실률 등의 네트워크 성능 지표를 관리합니다. 구현 방법으로는 트래픽 분류(Classification), 마킹(Marking), 큐잉(Queuing), 셰이핑(Shaping), 폴리싱(Policing)이 있습니다. IntServ는 경로상의 모든 라우터에서 자원을 예약하는 방식이고, DiffServ는 패킷에 DSCP 값을 설정하여 홉별로 차등 서비스를 제공합니다. 음성, 영상 같은 실시간 트래픽은 높은 우선순위를, 파일 전송 같은 트래픽은 낮은 우선순위를 부여합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q15. CDN(Content Delivery Network)의 동작 원리와 장점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>CDN은 전 세계에 분산된 캐시 서버를 통해 콘텐츠를 사용자와 가까운 위치에서 제공하는 서비스입니다. 사용자가 웹사이트에 접속하면 DNS를 통해 가장 가까운 엣지 서버로 리다이렉트됩니다. 캐시에 콘텐츠가 있으면 즉시 응답하고, 없으면 원본 서버에서 가져와 캐시한 후 응답합니다. 주요 장점으로는 응답 시간 단축, 원본 서버 부하 감소, 대역폭 비용 절감, 가용성 향상이 있습니다. 정적 콘텐츠(이미지, CSS, JS)는 물론 동적 콘텐츠나 스트리밍 서비스도 지원하며, DDoS 공격 완화 효과도 제공합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q16. SSL/TLS 핸드셰이크 과정을 단계별로 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>SSL/TLS 핸드셰이크는 클라이언트와 서버가 안전한 통신을 위해 암호화 파라미터를 협상하는 과정입니다. 클라이언트가 Client Hello 메시지로 지원하는 암호화 방식을 서버에 알립니다. 서버는 Server Hello로 선택한 암호화 방식과 인증서를 전송합니다. 클라이언트는 인증서를 검증하고 Pre-Master Secret을 서버의 공개키로 암호화하여 전송합니다. 양측이 Pre-Master Secret으로부터 대칭키를 생성하고, Finished 메시지를 교환하여 핸드셰이크를 완료합니다. 이후 모든 애플리케이션 데이터는 협상된 대칭키로 암호화됩니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q17. HTTP/2와 HTTP/1.1의 차이점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>HTTP/2는 HTTP/1.1의 성능 문제를 해결하기 위해 개발된 프로토콜입니다. 가장 큰 차이점은 멀티플렉싱으로, 하나의 TCP 연결에서 여러 요청을 동시에 처리할 수 있어 Head-of-Line Blocking 문제를 해결합니다. 헤더 압축을 통해 중복되는 헤더 정보를 압축하여 대역폭을 절약하고, 서버 푸시 기능으로 클라이언트 요청 전에 미리 리소스를 전송할 수 있습니다. 바이너리 프레이밍을 사용하여 파싱 효율성을 높이고, 스트림 우선순위를 통해 중요한 리소스를 먼저 전송할 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q18. 웹소켓(WebSocket)의 특징과 HTTP와의 차이점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>웹소켓은 클라이언트와 서버 간 양방향 실시간 통신을 제공하는 프로토콜입니다. HTTP와 달리 연결이 한 번 수립되면 지속적으로 유지되며, 양쪽에서 언제든 데이터를 전송할 수 있습니다. HTTP는 요청-응답 방식의 반이중 통신이지만, 웹소켓은 전이중 통신이 가능합니다. 초기 연결은 HTTP 업그레이드를 통해 이루어지고, 이후에는 웹소켓 프로토콜로 통신합니다. 채팅, 게임, 주식 시세, 협업 도구 등 실시간 상호작용이 필요한 애플리케이션에 적합하며, 폴링 방식보다 효율적입니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q19. 쿠키(Cookie)와 세션(Session)의 차이점과 보안 고려사항을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>쿠키는 클라이언트 브라우저에 저장되는 작은 데이터 조각으로, 서버가 클라이언트의 상태를 유지하기 위해 사용합니다. 세션은 서버에 저장되는 사용자 정보로, 보통 세션 ID만 쿠키에 저장합니다. 쿠키는 클라이언트에서 조작 가능하여 보안에 취약하고, 세션은 서버에 저장되어 더 안전하지만 서버 메모리를 사용합니다. 보안 고려사항으로는 HttpOnly 플래그로 XSS 공격 방지, Secure 플래그로 HTTPS에서만 전송, SameSite 속성으로 CSRF 공격 방지, 적절한 만료시간 설정 등이 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q20. 포트 번호의 분류와 잘 알려진 포트들을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>포트 번호는 0-65535 범위에서 세 그룹으로 분류됩니다. Well-known 포트(0-1023)는 시스템 서비스용으로 예약되어 있고, Registered 포트(1024-49151)는 특정 애플리케이션용으로 등록된 포트, Dynamic 포트(49152-65535)는 임시로 사용되는 포트입니다. 주요 well-known 포트로는 HTTP(80), HTTPS(443), FTP(21), SSH(22), Telnet(23), SMTP(25), DNS(53), DHCP(67/68), POP3(110), IMAP(143), SNMP(161) 등이 있습니다. 애플리케이션은 포트 번호를 통해 동시에 여러 서비스를 구분하여 제공할 수 있습니다.</p>
    </div>
  </details>

  </div>
</details>

<!-- ② 심화 면접 Q&A -->
<details>
  <summary><span class="accordion-title">🚀 심화 면접 Q&A</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <details>
    <summary style="font-size:1rem;"><b>Q21. BGP(Border Gateway Protocol)의 동작 원리와 AS(Autonomous System)의 개념을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>BGP는 인터넷의 서로 다른 AS 간에 라우팅 정보를 교환하는 프로토콜입니다. AS는 단일 관리 정책하에 운영되는 라우터들의 집합으로, 각각 고유한 AS 번호를 가집니다. BGP는 경로 벡터 알고리즘을 사용하여 목적지까지의 AS 경로 정보를 유지하고, 루프 방지를 위해 자신의 AS가 경로에 포함된 경우 해당 경로를 거부합니다. iBGP는 같은 AS 내부에서, eBGP는 서로 다른 AS 간에 사용됩니다. 경로 선택 시 AS-Path 길이, Origin, Local Preference 등의 속성을 고려하여 최적 경로를 결정합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q22. MPLS(Multiprotocol Label Switching)의 동작 원리와 장점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>MPLS는 패킷에 레이블을 부착하여 빠른 스위칭을 제공하는 기술입니다. 패킷이 MPLS 네트워크에 진입할 때 LER(Label Edge Router)이 FEC(Forwarding Equivalence Class)에 따라 레이블을 부착합니다. LSR(Label Switch Router)들은 IP 헤더를 분석하지 않고 레이블만으로 빠른 포워딩을 수행합니다. 출구에서 다시 레이블을 제거하고 일반 IP 패킷으로 전송합니다. 장점으로는 빠른 포워딩 속도, QoS 지원, Traffic Engineering, VPN 구축 용이성이 있으며, 특히 ISP 백본 네트워크에서 많이 사용됩니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q23. STP(Spanning Tree Protocol)와 RSTP의 차이점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>STP는 스위치 네트워크에서 루프를 방지하기 위한 프로토콜입니다. 모든 스위치 중 하나를 Root Bridge로 선정하고, 각 스위치는 Root Bridge로의 최단 경로를 계산합니다. 포트 상태는 Blocking, Listening, Learning, Forwarding으로 변화하며, 컨버전스 시간이 50초 정도 걸립니다. RSTP는 STP의 개선 버전으로 컨버전스 시간을 대폭 단축했습니다. 포트 역할을 더 세분화하고(Root, Designated, Alternate, Backup), P2P 링크에서는 즉시 Forwarding 상태로 전환할 수 있어 서브초 단위의 빠른 복구가 가능합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q24. SDN(Software Defined Network)의 개념과 OpenFlow 프로토콜을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>SDN은 네트워크의 제어 평면과 데이터 평면을 분리하여 중앙집중식으로 네트워크를 관리하는 아키텍처입니다. 컨트롤러가 전체 네트워크의 토폴로지를 파악하고 최적의 경로를 계산하여 각 스위치에 플로우 테이블을 설정합니다. OpenFlow는 컨트롤러와 스위치 간의 통신 프로토콜로, 플로우 규칙을 전달하고 통계 정보를 수집합니다. 플로우 테이블은 매치 필드, 액션, 우선순위로 구성되어 있으며, 패킷이 매치되지 않으면 컨트롤러에게 문의합니다. 네트워크 프로그래밍이 가능하고 중앙집중 관리로 일관된 정책 적용이 장점입니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q25. IPv6의 특징과 IPv4에서의 전환 방법들을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>IPv6는 128비트 주소 공간을 제공하여 주소 부족 문제를 해결하고, 헤더 구조를 단순화하여 처리 효율성을 높였습니다. IPSec이 필수 구현되어 보안이 강화되고, 자동 설정 기능으로 DHCP 없이도 주소 할당이 가능합니다. 전환 방법으로는 Dual Stack(IPv4/IPv6 동시 운영), 터널링(IPv6 패킷을 IPv4로 캡슐화), 변환(NAT64/DNS64)이 있습니다. 주소 표기법은 콜론으로 구분된 16진수를 사용하고, 연속된 0은 ::로 축약할 수 있습니다. 멀티캐스트가 기본이고 브로드캐스트는 없으며, Neighbor Discovery로 ARP를 대체합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q26. 네트워크 보안에서 IDS와 IPS의 차이점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>IDS(Intrusion Detection System)는 네트워크나 시스템에 대한 침입을 탐지하고 알림을 제공하는 시스템입니다. 패시브 방식으로 동작하여 침입을 탐지만 하고 차단하지는 않습니다. NIDS는 네트워크 트래픽을 모니터링하고, HIDS는 호스트 시스템을 감시합니다. IPS(Intrusion Prevention System)는 IDS의 탐지 기능에 능동적 차단 기능을 추가한 시스템입니다. 인라인으로 배치되어 실시간으로 악성 트래픽을 차단하며, 오탐으로 인한 정상 트래픽 차단 위험이 있습니다. 시그니처 기반과 이상 행위 기반 탐지 방법을 사용합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q27. 네트워크 가상화 기술인 VXLAN의 동작 원리를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>VXLAN(Virtual eXtensible LAN)은 L2 이더넷 프레임을 UDP 패킷으로 캡슐화하여 L3 네트워크 위에서 L2 연결성을 제공하는 터널링 기술입니다. 24비트 VNI(VXLAN Network Identifier)를 사용하여 최대 1600만 개의 논리적 네트워크를 구성할 수 있어 기존 VLAN의 4096개 제한을 극복합니다. VTEP(VXLAN Tunnel Endpoint)는 캡슐화와 역캡슐화를 담당하며, 멀티캐스트나 컨트롤 플레인을 통해 원격 VTEP를 학습합니다. 클라우드 환경에서 테넌트 격리와 확장성을 제공하며, 물리적 위치에 관계없이 논리적 네트워크를 구성할 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q28. 마이크로서비스 아키텍처에서의 서비스 메시(Service Mesh)를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>서비스 메시는 마이크로서비스 간의 네트워크 통신을 관리하는 인프라 계층입니다. 각 서비스에 사이드카 프록시를 배치하여 모든 네트워크 트래픽을 가로채고 제어합니다. 서비스 디스커버리, 로드 밸런싱, 장애 복구, 보안, 모니터링 기능을 애플리케이션 코드와 분리하여 제공합니다. 데이터 플레인(사이드카 프록시)과 컨트롤 플레인(관리 서버)으로 구성되며, Istio, Linkerd, Consul Connect 등이 대표적입니다. mTLS를 통한 서비스 간 암호화, 정책 기반 접근 제어, 분산 추적을 통한 관찰성을 제공합니다.</p>
    </div>
  </details>

  </div>
</details>

<!-- ③ 추가 예상 질문 Q&A -->
<details>
  <summary><span class="accordion-title">💡 추가 예상 질문 Q&A</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <details>
    <summary style="font-size:1rem;"><b>Q29. HTTP/3과 QUIC 프로토콜의 특징을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>HTTP/3은 QUIC 프로토콜 위에서 동작하는 차세대 HTTP 프로토콜입니다. QUIC는 UDP 기반으로 설계되어 TCP의 Head-of-Line Blocking 문제를 완전히 해결합니다. 0-RTT 연결 설정으로 첫 요청부터 데이터를 전송할 수 있고, 연결 마이그레이션을 지원하여 네트워크가 변경되어도 연결이 유지됩니다. 패킷 레벨에서 암호화가 내장되어 보안이 강화되고, 스트림별 독립적인 플로우 제어와 혼잡 제어를 제공합니다. NAT나 방화벽 통과가 용이하고, 모바일 환경에서 성능 향상이 두드러집니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q30. 네트워크 모니터링 도구와 성능 지표들을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>네트워크 모니터링은 대역폭 사용률, 패킷 손실률, 지연시간, 지터를 주요 지표로 측정합니다. SNMP를 통해 네트워크 장비의 상태 정보를 수집하고, sFlow나 NetFlow로 트래픽 패턴을 분석합니다. 핑(ping)으로 연결성과 RTT를 측정하고, 트레이스라우트(traceroute)로 경로를 추적합니다. 포트 미러링이나 TAP을 통해 실제 트래픽을 캡처하여 프로토콜 분석을 수행합니다. Wireshark, PRTG, Nagios, Zabbix 등의 도구가 사용되며, 실시간 모니터링과 알람을 통해 네트워크 장애를 조기에 발견할 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q31. 5G 네트워크의 핵심 기술과 특징을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>5G는 eMBB(대용량), URLLC(초저지연), mMTC(대규모 연결)의 세 가지 주요 서비스 시나리오를 지원합니다. 네트워크 슬라이싱으로 하나의 물리 인프라에서 여러 논리적 네트워크를 제공하고, 엣지 컴퓨팅으로 지연시간을 최소화합니다. Massive MIMO와 빔포밍으로 스펙트럼 효율성을 높이고, mmWave 주파수로 초고속 전송을 지원합니다. NFV와 SDN을 활용하여 네트워크 기능을 소프트웨어화하고, 클라우드 네이티브 아키텍처로 유연성과 확장성을 제공합니다. 최대 20Gbps 속도, 1ms 이하 지연시간, km²당 100만 개 기기 연결을 목표로 합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q32. DoH(DNS over HTTPS)와 DoT(DNS over TLS)의 차이점과 보안상 이점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>기존 DNS는 평문으로 전송되어 도청과 조작에 취약했습니다. DoT는 TLS로 DNS 쿼리를 암호화하여 853번 포트를 사용하고, DoH는 HTTPS를 통해 DNS 쿼리를 전송하여 443번 포트를 사용합니다. DoH는 일반 웹 트래픽과 구분하기 어려워 차단이 어렵지만, DoT는 전용 포트를 사용하여 네트워크 관리가 용이합니다. 두 방식 모두 DNS 프라이버시를 보호하고 중간자 공격을 방지하며, DNS 하이재킹과 DNS 스푸핑을 차단합니다. 그러나 기업 환경에서는 DNS 필터링이 어려워질 수 있어 정책적 고려가 필요합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q33. 제로 트러스트 네트워크 보안 모델을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>제로 트러스트는 "믿지 말고 검증하라"는 원칙 하에 모든 네트워크 트래픽을 의심하고 지속적으로 검증하는 보안 모델입니다. 기존의 경계 기반 보안에서 벗어나 사용자, 기기, 애플리케이션을 모두 검증합니다. 최소 권한 원칙을 적용하여 필요한 최소한의 접근만 허용하고, 마이크로 세그멘테이션으로 네트워크를 세분화합니다. 지속적인 모니터링과 행동 분석을 통해 비정상적인 활동을 탐지하고, 동적 접근 제어로 위험도에 따라 권한을 조정합니다. 클라우드와 원격 근무 환경의 증가로 더욱 중요해지고 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q34. 네트워크 자동화와 NetOps/AIOps의 개념을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>네트워크 자동화는 반복적인 네트워크 관리 작업을 스크립트나 도구로 자동화하는 것입니다. 설정 배포, 백업, 모니터링, 문제 해결을 자동화하여 운영 효율성을 높이고 인적 오류를 줄입니다. NetOps는 DevOps 원칙을 네트워크 운영에 적용한 것으로, 네트워크를 코드로 관리(Infrastructure as Code)하고 CI/CD 파이프라인을 활용합니다. AIOps는 인공지능과 머신러닝을 활용하여 네트워크 이상을 자동 탐지하고, 예측적 유지보수를 수행하며, 자동 복구 기능을 제공합니다. Ansible, Puppet, Terraform 등의 도구가 사용됩니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q35. Edge Computing과 MEC(Multi-access Edge Computing)의 개념을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>엣지 컴퓨팅은 데이터 처리를 클라우드가 아닌 데이터 소스에 가까운 곳에서 수행하는 분산 컴퓨팅 패러다임입니다. 지연시간을 줄이고 대역폭 사용량을 절약하며, 데이터 프라이버시를 향상시킵니다. MEC는 모바일 네트워크에서 기지국이나 집합 포인트에 컴퓨팅 자원을 배치하는 기술입니다. 5G 네트워크와 결합하여 초저지연 서비스를 제공하고, AR/VR, 자율주행, 산업용 IoT 등의 실시간 애플리케이션을 지원합니다. CDN과 달리 단순 캐싱이 아닌 실제 연산 처리가 가능하며, 네트워크 슬라이싱과 함께 맞춤형 서비스를 제공합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q36. 블록체인 네트워크의 합의 알고리즘과 네트워킹 특징을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>블록체인은 P2P 네트워크에서 분산 원장을 유지하는 시스템입니다. PoW(Proof of Work)는 연산량으로 합의하지만 에너지 소모가 크고, PoS(Proof of Stake)는 지분 기반으로 효율적이며, DPoS(Delegated PoS)는 대표자를 통해 빠른 처리가 가능합니다. 네트워킹 측면에서는 가십 프로토콜로 트랜잭션과 블록을 전파하고, 풀 노드와 라이트 노드로 역할을 구분합니다. 네트워크 파티션 공격, 51% 공격 등의 보안 위협이 있으며, 확장성 문제 해결을 위해 샤딩, 라이트닝 네트워크 등의 기술이 연구되고 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q37. 네트워크 테스팅과 검증 방법들을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>네트워크 테스팅은 성능, 기능, 보안 측면에서 수행됩니다. 성능 테스트는 처리량, 지연시간, 패킷 손실률을 측정하고, 로드 테스트로 최대 용량을 확인합니다. 기능 테스트는 라우팅, 스위칭, VLAN, QoS 등의 기능이 정상 동작하는지 검증합니다. 보안 테스트는 취약점 스캐닝, 침투 테스트, DoS 공격 시뮬레이션을 포함합니다. 네트워크 에뮬레이터(GNS3, EVE-NG)로 가상 환경에서 테스트하고, Chaos Engineering으로 장애 상황을 시뮬레이션합니다. 자동화된 테스트 스위트로 지속적인 검증을 수행하고, A/B 테스팅으로 설정 변경의 영향을 측정합니다.</p>
    </div>
  </details>

  </div>
</details>

<!-- ④ 네트워크 개념 요약 노트 -->
<details>
  <summary><span class="accordion-title">📚 네트워크 개념 요약 노트</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <h3>🏗️ 네트워크 아키텍처</h3>
  <p><b>OSI 7계층</b></p>
  <pre><code>7. 응용 계층 (Application) - HTTP, FTP, SMTP
6. 표현 계층 (Presentation) - 암호화, 압축
5. 세션 계층 (Session) - 연결 관리
4. 전송 계층 (Transport) - TCP, UDP
3. 네트워크 계층 (Network) - IP, ICMP, ARP
2. 데이터링크 계층 (Data Link) - Ethernet, WiFi
1. 물리 계층 (Physical) - 케이블, 전기신호</code></pre>

  <p><b>TCP/IP 모델</b></p>
  <ul>
    <li>애플리케이션 계층 (HTTP, DNS, FTP)</li>
    <li>전송 계층 (TCP, UDP)</li>
    <li>인터넷 계층 (IP, ICMP, ARP)</li>
    <li>네트워크 액세스 계층 (Ethernet, WiFi)</li>
  </ul>

  <h3>🔄 프로토콜 비교</h3>
  <p><b>TCP vs UDP</b></p>
  <table>
    <thead>
      <tr><th>특성</th><th>TCP</th><th>UDP</th></tr>
    </thead>
    <tbody>
      <tr><td>연결성</td><td>연결지향</td><td>비연결형</td></tr>
      <tr><td>신뢰성</td><td>보장</td><td>보장 안함</td></tr>
      <tr><td>속도</td><td>느림</td><td>빠름</td></tr>
      <tr><td>오버헤드</td><td>높음</td><td>낮음</td></tr>
      <tr><td>용도</td><td>웹, 메일</td><td>게임, 스트리밍</td></tr>
    </tbody>
  </table>

  <p><b>HTTP 버전 비교</b></p>
  <ul>
    <li>HTTP/1.1: 지속연결, 파이프라이닝</li>
    <li>HTTP/2: 멀티플렉싱, 헤더압축, 서버푸시</li>
    <li>HTTP/3: QUIC 기반, 0-RTT, 연결마이그레이션</li>
  </ul>

  <h3>🌐 IP 주소 체계</h3>
  <p><b>IPv4 주소 클래스</b></p>
  <ul>
    <li>Class A: 1-126 (8비트 네트워크)</li>
    <li>Class B: 128-191 (16비트 네트워크)</li>
    <li>Class C: 192-223 (24비트 네트워크)</li>
    <li>사설 IP: 10.x.x.x, 172.16-31.x.x, 192.168.x.x</li>
  </ul>

  <p><b>서브넷팅 계산</b></p>
  <ul>
    <li>/24 = 255.255.255.0 (256개 주소)</li>
    <li>/25 = 255.255.255.128 (128개 주소)</li>
    <li>/26 = 255.255.255.192 (64개 주소)</li>
  </ul>

  <p><b>IPv6 특징</b></p>
  <ul>
    <li>128비트 주소 공간</li>
    <li>자동 설정 (SLAAC)</li>
    <li>IPSec 내장</li>
    <li>멀티캐스트 기본</li>
  </ul>

  <h3>📡 네트워크 장비</h3>
  <p><b>스위치 (Switch)</b></p>
  <ul>
    <li>L2에서 MAC 주소로 프레임 전송</li>
    <li>VLAN, STP, 포트 미러링 지원</li>
    <li>MAC 주소 테이블 학습</li>
  </ul>

  <p><b>라우터 (Router)</b></p>
  <ul>
    <li>L3에서 IP 주소로 패킷 라우팅</li>
    <li>라우팅 테이블, NAT, DHCP 기능</li>
    <li>정적/동적 라우팅 프로토콜</li>
  </ul>

  <p><b>방화벽 (Firewall)</b></p>
  <ul>
    <li>패킷 필터링, 상태추적</li>
    <li>응용계층 게이트웨이</li>
    <li>IPS/IDS 기능 통합</li>
  </ul>

  <h3>🔐 네트워크 보안</h3>
  <p><b>보안 프로토콜</b></p>
  <ul>
    <li>SSL/TLS: 웹 보안</li>
    <li>IPSec: VPN 보안</li>
    <li>SSH: 원격 접속 보안</li>
    <li>HTTPS: HTTP + TLS</li>
  </ul>

  <p><b>공격 유형</b></p>
  <ul>
    <li>DDoS: 분산 서비스 거부</li>
    <li>MITM: 중간자 공격</li>
    <li>ARP 스푸핑: MAC 주소 위조</li>
    <li>DNS 스푸핑: DNS 응답 조작</li>
  </ul>

  <p><b>보안 대책</b></p>
  <ul>
    <li>방화벽 + IPS/IDS</li>
    <li>VPN 암호화 터널</li>
    <li>네트워크 세그멘테이션</li>
    <li>보안 모니터링</li>
  </ul>

  <h3>⚡ 성능 최적화</h3>
  <p><b>QoS 구현</b></p>
  <ul>
    <li>분류 (Classification)</li>
    <li>마킹 (Marking)</li>
    <li>큐잉 (Queuing)</li>
    <li>쉐이핑 (Shaping)</li>
  </ul>

  <p><b>로드 밸런싱 알고리즘</b></p>
  <ul>
    <li>Round Robin: 순차 분배</li>
    <li>Weighted: 가중치 기반</li>
    <li>Least Connections: 최소 연결</li>
    <li>IP Hash: 클라이언트 IP 기반</li>
  </ul>

  <p><b>캐싱 전략</b></p>
  <ul>
    <li>CDN: 지리적 분산</li>
    <li>프록시 캐시: 중앙 집중</li>
    <li>브라우저 캐시: 클라이언트</li>
    <li>DNS 캐시: 이름 해석</li>
  </ul>

  <h3>🔧 네트워크 관리</h3>
  <p><b>모니터링 지표</b></p>
  <ul>
    <li>대역폭 사용률 (%)</li>
    <li>패킷 손실률 (%)</li>
    <li>지연시간 (ms)</li>
    <li>가용성 (uptime %)</li>
  </ul>

  <p><b>프로토콜별 포트</b></p>
  <table>
    <thead>
      <tr><th>서비스</th><th>포트</th><th>프로토콜</th></tr>
    </thead>
    <tbody>
      <tr><td>HTTP</td><td>80</td><td>TCP</td></tr>
      <tr><td>HTTPS</td><td>443</td><td>TCP</td></tr>
      <tr><td>DNS</td><td>53</td><td>UDP/TCP</td></tr>
      <tr><td>SSH</td><td>22</td><td>TCP</td></tr>
      <tr><td>FTP</td><td>21</td><td>TCP</td></tr>
      <tr><td>SMTP</td><td>25</td><td>TCP</td></tr>
    </tbody>
  </table>

  <p><b>네트워크 명령어</b></p>
  <ul>
    <li>ping: 연결 테스트</li>
    <li>traceroute: 경로 추적</li>
    <li>nslookup: DNS 조회</li>
    <li>netstat: 연결 상태</li>
    <li>tcpdump: 패킷 캡처</li>
  </ul>

  <h3>🚀 최신 기술 동향</h3>
  <p><b>클라우드 네트워킹</b></p>
  <ul>
    <li>VPC (Virtual Private Cloud)</li>
    <li>서비스 메시 (Service Mesh)</li>
    <li>컨테이너 네트워킹 (CNI)</li>
    <li>멀티 클라우드 연결</li>
  </ul>

  <p><b>네트워크 자동화</b></p>
  <ul>
    <li>SDN (Software Defined Network)</li>
    <li>NFV (Network Function Virtualization)</li>
    <li>인프라스트럭처 as 코드</li>
    <li>NetOps/AIOps</li>
  </ul>

  <p><b>엣지 컴퓨팅</b></p>
  <ul>
    <li>CDN 진화</li>
    <li>MEC (Multi-access Edge Computing)</li>
    <li>5G + 엣지</li>
    <li>IoT 엣지 게이트웨이</li>
  </ul>

  <h3>🎯 트러블슈팅 가이드</h3>
  <p><b>네트워크 장애 분류</b></p>
  <ol>
    <li>물리적 장애: 케이블, 포트 문제</li>
    <li>설정 오류: IP, 라우팅 설정</li>
    <li>성능 저하: 대역폭, 지연시간</li>
    <li>보안 문제: 방화벽, 접근제어</li>
  </ol>

  <p><b>계층별 문제 해결</b></p>
  <ul>
    <li>L1: 링크 상태, 케이블 확인</li>
    <li>L2: MAC 주소, VLAN, STP</li>
    <li>L3: IP 주소, 라우팅 테이블</li>
    <li>L4: 포트, 방화벽 규칙</li>
    <li>L7: 애플리케이션 로그</li>
  </ul>

  <h3>💡 면접 팁</h3>
  <ol>
    <li><b>OSI 7계층을 정확히 암기</b>하고 각 계층의 역할과 프로토콜 설명</li>
    <li><b>실무 경험과 연결</b>하여 구체적인 예시 제시</li>
    <li><b>성능과 보안</b>을 항상 함께 고려한 답변</li>
    <li><b>최신 기술 동향</b>에 대한 관심과 이해 표현</li>
    <li><b>계층별 접근법</b>으로 체계적인 문제 해결 능력 어필</li>
    <li><b>실제 네트워크 구축 경험</b>이나 트러블슈팅 사례 활용</li>
  </ol>

  </div>
</details>
