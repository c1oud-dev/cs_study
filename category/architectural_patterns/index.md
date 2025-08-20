---
layout: default
title: "Architectural Patterns"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>Architectural Patterns</h2>
  <p>아키텍처 패턴(Architectural Pattern)은 특정한 맥락(context)에서 소프트웨어 아키텍처에서 자주 발생하는 문제에 대한 일반적이고 재사용 가능한 해결책이다. 아키텍처 패턴은 컴퓨터 하드웨어 성능 제한, 높은 가용성, 비즈니스 리스크 최소화 등과 같은 소프트웨어 공학의 다양한 문제들을 다룬다.</p>
  <p><strong>정리: 아키텍처 패턴은 소프트웨어 아키텍처 문제를 해결하기 위한 재사용 가능한 설계 틀이다.</strong></p>
</section>

<!-- 설명 -->
<details open>
<summary><span class="accordion-title">Monolithic Apps(모놀리식 애플리케이션)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>Monolithic Application은 <b>하나의 응집된 단일 단위</b>로 설계되며, 사용자 인터페이스, 비즈니스 로직, 데이터 액세스 같은 모든 컴포넌트가 긴밀하게 통합되어 하나의 서비스로 실행된다.</p>
  <p>이러한 아키텍처는 전체 애플리케이션이 함께 관리되고 배포되기 때문에 <b>개발과 배포가 단순</b>해진다. 그러나 애플리케이션이 커질수록 <b>확장성, 유지보수성, 민첩성</b> 측면에서 문제가 발생할 수 있다. 애플리케이션의 한 부분을 변경하려면 전체 시스템을 다시 배포해야 하고, 확장을 위해서는 개별 컴포넌트만 확장하는 것이 아니라 전체 애플리케이션을 복제해야 할 수도 있다.</p>
  <p>따라서 모놀리식 아키텍처는 <b>작은 규모의 애플리케이션</b>이나 <b>복잡성이 낮은 프로젝트</b>에는 적합할 수 있지만, 많은 조직들이 확장 단계에서 이러한 한계를 극복하기 위해 <b>마이크로서비스나 모듈형 아키텍처</b>로 전환한다.</p>
  <p><strong>정리: 모놀리식 아키텍처는 단일 서비스로 단순하지만, 확장성과 유연성이 떨어진다.</strong></p>
  <!-- 가로선 추가 -->
  <hr>
  <ul>
    <li><strong>비즈니스 로직:</strong> 애플리케이션에서 핵심 규칙과 처리 절차를 담는 부분으로, 입력 데이터를 기반으로 원하는 결과를 만들어내는 실제 업무 규칙을 구현한다.</li>
    <li><strong>마이크로서비스 아키텍처:</strong> 애플리케이션을 작은 독립 서비스 단위로 나누어 각각 독립적으로 개발, 배포, 확장할 수 있는 아키텍처. 서비스 간은 주로 API를 통해 통신한다.</li>
    <li><strong>모듈형 아키텍처:</strong> 애플리케이션을 기능별 모듈로 나누어 개발하는 방식으로, 모듈은 서로 독립적이면서도 전체 시스템과 유기적으로 동작한다. 마이크로서비스보다 결합도가 높지만 모놀리식보다는 유연하다.</li>
  </ul>

</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title">Microservices(마이크로서비스)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>Microservices는 애플리케이션을 <b>느슨하게 결합된 독립적으로 배포 가능한 서비스들의 집합</b>으로 구성하는 아키텍처 스타일이다. 각 마이크로서비스는 특정한 비즈니스 기능에 집중하며, 일반적으로 HTTP나 메시징 큐 같은 경량 프로토콜을 통해 다른 서비스와 통신한다.</p>
  <p>이 방식은 서비스들이 독립적으로 개발, 배포, 확장될 수 있기 때문에 <b>확장성, 유연성, 탄력성</b>을 높여준다. 또한 컴포넌트별로 다양한 기술과 언어를 사용할 수 있으며, 지속적 전달(Continuous Delivery)과 배포를 지원한다. 그러나 마이크로서비스를 관리할 때는 서비스 간 통신, 데이터 일관성, 배포 오케스트레이션 같은 <b>복잡성</b>이 따른다.</p>
  <p><strong>정리: 마이크로서비스는 독립 서비스들의 집합으로 확장성과 유연성은 높지만, 관리 복잡성이 크다.</strong></p>
  <!-- 가로선 추가 -->
  <hr>
  <ul>
    <li><strong>메시징 큐(Messaging Queue):</strong> 애플리케이션 컴포넌트 간에 메시지를 비동기적으로 전달하는 시스템으로, 생산자(Producer)가 보낸 메시지를 큐에 저장하고 소비자(Consumer)가 이를 꺼내 처리한다.</li>
      <ul><li>예: RabbitMQ, Kafka</li></ul>
    <li><strong>경량 프로토콜(Lightweight Protocol):</strong> 데이터 교환 시 불필요한 오버헤드를 최소화한 단순하고 효율적인 통신 규약.</li>
      <ul><li>예: HTTP/REST, gRPC</li></ul>
    <li><strong>지속적 전달(Continuous Delivery, CD):</strong> 애플리케이션을 언제든 안정적으로 배포할 수 있도록 자동화된 테스트와 빌드를 거쳐 릴리스 후보를 지속적으로 제공하는 소프트웨어 개발 방식.</li>
    <li><strong>배포 오케스트레이션(Deployment Orchestration):</strong> 여러 서비스나 컨테이너를 자동으로 배포·관리·스케일링하는 프로세스로, 의존성과 순서를 고려해 전체 시스템을 조율한다.</li>
      <ul><li>예: Kubernetes</li></ul>
  </ul>

