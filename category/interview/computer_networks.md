---
layout: default
title: "네트워크 면접 대비 — 완전 정리"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>네트워크 면접 대비</h2>
  <p>구성: 기본 면접 Q&A → 심화 면접 Q&A → 추가 예상 질문 Q&A → 네트워크 개념 요약 노트</p>
</section>

<!-- ① 기본 면접 Q&A -->
<details open>
  <summary><span class="accordion-title">📋 기본 면접 Q&A</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <details>
    <summary style="font-size:1rem;"><b>Q1. OSI 7계층 모델을 설명하고 각 계층의 역할을 말해주세요.</b></summary>
    <div class="accordion-content">
      <p>OSI 7계층은 네트워크 통신을 7개의 논리적 계층으로 나눈 참조 모델입니다. 물리 계층은 실제 전기적 신호 전송을 담당하고, 데이터 링크 계층은 인접한 노드 간 신뢰성 있는 전송을 보장합니다. 네트워크 계층은 IP 주소를 이용한 라우팅을 수행하고, 전송 계층은 TCP/UDP를 통해 종단 간 연결을 관리합니다. 세션 계층은 대화 관리, 표현 계층은 데이터 암호화와 압축, 응용 계층은 사용자에게 네트워크 서비스를 제공합니다. 각 계층은 독립적으로 동작하며 하위 계층의 서비스를 이용합니다.</p>
      <hr>
      <h4>💡 OSI 7계층</h4>
      <img
        src="https://github.com/user-attachments/assets/00ec0ea3-b0b0-4967-ac54-b2edd3e66683"
        alt="OSI 7계층"
        width="720" height="363" loading="lazy"
        style="max-width:100%; height:auto; display:inline-block;"
      />
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q2. TCP와 UDP의 차이점을 상세히 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>TCP는 연결 지향 프로토콜로 3-way handshake를 통해 연결을 설정하고, 신뢰성 있는 데이터 전송을 보장합니다. 순서 보장, 오류 검출 및 재전송, 흐름 제어, 혼잡 제어 기능을 제공하여 데이터 손실 없이 정확한 전송이 가능하지만 오버헤드가 큽니다. UDP는 비연결형 프로토콜로 연결 설정 과정 없이 바로 데이터를 전송합니다. 빠르고 간단하지만 신뢰성을 보장하지 않으며, 순서가 바뀌거나 데이터가 손실될 수 있습니다. 실시간 스트리밍이나 DNS 조회 같은 빠른 응답이 중요한 서비스에 적합합니다.</p>
    <hr>
    <h4>💡 3-way handshake</h4>
    <p>TCP 연결을 만들 때 서로 준비됐는지 3번 신호를 주고받는 절차</p>
      <ul>
        <li><b>SYN</b> — 클라이언트 → 서버</li>
        <li><b>SYN-ACK</b> — 서버 → 클라이언트</li>
        <li><b>ACK</b> — 클라이언트 → 서버</li>
        <li><b>왜 3번인가?</b></li>
          <ul>
            <li>둘 다 송수신이 가능한지와 서로의 초기 시퀀스 번호를 서로 확인해야 해서 2번으론 부족하다.</li>
          </ul>
        <li><b>핵심 효과</b></li>
          <ul>
            <li>연결 확립, 번호 동기화(세션 식별/순서 보장), 초기 유효성 확인.</li>
          </ul>
      </ul>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q3. HTTP와 HTTPS의 차이점과 HTTPS의 동작 원리를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>HTTP는 웹에서 데이터를 주고받는 프로토콜이지만 데이터가 평문으로 전송되어 보안에 취약합니다. HTTPS는 HTTP에 SSL/TLS 암호화를 추가한 보안 프로토콜입니다. 클라이언트가 서버에 연결 요청을 하면, 서버는 인증서를 전송하고 클라이언트는 이를 검증합니다. 그 다음 대칭키를 안전하게 교환하고, 이후 모든 통신은 이 대칭키로 암호화됩니다. 공개키 암호화로 초기 키 교환을 하고, 실제 데이터는 대칭키 암호화로 처리하여 보안과 성능을 모두 확보합니다.</p>
      <hr>
      <h4>💡 SSL/TLS 암호화</h4>
      <p>HTTPS의 SSL/TLS는 브라우저–서버 사이 트래픽을 암호화해서 도청/변조/위장을 막는 기술</p>
      <ul>
        <li><b>핵심 원리</b></li>
        <ol>
          <li>서버 인증서로 진짜 서버인지 확인(CA가 서명)</li>
          <li>비대칭키(공개키)로 세션키를 안전하게 합의</li>
          <li>합의된 세션키(대칭키)로 실제 데이터 고속 암호화</li>
        </ol>
        <li><b>무엇을 보장하나?</b></li>
          <ul>
            <li>기밀성, 무결성, 인증</li>
          </ul>
      </ul>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q4. IP 주소와 서브넷 마스크의 개념을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>IP 주소는 네트워크에서 각 장치를 식별하는 고유한 논리적 주소입니다. IPv4는 32비트로 구성되며 점으로 구분된 4개의 10진수로 표현합니다. 서브넷 마스크는 IP 주소에서 네트워크 부분과 호스트 부분을 구분하는 역할을 합니다. 예를 들어 192.168.1.10/24에서 /24는 앞의 24비트가 네트워크 주소임을 의미합니다. 서브네팅을 통해 큰 네트워크를 작은 단위로 나누어 관리할 수 있고, 브로드캐스트 도메인을 분리하여 네트워크 효율성을 높일 수 있습니다.</p>
      <hr>
      <h4>💡 서브네팅(subnetting)</h4>
      <p>하나의 IP 네트워크를 작은 네트워크(서브넷) 들로 나눠서 브로드캐스트 범위를 줄이고, 보안/관리/용량 계획을 쉽게 만드는 기술</p>
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
      <hr>
      <h4>💡 MAC 주소</h4>
      <p>네트워크 카드(NIC)에 붙은 하드웨어 고유 식별자(6바이트, 보통 AA:BB:CC:DD:EE:FF). 데이터 링크 계층(L2)에서 쓰인다.</p>
      <ul>
        <li><b>스위치가 MAC을 어떻게 쓰는가?</b></li>
        <ol>
          <li><b>학습(Learning):</b> 스위치는 들어온 프레임의 출발지 MAC과 포트를 테이블에 기록.</li>
          <li><b>전달(Forwarding):</b> 목적지 MAC이 테이블에 있으면 그 포트로만 전송.</li>
          <li><b>플러딩(Flooding):</b> 모르면 같은 VLAN 내 모든 포트로 뿌림(학습되기 전).<br> → 이렇게 해서 브로드캐스트 도메인 내에서 충돌 줄이고 효율적으로 전달!</li>
        </ol>
        <li><b>형식/종류</b></li>
        <ul>
          <li>앞 3바이트(OUI)는 제조사 식별, 뒤 3바이트는 장치 고유.</li>
          <li>유니캐스트(개별 NIC), 멀티캐스트, 브로드캐스트(FF:FF:FF:FF:FF:FF) 구분.</li>
        </ul>
      </ul>
      <h4>💡 유니캐스트 (Unicast)</h4>
      <p>한 송신자 → 한 수신자 (1:1 전송)</p>
      <ul>
        <li><b>예시:</b> 내 PC(192.168.1.10)가 서버(192.168.1.20)로 HTTP 요청 보냄</li>
        <li><b>주소:</b> 특정 IP 주소(L3)나 MAC 주소(L2)</li>
        <li><b>특징:</b> 가장 일반적이고 효율적. 필요한 대상에게만 보냄</li>
      </ul>
      <h4>💡 브로드캐스트 (Broadcast)</h4>
      <p>한 송신자 → 같은 네트워크(브로드캐스트 도메인)의 모든 호스트 (1:모두)</p>
      <ul>
        <li><b>예시:</b> ARP Request (목적 MAC: FF:FF:FF:FF:FF:FF, IPv4 한정)</li>
        <li><b>주소:</b> IPv4의 255.255.255.255(로컬), 서브넷 지향 브로드캐스트(예: 192.168.1.255)</li>
        <li><b>특징:</b> 라우터를 넘지 않음(도메인 한정). 트래픽이 커질 수 있어 과다 사용 지양</li>
        <li>※ IPv6에는 브로드캐스트가 없고 멀티캐스트로 대체</li>
      </ul>
      <h4>💡 애니캐스트 (Anycast)</h4>
      <p>한 송신자 → 여러 곳에 분산 배치된 동일 서비스 IP 중 가장 가까운(라우팅상 최단/최적) 한 곳으로 전달 (1:가까운 1)</p>
      <ul>
        <li><b>예시:</b> DNS 공개 리졸버(예: 1.1.1.1, 8.8.8.8). 전 세계 여러 데이터센터가 같은 IP를 광고하고, 라우팅이 가장 가까운 인스턴스로 보냄</li>
        <li><b>주소/작동:</b> 여러 서버가 동일 IP(prefix)를 BGP 등으로 광고 → 라우팅이 자동으로 근접 노드 선택</li>
        <li><b>특징:</b> 지연 감소, 가용성·부하분산 향상. 주로 L3(인터넷 라우팅)에서 사용</li>
      </ul>
      <h4>💡 멀티캐스트 (Multicast)</h4>
      <p>한 송신자(또는 여러 송신자)가 특정 그룹에 가입한 수신자들만 대상으로 데이터를 보내는 방식 (1:선택된 여러 명).<br>
      <b>장점:</b> 같은 데이터를 여러 대상에 보낼 때 대역폭 절약(한 번만 전송 → 네트워크가 필요한 지점에서 복제), 지연 균일.</p>
      <ul>
        <li><b>사용 예시:</b> 실시간 라이브 스트리밍/IPTV, 주식 시세 틱 데이터, 온라인 강의, 대규모 소프트웨어 배포, 게임 상태 동기화, 일부 WebRTC SFU 시나리오 등.</li>
      </ul>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q7. ARP(Address Resolution Protocol)의 동작 과정을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>ARP는 IP 주소를 MAC 주소로 변환하는 프로토콜입니다. 호스트가 같은 서브넷의 다른 호스트와 통신하려고 할 때, 목적지 IP 주소의 MAC 주소를 알아야 합니다. <br>먼저 ARP 캐시 테이블을 확인하고, 없으면 ARP Request를 브로드캐스트로 전송합니다. <br>해당 IP를 가진 호스트가 자신의 MAC 주소를 담은 ARP Reply를 유니캐스트로 응답합니다. <br>받은 정보를 ARP 캐시에 저장하여 일정 시간 동안 재사용합니다. <br>이를 통해 IP 패킷을 이더넷 프레임으로 캡슐화할 수 있습니다.</p>
      <hr>
      <h4>💡 호스트(Host)</h4>
      <p>호스트는 네트워크에 연결된 개별 기기를 말한다. PC, 노트북, 스마트폰, 서버, 프린터 등 IP·MAC 주소를 갖고 통신하는 주체면 전부 호스트이다.</p>
      <h4>서브넷(Subnet)</h4>
      <p>큰 네트워크를 작게 나눈 영역이다. 같은 서브넷에 있는 호스트끼리는 스위치만 거쳐 직접 통신하고(ARP 필요), 다른 서브넷과는 라우터를 통해 통신한다.</p>
      <ul>
        <li>192.168.1.0/24 라는 서브넷이면 IP가 192.168.1.0 ~ 192.168.1.255 범위(보통 호스트용은 .1~.254)가 같은 서브넷</li>
      </ul>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q8. DHCP의 동작 과정을 4단계로 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>DHCP는 네트워크 장치에 자동으로 IP 주소와 네트워크 설정을 할당하는 프로토콜입니다. <br>첫 번째 단계인 Discover에서 클라이언트가 DHCP 서버를 찾기 위해 브로드캐스트로 요청을 보냅니다. <br>두 번째 Offer 단계에서 DHCP 서버가 사용 가능한 IP 주소와 설정 정보를 제안합니다. <br>세 번째 Request 단계에서 클라이언트가 제안받은 설정을 사용하겠다고 요청합니다. <br>마지막 ACK 단계에서 서버가 확인 응답을 보내면 클라이언트는 해당 IP 주소와 설정을 사용하기 시작합니다.</p>
      <h4>💡 DHCP의 동작 과정</h4>
      <hr>
      <img
        src="https://github.com/user-attachments/assets/66ab308e-6e49-4fde-99de-e12d7d2fec15"
        alt="DHCP 동작 과정"
        width="1129" height="651" loading="lazy"
        style="max-width:100%; height:auto; display:inline-block;"
      />
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q9. NAT(Network Address Translation)의 종류와 동작 원리를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>NAT는 사설 IP 주소를 공인 IP 주소로 변환하는 기술입니다. <br>Static NAT는 사설 IP와 공인 IP를 1:1로 고정 매핑하고, Dynamic NAT는 사설 IP를 공인 IP 풀에서 동적으로 할당합니다. <br>PAT(Port Address Translation)는 포트 번호를 이용하여 하나의 공인 IP로 여러 사설 IP를 지원합니다. <br>내부에서 외부로 패킷이 나갈 때 소스 IP와 포트를 변환하고 NAT 테이블에 기록합니다. 외부에서 응답이 오면 NAT 테이블을 참조하여 원래 내부 IP와 포트로 변환하여 전달합니다.</p>
      <hr>
      <h4>💡 1:1 고정 매핑이란?</h4>
      <p>내부 사설 IP 하나가 항상 같은 공인 IP 하나와 짝지어 연결되는 것을 말한다.</p>
      <h4>💡 풀에서 동적으로 할당한다는 무슨 뜻인가?</h4>
      <p>NAT 장비가 미리 가진 공인 IP “묶음(풀)” 중에서 내부 호스트가 외부로 나갈 그때그때 빈 공인 IP를 하나 임시로 빌려주고 세션이 끝나거나 타임아웃 나면 반납해서 다시 다른 내부 호스트가 쓸 수 있게 하는 걸 말한다.</p>
      <h4>💡 내부와 외부</h4>
      <ul>
        <li><b>내부(inside):</b> NAT 장비(공유기/라우터) 안쪽 사설 네트워크를 말한다.</li>
        <ul>
          <li>192.168.1.0/24 라는 서브넷이면 IP가 192.168.1.0 ~ 192.168.1.255 범위(보통 호스트용은 .1~.254)가 같은 서브넷</li>
        </ul>예: 192.168.x.x, 10.x.x.x 같은 사설 IP를 쓰는 영역.
        <li><b>외부(outside):</b> NAT 장비 바깥쪽 네트워크이다. 보통 인터넷(공인 IP 영역)을 뜻하지만, 기업망에선 NAT 경계 밖의 다른 상위 네트워크를 의미할 수도 있다.</li>
      </ul>
      <p>즉, “내부에서 외부로”는 사설망 → (NAT 거쳐) → 공인망 방향을 말한다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q10. 로드 밸런싱의 종류와 알고리즘들을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>로드 밸런싱은 여러 서버에 트래픽을 분산하여 가용성과 성능을 향상시키는 기술입니다. L4 로드 밸런서는 IP와 포트 정보를 기반으로 분산하고, L7 로드 밸런서는 HTTP 헤더나 쿠키 같은 응용 계층 정보를 활용합니다. <br>주요 알고리즘으로는 Round Robin(순차 분배), Weighted Round Robin(가중치 기반 분배), Least Connections(최소 연결 수 기준), IP Hash(클라이언트 IP 해시 기반) 등이 있습니다. 헬스 체크 기능으로 장애 서버를 자동으로 제외하고, 세션 지속성을 통해 같은 클라이언트를 동일 서버로 연결할 수 있습니다.</p>
      <hr>
      <h4>💡 트래픽(traffic)</h4>
      <p>서버가 처리해야 하는 요청량과 데이터 흐름.</p>
      <ul>
        <li><b>측정:</b> RPS/QPS(초당 요청 수), 대역폭(Mbps/Gbps), 동시 연결 수 등.</li>
        <li><b>목표:</b> 트래픽이 몰려도 지연·오류 없이 처리하도록 여러 서버로 분산.</li>
      </ul>
      <h4>💡 분산 알고리즘</h4>
      <ul>
        <li><b>Round Robin (순차 분배)</b><br>서버 A→B→C→A… 차례대로 돌려가며 분배. 설정 간단, 균등 분배에 유리.</li>
        <li><b>Weighted Round Robin (가중치 분배)</b><br>서버 성능에 따라 비율을 둠. 예: A:2, B:1이면 A가 2번, B가 1번 비율로 받음.</li>
        <li><b>Least Connections (최소 연결 수)</b><br>현재 활성 연결이 가장 적은 서버로 보냄. 요청 처리 시간이 들쭉날쭉할 때 효율적.</li>
        <li><b>IP Hash (클라이언트 IP 해시)</b><br>클라이언트 IP를 해시해서 특정 서버에 일관되게 매핑. 세션 유지에 유리(쿠키 없이도).</li>
      </ul>
      <h4>💡 헬스 체크(Health Check)</h4>
      <p>고장 서버를 자동 배제/복귀시켜 가용성을 높이는 장치</p>
      <ul>
        <li><b>목적:</b> 문제 있는 서버를 자동으로 제외하고, 정상 복구되면 다시 포함.</li>
        <li><b>방법</b></li>
        <ul>
          <li><b>L4/TCP 체크:</b> 포트가 열려 있는지(3-way handshake 성공?)</li>
          <li><b>HTTP/HTTPS 체크:</b> 특정 경로(/health)로 상태 코드 200 등 확인</li>
          <li><b>애플리케이션 체크:</b> DB 연결, 의존 서비스 상태까지 내부 로직 검사</li>
          <li><b>수동/수동+수동:</b> 보통 액티브 체크(주기적 프로빙) + 패시브 체크(실패율 관찰) 병행</li>
        </ul>
        <li><b>파라미터 예:</b> 인터벌(주기), 타임아웃, 실패/성공 임계치(예: 3번 연속 실패 시 불건강).</li>
      </ul>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q11. VLAN의 개념과 장점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>VLAN(Virtual LAN)은 물리적으로 연결된 네트워크를 논리적으로 분할하는 기술입니다. 스위치 포트를 그룹화하여 각 그룹이 독립된 브로드캐스트 도메인을 형성합니다. Tag VLAN은 이더넷 헤더에 VLAN ID를 추가하여 여러 VLAN 트래픽을 하나의 링크로 전송할 수 있게 합니다. 주요 장점으로는 브로드캐스트 트래픽 감소, 보안 향상, 네트워크 관리 유연성 증가, 물리적 제약 없는 그룹 구성이 있습니다. 트렁크 포트를 통해 여러 VLAN 간 통신이 가능하며, 라우터나 L3 스위치로 VLAN 간 라우팅을 수행합니다.</p>
      <hr>
      <h4>💡 스위치 포트</h4>
      <p>스위치의 인터페이스(구멍/논리 포트)로, 여기에 PC·서버·다른 스위치를 연결한다.<br>포트는 보통 Access 포트(한 개 VLAN, 프레임은 태그 제거/미부착)와 Trunk 포트(여러 VLAN, 프레임에 802.1Q 태그 부착)로 동작 모드를 정한다.</p>
      <h4>💡 트렁크 포트 (Trunk)</h4>
      <p>여러 VLAN의 프레임을 한 링크로 운반하는 스위치 포트 모드.<br>프레임에 802.1Q 태그를 붙여 “이 프레임은 VLAN 10, 저건 VLAN 20”처럼 구분.<br>스위치 간 업링크, 방화벽/로드밸런서/하이퍼바이저와 연결할 때 자주 사용.</p>
      <h4>💡 Tag VLAN과의 관계</h4>
      <p>VLAN을 쓰면 스위치 안에서는 포트를 그룹으로 나눌 수 있다. 그런데 스위치↔스위치 또는 스위치↔가상화 호스트처럼 하나의 링크로 여러 VLAN 트래픽을 동시에 보내려면, 프레임에 VLAN ID를 표시해야 구분이 된다. 이때 사용하는 표준이 802.1Q 태깅(Tag VLAN)이다. (이더넷 헤더에 VLAN ID 추가)</p>
      <h4>💡 L3 스위치 (Multilayer Switch)</h4>
      <p>스위치(스위칭) + 라우터(라우팅) 기능을 함께 가진 장비.<br>VLAN마다 SVI(가상 인터페이스, 예: VLAN 10에 192.168.10.1) 를 만들어 VLAN 간 라우팅(Inter-VLAN Routing) 을 장비 내부에서 고속 처리한다.</p>
      <h4>💡 라우터와 라우팅</h4>
      <ul>
        <li><b>라우터:</b> 서로 다른 IP 네트워크(서브넷) 간에 패킷을 전달하는 장비.</li>
        <li><b>라우팅:</b> 목적지까지 가는 다음 홉을 라우팅 테이블/프로토콜(OSPF, BGP 등)로 결정해 포워딩하는 과정.</li>
        <li>포인트: VLAN은 2계층 분리, VLAN 간 통신은 3계층(라우터/L3 스위치)이 담당합니다.</li>
        <li>※ 트렁크 포트는 “여러 VLAN을 한 선으로 운반”하는 거고, “서로 통신”하게 만드는 건 라우팅</li>
      </ul>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q12. 방화벽의 종류와 동작 방식을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>방화벽은 네트워크 보안을 위해 트래픽을 제어하는 시스템입니다. <br>패킷 필터링 방화벽은 IP 헤더 정보(소스/목적지 IP, 포트)로 패킷을 차단하거나 허용합니다. <br>상태 추적 방화벽은 연결 상태를 기억하여 동적으로 규칙을 적용하고, 이를 보완해 응용 계층 게이트웨이는 특정 프로토콜의 내용까지 분석합니다. <br>차세대 방화벽은 DPI(Deep Packet Inspection), IPS 기능, 사용자 인증 등을 통합 제공합니다. 방화벽 정책은 기본적으로 deny-all 원칙을 따르고, 필요한 트래픽만 명시적으로 허용하는 화이트리스트 방식을 사용합니다.</p>
      <hr>
      <h4>💡 상태 추적 방화벽 ↔ 응용 계층 게이트웨이(ALG)의 관계</h4>
      <ul>
        <li><b>상태 추적 방화벽(Stateful):</b> L3/L4(IP/포트, TCP 상태) 중심으로 연결 상태(예: SYN→ESTABLISHED) 를 기억해 동적으로 허용/차단.</li>
        <li><b>응용 계층 게이트웨이(ALG / Application Proxy):</b> L7(프로토콜 내용)까지 이해하고, FTP/SIP 같은 복잡한 프로토콜의 제어 채널을 파싱·필요 시 재작성(예: 포트 넘버 열기) 해줌.</li>
      </ul>
      <p>서로 대체가 아니라 보완적. 실제 제품에선 상태 추적 엔진 + ALG 모듈이 함께 동작해, 연결의 “상태”도 보고 “내용”도 이해하여 더 정확히 제어합니다. (차세대 방화벽은 이 L7 기능을 더 폭넓게 통합)</p>
      <h4>💡 DPI와 IPS</h4>
      <ul>
        <li><b>DPI (Deep Packet Inspection):</b> 패킷의 페이로드(내용) 를 분석해 애플리케이션 식별, 서명 기반 악성 트래픽 탐지, 정책 적용(예: 특정 앱 차단).</li>
        <li><b>IPS (Intrusion Prevention System):</b> 탐지에 그치지 않고 실시간 차단까지 수행하는 보안 장비/기능.</li>
        <ul>
          <li><b>IDS vs IPS:</b> IDS는 탐지/알림, IPS는 탐지 + 즉시 차단(인라인).</li>
          <li><b>방법:</b> 서명(Signature), 이상행위(Anomaly), 평판(Reputation), 취약점 가상패치 등.</li>
        </ul>
      </ul>
      <h4>💡 deny-all 원칙</h4>
      <p>기본 정책을 모두 차단(default deny) 으로 두고, 필요한 것만 명시적으로 허용(화이트리스트) 하는 설계.</p>
      <ul>
        <li><b>이점:</b> 최소 권한(Least Privilege) 보장, 설정 누락/오류로 인한 무의도한 개방 차단, 감사·관리 용이.</li>
        <li><b>실무 팁</b> </li>
        <ul>
          <li>인바운드/아웃바운드 각각 기본 차단 + 명시 허용 규칙 순서 적용</li>
          <li>허용 규칙은 최소 범위(소스/목적지 IP·포트·프로토콜) 로 구체화</li>
          <li>로그/모니터링 켜서 누락 트래픽 확인 후 필요한 것만 추가 허용</li>
        </ul>
      </ul>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q13. VPN의 종류와 터널링 기술을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>VPN은 공중망을 통해 안전한 사설망 연결을 제공하는 기술입니다. Site-to-Site VPN은 지사 간 연결에 사용하고, Remote Access VPN은 개별 사용자의 원격 접속에 활용합니다. 터널링 프로토콜로는 PPTP(간단하지만 보안 취약), L2TP/IPSec(강력한 보안), SSL VPN(웹 브라우저 기반 접근), OpenVPN(오픈소스 솔루션) 등이 있습니다. 터널링은 원본 패킷을 암호화하고 새로운 IP 헤더로 감싸서 전송하며, 목적지에서 복호화하여 원본 패킷을 복원합니다. 인증, 암호화, 무결성 검증을 통해 보안을 보장합니다.</p>
      <hr>
      <h4>💡 공중망(公共網, Public Network)</h4>
      <p>누구나 이용하는 공용 네트워크를 말한다. 대표적으로 인터넷이 공중망이다. (통신사 백본, ISP 구간 포함)</p>
      <h4>💡 VPN과 터널링의 관계</h4>
      <ul>
        <li><b>VPN:</b> 공중망(인터넷) 위에서 사설망처럼 안전하게 통신하도록 해주는 전체 솔루션/개념. (인증·암호화·무결성 포함)</li>
        <li><b>터널링:</b> 그 VPN을 구현하는 핵심 기술 방식. 원본 패킷을 암호화하고 새 IP 헤더로 감싸(캡슐화) 공중망을 지나가게 함.</li>
      </ul>
      <p>👉 요약: VPN(서비스)를 만들기 위해 터널링(기술)을 사용한다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q14. QoS(Quality of Service)의 개념과 구현 방법을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>QoS는 네트워크에서 특정 트래픽에 우선순위를 부여하여 서비스 품질을 보장하는 기술입니다. 대역폭, 지연시간, 지터, 패킷 손실률 등의 네트워크 성능 지표를 관리합니다. 구현 방법으로는 트래픽 분류(Classification), 마킹(Marking), 큐잉(Queuing), 셰이핑(Shaping), 폴리싱(Policing)이 있습니다. IntServ는 경로상의 모든 라우터에서 자원을 예약하는 방식이고, DiffServ는 패킷에 DSCP 값을 설정하여 홉별로 차등 서비스를 제공합니다. 음성, 영상 같은 실시간 트래픽은 높은 우선순위를, 파일 전송 같은 트래픽은 낮은 우선순위를 부여합니다.</p>
      <hr>
      <h4>💡 지터 (Jitter)</h4>
      <p>패킷이 도착하는 간격의 흔들림(시간 변동). 음성/영상은 일정 간격으로 도착해야 부드러운데, 지터가 크면 끊김·왜곡 발생.</p>
      <h4>💡 QoS 구성 요소</h4>
      <ul>
        <li><b>트래픽 분류 (Classification):</b> 패킷을 누구 것/무슨 앱인지 구분 (IP/포트/프로토콜/DSCP/ACL 등).</li>
        <li><b>마킹 (Marking):</b> 분류 결과를 헤더에 표시(예: DSCP 값 설정)해 이후 장비들도 우선순위를 인지.</li>
        <li><b>큐잉 (Queuing):</b> 우선순위별 대기열에 넣어 스케줄링 (예: Priority/Weighted Fair Queuing).</li>
        <li><b>셰이핑 (Shaping):</b> 버스트를 완화해 정해진 속도로 부드럽게 내보냄(버퍼 사용, 지연 증가 가능).</li>
        <li><b>폴리싱 (Policing):</b> 정해진 속도 초과 트래픽은 즉시 드롭/리마크(버퍼 X, 지연 증가 없음).</li>
      </ul>
      <h4>💡 QoS와 IntServ / DiffServ 관계</h4>
      <ul>
        <li><b>QoS:</b> “품질을 보장하려는 전체 개념/메커니즘”의 총칭.</li>
        <li><b>IntServ (Integrated Services):</b> 흐름 단위로 자원 예약(RSVP). 경로의 모든 라우터가 대역폭/큐를 예약 → 정확하지만 확장성 낮음.</li>
        <li><b>DiffServ (Differentiated Services):</b> 패킷에 DSCP로 클래스(우선순위) 표시 → 각 홉에서 클래스별 차등 처리 → 확장성 높음, 코어는 단순 처리.</li>
      </ul>
      <h4>💡 DSCP</h4>
      <p>우선순위 표식, 홉은 라우터 하나 지나갈 때마다의 단계.</p>
       <ul>
        <li><b>DSCP 값:</b> IPv4/IPv6 헤더의 6비트 필드(TOS/Traffic Class 일부).</li>
        <li><b>역할:</b> 패킷의 서비스 클래스/우선순위를 표시(예: EF=실시간 음성, AFxx=보장형, BE=일반).</li>
        <li><b>효과:</b> 네트워크 장비가 DSCP를 읽고 큐잉/스케줄링/드롭 정책을 차등 적용.</li>
      </ul>
      <h4>💡 홉 (Hop)</h4>
      <p>패킷이 라우터(또는 L3 장비) 를 한 번 지날 때마다 1홉.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q15. CDN(Content Delivery Network)의 동작 원리와 장점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>CDN은 전 세계에 분산된 캐시 서버를 통해 콘텐츠를 사용자와 가까운 위치에서 제공하는 서비스입니다. 사용자가 웹사이트에 접속하면 DNS를 통해 가장 가까운 엣지 서버로 리다이렉트됩니다. 캐시에 콘텐츠가 있으면 즉시 응답하고, 없으면 원본 서버에서 가져와 캐시한 후 응답합니다. 주요 장점으로는 응답 시간 단축, 원본 서버 부하 감소, 대역폭 비용 절감, 가용성 향상이 있습니다. 정적 콘텐츠(이미지, CSS, JS)는 물론 동적 콘텐츠나 스트리밍 서비스도 지원하며, DDoS 공격 완화 효과도 제공합니다.</p>
      <hr>
      <h4>💡 엣지 서버(Edge Server)</h4>
      <p>사용자에게 지리적으로 가까운 CDN 캐시 서버이다. 이미지·CSS·JS 같은 콘텐츠를 미리/요청 시 캐시에 저장해, 짧은 지연 시간으로 빠르게 보내준다. (CDN의 PoP(Point of Presence) 안에 위치)</p>
      <h4>💡 리다이렉트 의미(DNS 기준)</h4>
      <p>여기서 “리다이렉트”는 HTTP 3xx 이동이 아니라, DNS가 가장 가까운 엣지 서버의 IP를 응답하는 걸 말한다. 즉, 브라우저가 도메인을 조회하면 DNS가 근접 PoP의 IP를 돌려주고, 브라우저는 그 IP(엣지 서버)에 곧바로 접속한다.</p>
      <h4>💡 DDoS 공격(Distributed Denial of Service)</h4>
      <p>다수의 좀비/봇 기기로부터 트래픽을 한꺼번에 퍼부어 서비스를 마비시키는 공격. CDN은 전 세계 분산 인프라로 트래픽을 분산·흡수하고, 애니캐스트 라우팅, 레이트 리밋, WAF/봇 차단, 캐시 히트 등으로 영향 범위를 줄이며 가용성을 높인다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q16. SSL/TLS 핸드셰이크 과정을 단계별로 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>SSL/TLS 핸드셰이크는 클라이언트와 서버가 안전한 통신을 위해 암호화 파라미터를 협상하는 과정입니다. 클라이언트가 Client Hello 메시지로 지원하는 암호화 방식을 서버에 알립니다. 서버는 Server Hello로 선택한 암호화 방식과 인증서를 전송합니다. 클라이언트는 인증서를 검증하고 Pre-Master Secret을 서버의 공개키로 암호화하여 전송합니다. 양측이 Pre-Master Secret으로부터 대칭키를 생성하고, Finished 메시지를 교환하여 핸드셰이크를 완료합니다. 이후 모든 애플리케이션 데이터는 협상된 대칭키로 암호화됩니다.</p>
      <h4>💡 SSL/TLS 핸드셰이크 과정</h4>
      <hr>
      <img
        src="https://github.com/user-attachments/assets/438c38a1-2620-42b1-99dd-4022f882d526"
        alt="SSL/TLS 핸드셰이크 과정"
        width="214" height="235" loading="lazy"
        style="max-width:100%; height:auto; display:inline-block;"
      />
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q17. HTTP/2와 HTTP/1.1의 차이점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>HTTP/2는 HTTP/1.1의 성능 문제를 해결하기 위해 개발된 프로토콜입니다. 가장 큰 차이점은 멀티플렉싱으로, 하나의 TCP 연결에서 여러 요청을 동시에 처리할 수 있어 Head-of-Line Blocking 문제를 해결합니다. 헤더 압축을 통해 중복되는 헤더 정보를 압축하여 대역폭을 절약하고, 서버 푸시 기능으로 클라이언트 요청 전에 미리 리소스를 전송할 수 있습니다. 바이너리 프레이밍을 사용하여 파싱 효율성을 높이고, 스트림 우선순위를 통해 중요한 리소스를 먼저 전송할 수 있습니다.</p>
      <hr>
      <h4>💡 멀티플렉싱 (Multiplexing)</h4>
      <p>하나의 TCP 연결 위에서 여러 요청/응답 스트림을 동시에 섞어서 보낸다. 탭 여러 개 열어도 연결 1개로 병렬 처리 가능.</p>
      <h4>💡 Head-of-Line Blocking(HoLB) 문제</h4>
      <p>HTTP/1.1의 파이프라이닝/직렬 처리에서는 앞선 응답이 지연되면 뒤 요청들도 줄줄이 대기해야 했다. HTTP/2 멀티플렉싱은 서로 다른 스트림이 독립적이라 앞 요청이 막혀도 뒤 요청이 먼저 도착할 수 있어 이 문제를 크게 줄인다.</p>
      <h4>💡 서버 푸시 (Server Push)</h4>
      <p>클라이언트가 HTML을 요청하면, 서버가 CSS/JS 같은 리소스를 요청 전에 먼저 밀어준다. 초기 로딩을 빠르게 하려는 기능. 요즘은 과푸시/캐시 충돌 이슈로 신중히 쓰이거나 대체 전략(Preload/HTTP/3 등)을 선호하기도 한다.</p>
      <h4>💡 바이너리 프레이밍 (Binary Framing)</h4>
      <p>HTTP/2는 텍스트 대신 이진 프레임 단위로 메시지를 쪼개 전송합니다(HEADERS, DATA 등).</p>
      <ul>
        <li><b>장점:</b> 파싱 효율↑, 오버헤드↓, 스트림 식별/우선순위 같은 기능을 프로토콜 레벨에서 정확하게 처리.</li>
      </ul>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q18. 웹소켓(WebSocket)의 특징과 HTTP와의 차이점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>웹소켓은 클라이언트와 서버 간 양방향 실시간 통신을 제공하는 프로토콜입니다. HTTP와 달리 연결이 한 번 수립되면 지속적으로 유지되며, 양쪽에서 언제든 데이터를 전송할 수 있습니다. HTTP는 요청-응답 방식의 반이중 통신이지만, 웹소켓은 전이중 통신이 가능합니다. 초기 연결은 HTTP 업그레이드를 통해 이루어지고, 이후에는 웹소켓 프로토콜로 통신합니다. 채팅, 게임, 주식 시세, 협업 도구 등 실시간 상호작용이 필요한 애플리케이션에 적합하며, 폴링 방식보다 효율적입니다.</p>
      <hr>
      <h4>💡 반이중 통신(Half-duplex) vs 전이중 통신(Full-duplex)</h4>
      <ul>
        <li><b>반이중:</b> 한 순간엔 한쪽만 전송 가능. 보내거나 받거나 번갈아 함.</li>
        <ul>
          <li>예: 무전기(“오버!” 하고 교대), HTTP 요청-응답(클라이언트가 보내면 서버가 답).</li>
        </ul>
        <li><b>전이중:</b> 동시에 양방향 전송 가능. 보내면서 동시에 받을 수 있음.</li>
        <ul>
          <li>예: 전화 통화, 웹소켓 데이터 송수신.</li>
        </ul>
      </ul>
      <p>=> 웹소켓은 전이중이라 채팅 입력과 수신 메시지가 동시에 흐를 수 있다.</p>
      <h4>💡 폴링 방식(Polling)</h4>
      <p>클라이언트가 “새 거 있어?” 하고 주기적으로 요청을 보내 서버 업데이트를 확인하는 방식.</p>
      <ul>
        <li><b>종류</b></li>
        <ul>
          <li><b>짧은 폴링(Short polling):</b> 정해진 간격(예: 1초, 5초)으로 반복 요청. 구현 쉬우나 요청 낭비/지연 발생.</li>
          <li><b>롱 폴링(Long polling):</b> 요청을 보내면 서버가 새 이벤트가 생길 때까지 응답을 지연했다가 보내줌. 지연은 줄지만 연결/리소스 비용이 큼.</li>
        </ul>
        <li><b>비교:</b> 폴링은 HTTP 요청을 반복해서 오버헤드가 크고, 실시간성/효율이 아쉬움. 웹소켓은 연결을 한 번 업그레이드 후 유지하며 전이중으로 푸시 가능해 지연↓, 오버헤드↓.</li>
      </ul>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q19. 쿠키(Cookie)와 세션(Session)의 차이점과 보안 고려사항을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>쿠키는 클라이언트 브라우저에 저장되는 작은 데이터 조각으로, 서버가 클라이언트의 상태를 유지하기 위해 사용합니다. 세션은 서버에 저장되는 사용자 정보로, 보통 세션 ID만 쿠키에 저장합니다. 쿠키는 클라이언트에서 조작 가능하여 보안에 취약하고, 세션은 서버에 저장되어 더 안전하지만 서버 메모리를 사용합니다. 보안 고려사항으로는 HttpOnly 플래그로 XSS 공격 방지, Secure 플래그로 HTTPS에서만 전송, SameSite 속성으로 CSRF 공격 방지, 적절한 만료시간 설정 등이 있습니다.</p>
      <hr>
      <h4>💡 HttpOnly</h4>
      <p>브라우저의 JS에서 쿠키 접근 금지(document.cookie 불가).</p>
      <ul>
        <li><b>효과:</b> XSS가 발생해도 쿠키 탈취(세션 하이재킹) 위험 감소.</li>
        <li><b>한계:</b> XSS 자체를 막는 건 아님(렌더링·DOM 조작은 여전히 가능).</li>
      </ul>
      <h4>💡 Secure</h4>
      <p>HTTPS에서만 쿠키 전송. 평문 HTTP 전송 차단 → 도청 방지.</p>
      <ul>
        <li><b>실무:</b> SameSite=None을 쓰면 Secure 필수(현대 브라우저 정책).</li>
      </ul>
      <h4>💡 SameSite (CSRF 완화)</h4>
      <p>서드파티 컨텍스트에서 자동 전송을 제한해 CSRF를 완화.</p>
      <ul>
        <li><b>모드</b> </li>
        <ul>
          <li><b>Lax(기본):</b> 대부분의 서드파티 요청엔 미전송, 단 GET 네비게이션 등 일부는 전송.</li>
          <li><b>Strict:</b> 타 사이트에서 오는 모든 요청에 미전송(보안 높음, UX 제약 큼).</li>
          <li><b>None:</b> 항상 전송, 단 Secure와 함께만 사용 가능(크로스 도메인 필요 시).</li>
        </ul>
        <li><b>주의:</b> CSRF 토큰 등 추가 대책과 함께 쓰는 게 안전.</li>
      </ul>
      <h4>💡 만료 시간(수명) 설정</h4>
      <ul>
        <li>Expires(절대시각) 또는 Max-Age(초 단위, 상대시간)로 쿠키 수명을 지정.</li>
        <li>민감 쿠키(세션 ID 등)는 짧게 설정하고, 미사용 시 서버 세션도 만료.</li>
        <li>“세션 쿠키”(만료 미지정)는 브라우저 종료 시 삭제(브라우저 정책 영향 가능).</li>
      </ul>
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