</div>
</details>


<!-- 설명 -->
<details>
<summary><span class="accordion-title">SOA(Service-Oriented Architecture, 서비스 지향 아키텍처) </span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>서비스 지향 아키텍처는 소프트웨어 컴포넌트(서비스라 불림)를 <b>재사용 가능하고 느슨하게 결합되며 네트워크를 통해 상호작용</b>하도록 설계하는 아키텍처 패턴이다. 각 서비스는 특정 비즈니스 기능을 수행하는 <b>자급자족형 단위(self-contained unit)</b>이며, HTTP와 XML 같은 표준화된 프로토콜과 데이터 포맷을 통해 다른 서비스와 통신한다.</p>
  <p>SOA는 서비스가 독립적으로 개발, 배포, 유지될 수 있게 하여 조직이 <b>확장 가능하고, 유연하며, 상호운용성 있는 시스템</b>을 구축하도록 돕는다. 이 접근법은 모듈화, 이질적인 시스템 간의 손쉬운 통합, 변화하는 비즈니스 요구에 대한 민첩성을 촉진한다.</p>
  <p><strong>정리: SOA는 표준 프로토콜을 통해 느슨하게 결합된 재사용 가능한 서비스들의 아키텍처다.</strong></p>
  <!-- 가로선 추가 -->
  <hr>
  <ul>
    <li><strong>자급자족형 단위(Self-contained unit):</strong> 외부에 크게 의존하지 않고, 자체적으로 실행·관리 가능한 독립적인 컴포넌트를 의미한다. 예를 들어, 하나의 서비스가 자신의 데이터 저장, 로직, 인터페이스를 모두 갖추고 있어서 단독으로 동작할 수 있는 형태.</li>
    <li><strong>데이터 포맷(Data format):</strong> 데이터를 저장하거나 교환하기 위해 구조화한 표현 방식이다. 시스템 간 통신에서 공통 규칙을 정해주며, 대표적으로 JSON, XML, CSV 같은 형식이 있다.</li>
  </ul>

</div>
</details>


<!-- 설명 -->
<details>
<summary><span class="accordion-title">Serverless(서버리스) </span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>서버리스 컴퓨팅(Serverless Computing)은 개발자가 서버 인프라를 관리하지 않고 애플리케이션을 구축하고 실행할 수 있는 <b>클라우드 컴퓨팅 모델</b>이다. 이 모델에서 서버 관리, 확장, 유지보수 작업은 클라우드 제공자가 담당한다.</p>
  <p>개발자는 코드를 <b>함수(Function)</b> 형태로 배포하며, 이는 이벤트나 트리거에 반응해 실행된다. 또한 예약된 용량이 아니라 <b>실제 사용량</b>에 따라 비용이 청구된다. 이 접근 방식은 인프라 관리 문제를 추상화하여 개발을 단순화하고, 자동 확장을 가능하게 하며, 운영 부담을 줄여준다.</p>
  <p>대표적인 서버리스 플랫폼으로는 <b>AWS Lambda, Google Cloud Functions, Azure Functions</b> 등이 있으며, 이벤트 기반 애플리케이션과 마이크로서비스를 폭넓게 지원한다.</p>
  <p><strong>정리: 서버리스는 서버 관리 없이 함수 단위 코드만 실행하는 클라우드 모델이다.</strong></p>
  <!-- 가로선 추가 -->
  <hr>
  <ul>
    <li><strong>서버 인프라(Server Infrastructure):</strong> 애플리케이션이 실행되기 위해 필요한 하드웨어와 소프트웨어 자원(서버, 네트워크, 스토리지, 운영체제 등)을 통합한 기반 환경.</li>
    <li><strong>클라우드 컴퓨팅(Cloud Computing):</strong> 인터넷을 통해 서버, 스토리지, 데이터베이스, 네트워크, 소프트웨어 같은 IT 자원을 필요할 때 바로 제공받아 사용하는 방식. 사용자는 자원을 소유하지 않고 임대해 쓰는 개념.</li>
    <li><strong>함수(Function):</strong> 서버리스 컴퓨팅에서 실행 단위로 사용되는 작은 코드 블록으로, 특정 입력을 받아 한 가지 작업을 수행하고 결과를 반환한다.</li>
    <li><strong>트리거(Trigger):</strong> 함수를 실행시키는 이벤트나 조건으로, 예를 들어 HTTP 요청, 파일 업로드, DB 변경 같은 상황이 트리거가 될 수 있다.</li>
  </ul>

</div>
</details>


<!-- 설명 -->
<details>
<summary><span class="accordion-title">Service Mesh(서비스 메시) </span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>Service Mesh는 분산 네트워크에서 마이크로서비스 간의 <b>통신, 보안, 관리 기능을 향상</b>시키기 위한 아키텍처 패턴이다. 서비스 메시에서는 지능형 프록시 집합을 사용해 서비스 간 통신을 관리하며, 이를 통해 높은 가용성, 효율적인 로드 밸런싱, 강력한 서비스 디스커버리를 보장한다.</p>
  <p>또한 서비스 메시에는 네트워크 동작을 모니터링하는 <b>가시성(Observability)</b>, 다양한 트래픽 관리 기능 같은 고급 기능도 제공된다. 일반적인 서비스 메시 구조에서는 각 마이크로서비스에 하나의 프록시가 쌍을 이루어 배치된다. 이 프록시는 주로 <b>사이드카 패턴(Sidecar Pattern)</b>을 사용해 배포되며, 해당 마이크로서비스의 통신을 처리할 뿐 아니라 로드 밸런싱, 지능형 라우팅, 안전한 데이터 전송 등 다양한 네트워크 기능도 구현한다.</p>
  <p>사이드카 패턴은 특히 쿠버네티스 환경에서 <b>메인 마이크로서비스 컨테이너 옆에 프록시 컨테이너를 함께 배치</b>하는 방식으로 활용된다. 이러한 설계 덕분에 서비스 메시는 마이크로서비스 자체와 독립적으로 동작할 수 있어 관리와 업데이트를 단순화한다.</p>
  <p><strong>정리: 서비스 메시는 사이드카 프록시로 마이크로서비스 간 통신·보안을 관리하는 아키텍처다.</strong></p>
  <!-- 가로선 추가 -->
  <hr>
  <ul>
    <li><strong>지능형 프록시(Intelligent Proxy):</strong> 서비스 간 트래픽을 중계하면서 <b>보안, 로깅, 라우팅, 모니터링</b> 같은 추가 기능을 제공하는 고급 프록시.</li>
    <li><strong>로드 밸런싱(Load Balancing):</strong> 다수의 서버나 서비스 인스턴스로 들어오는 요청을 <b>균등하게 분산</b>시켜 성능과 가용성을 높이는 기술.</li>
    <li><strong>서비스 디스커버리(Service Discovery):</strong> 분산 환경에서 동적으로 생성되는 서비스들의 <b>위치(IP, 포트 등)를 자동으로 탐색</b>하고 연결하는 메커니즘.</li>
    <li><strong>사이드카 패턴(Sidecar Pattern):</strong> 애플리케이션(주 서비스)과 함께 <b>보조 기능을 담당하는 별도 컨테이너(사이드카)</b>를 배치하는 설계 패턴.</li>
    <li><strong>지능형 라우팅(Intelligent Routing):</strong> 단순히 목적지로 보내는 것이 아니라, <b>상황(트래픽 상태, 정책, 버전 등)에 맞춰 최적 경로를 선택</b>해 요청을 전달하는 기술.</li>
    <li><strong>쿠버네티스 환경(Kubernetes Environment):</strong> 컨테이너화된 애플리케이션을 <b>자동 배포, 확장, 관리</b>할 수 있는 오케스트레이션 플랫폼 환경.</li>
    <li><strong>마이크로서비스 컨테이너(Microservice Container):</strong> 특정 비즈니스 기능을 수행하는 마이크로서비스를 실행하는 <b>독립적인 컨테이너.</b></li>
    <li><strong>프록시 컨테이너(Proxy Container):</strong> 마이크로서비스 컨테이너 옆에서 배치되어 <b>트래픽 관리, 보안, 통신 기능</b>을 담당하는 보조 컨테이너.</li>
  </ul>

</div>
</details>


<!-- 설명 -->
<details>
<summary><span class="accordion-title">Twelve-Factor Apps </span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>설명</p>
  <p><strong>정리:</strong></p>
  <!-- 가로선 추가 -->
  <hr>
  <ul>
    <li><strong>:</strong> </li>
  </ul>

</div>
</details>
