---
layout: default
title: "Architectural Patterns"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>Architectural Patterns</h2>
  <p>소프트웨어 시스템의 <b>전체 구조와 상호작용 방식</b>을 정의하는 반복 가능한 설계 방법으로 애플리케이션을 어떤 방식으로 <b>구성하고, 계층화하며, 확장/변경할지</b>에 대한 청사진을 제공한다.</p>
  <ul>
    <li><strong>Layered Pattern (계층형 아키텍처)</strong></li>
    <ul>
      <li>시스템을 <b>프레젠테이션, 비즈니스 로직, 데이터 접근</b> 등 여러 계층으로 나눔.</li>
      <li>각 계층은 바로 아래 계층에만 의존.</li>
      <li>예: Spring MVC (Controller → Service → Repository)</li>
    </ul>
    <li><strong>Client-Server Pattern</strong></li>
    <ul>
      <li>클라이언트는 서비스를 요청하고, 서버는 응답을 제공.</li>
      <li>예: 웹 브라우저(클라이언트) ↔ 웹 서버</li>
    </ul>
    <li><strong>Master-Slave Pattern</strong></li>
    <ul>
      <li>Master가 작업을 분배하고, Slave들이 처리 후 결과를 다시 Master에 전달.</li>
      <li>예: DB 복제(Master DB - Slave DB), 병렬 연산</li>
    </ul>
    <li><strong>Pipe-Filter Pattern</strong></li>
    <ul>
      <li>데이터를 **일련의 처리 단계(Filter)**를 거치며 흐르게(Pipe) 구성.</li>
      <li>각 Filter는 독립적인 처리 단위.</li>
      <li>예: Unix 파이프(cat file | grep "error" | sort), 데이터 스트리밍 처리</li>
    </ul>
    <li><strong>Broker Pattern</strong></li>
    <ul>
      <li>중재자(Broker)가 클라이언트와 서버 간의 통신을 관리.</li>
      <li>예: 메시지 큐(MQ), RPC(Remote Procedure Call)</li>
    </ul>
    <li><strong>Event-Driven Pattern</strong></li>
    <ul>
      <li>이벤트 발생 → 이벤트 핸들러가 반응.</li>
      <li>느슨한 결합, 비동기적.</li>
      <li>예: GUI 이벤트 처리, Kafka 같은 이벤트 스트리밍</li>
    </ul>
    <li><strong>Microkernel (Plug-in) Pattern</strong></li>
    <ul>
      <li>최소한의 코어 시스템 + 확장 모듈(Plug-in) 구조.</li>
      <li>예: IDE(Eclipse, IntelliJ) + 플러그인</li>
    </ul>
    <li><strong>Microservices Pattern</strong></li>
    <ul>
      <li>시스템을 작은 독립적 서비스들로 나누고, API를 통해 통신.</li>
      <li>예: Netflix, Amazon 아키텍처</li>
    </ul>
    <li><strong>Service-Oriented Architecture (SOA)</strong></li>
    <ul>
      <li>서비스 단위로 분리하여 느슨하게 결합된 구조.</li>
      <li>예: 기업용 ERP, ESB 기반 통합</li>
    </ul>
  </ul>
  <p><strong>정리: Architectural Patterns = 시스템을 어떻게 나누고 연결할지 정하는 설계 청사진</strong></p>
</section>

<!-- 설명 -->
<details open>
<summary><span class="accordion-title">Domain Driven Design(도메인 주도 설계)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>Domain-Driven Design(DDD)</b>는 핵심 비즈니스 도메인과 비즈니스 엔터티를 기반으로 소프트웨어 시스템을 설계하는 데 사용되는 아키텍처 패턴이다. 이 패턴은 소프트웨어 시스템 안에서 비즈니스 도메인을 명확하고 정확하게 표현하는 것과, 소프트웨어 시스템을 비즈니스 목표와 목적에 맞추는 것에 초점을 둔다.</p>
  <p>DDD는 다른 아키텍처 패턴보다 몇 가지 장점을 제공한다.</p>
  <ul>
    <li><strong>비즈니스 목표 및 목적과의 정렬(Alignment)</strong> </li>
    <li><strong>도메인 전문가와 개발자 간의 원활한 커뮤니케이션</strong> </li>
    <li><strong>비즈니스 도메인을 명확하고 표현력 있게 모델링 가능</strong> </li>
    <li><strong>더 나은 확장성과 유지보수성</strong> </li>
  </ul>
  <p>DDD는 <b>전략적 설계(Strategic Design), 서브도메인(Subdomains), 경계(Context, Bounded Context), 엔터티(Entity), 값 객체(Value Object), 애그리게이트(Aggregate), 리포지토리(Repository)</b> 와 같은 일련의 원칙과 패턴을 활용하여 구현된다.</p>
  <p><strong>정리: Domain-Driven Design는 비즈니스 도메인을 중심에 두고 소프트웨어를 설계하여, 시스템을 비즈니스 목표와 긴밀히 연결하는 아키텍처 패턴이다.</strong></p>

</div>
</details>


<!-- 설명 -->
<details>
<summary><span class="accordion-title">Model View Controller(MVC)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>Model-View-Controller(MVC)</b>는 소프트웨어 시스템의 관심사를 <b>모델(Model), 뷰(View), 컨트롤러(Controller)</b>라는 세 가지 별도의 구성 요소로 분리하는 아키텍처 패턴이다.</p>
  <ul>
    <li><strong>Model:</strong> 시스템의 데이터와 비즈니스 로직을 표현한다.</li>
    <li><strong>View:</strong> 시스템의 사용자 인터페이스(UI)를 표현한다.</li>
    <li><strong>Controller:</strong> 모델과 뷰 사이에서 중재자 역할을 한다.</li>
  </ul>
  <p>MVC의 주요 목표는 시스템의 관심사를 분리하여, 소프트웨어를 더 쉽게 이해하고, 유지보수하며, 발전시킬 수 있도록 하는 것이다. 이 패턴은 <b>웹 개발에서 널리 사용된다.</b></p>
  <p><strong>정리: MVC는 데이터(Model), 화면(View), 제어(Controller)를 분리해 유지보수성과 확장성을 높이는 아키텍처 패턴이다.</strong></p>

</div>
</details>


<!-- 설명 -->
<details>
<summary><span class="accordion-title">Microservices</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>Microservices</b>는 소프트웨어 시스템을 <b>작고 독립적이며 느슨하게 결합된 서비스들의 집합</b>으로 설계하는 데 사용되는 아키텍처 패턴이다. 각 서비스는 특정 기능에 책임을 지며, <b>독립적으로 개발, 배포, 확장</b>될 수 있다.</p>
  <p>마이크로서비스 아키텍처의 주요 장점은 <b>더 유연하고 확장 가능한 시스템</b>을 만들 수 있다는 점이다.또한, <b>장애 격리(Fault Isolation)</b>가 향상되고 <b>더 빠른 배포</b>가 가능하다.</p>
  <p>이 패턴은 종종 <b>이벤트 주도 아키텍처(Event-Driven Architecture), CQRS, 서비스 지향 아키텍처(SOA)</b> 등 다른 아키텍처 패턴 및 스타일과 함께 사용된다.</p>
  <p><strong>정리: Microservices는 작은 서비스 단위로 나누어 독립적 개발·배포·확장을 가능하게 하는 아키텍처 패턴이다.</strong></p>

</div>
</details>


<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Blackboard Pattern</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>Blackboard 아키텍처 패턴</b>은 여러 독립적인 모듈이나 서브시스템이 접근하고 수정할 수 있는 <b>중앙화된 저장소(blackboard)</b>를 만드는 소프트웨어 설계 패턴이다.</p>
  <p>블랙보드는 이러한 모듈들 사이에서 <b>정보 공유와 협력</b>을 가능하게 하는 <b>통신 및 조정 메커니즘</> 역할을 한다. 이를 통해 모듈들이 정보를 공유하고 협력하여 <b>공통의 목표를 달성</b>할 수 있다.</p>
  <p>이 패턴은 주로 <b>인공지능(AI) 및 의사결정 시스템</b>에서 사용되며, 여러 프로세스나 에이전트가 복잡한 데이터를 공유하고 추론해야 할 때 유용하다.</p>
  <p><strong>정리: Blackboard Pattern은 중앙 저장소(blackboard)를 통해 여러 모듈이 정보를 공유·협력하는 아키텍처 패턴이다.</strong></p>

</div>
</details>


<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Microkernel(마이크로커널)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>마이크로커널(Microkernel)</b>은 운영체제 설계에서 사용하는 아키텍처 패턴으로, 커널 모드(즉, 하드웨어 자원에 직접 접근할 수 있는 특권 모드)에서 실행되는 코드의 양을 최소화하고, 가능한 많은 기능을 <b>유저 모드(User Mode)</b>로 이동시키는 것을 목표로 한다.</p>
  <p>이를 위해 마이크로커널은 <b>메모리 관리, 프로세스 스케줄링, 프로세스 간 통신(IPC)</b> 같은 기본적인 작업만 처리하는 <b>작고 최소한의 핵심 커널</b>을 제공하며, 그 외의 모든 기능은 <b>유저 모드 프로세스</b>에서 구현되도록 한다.</p>
  <p><strong>정리: Microkernel은 최소한의 핵심 기능만 커널에 두고, 나머지는 유저 모드에서 처리하는 운영체제 아키텍처 패턴이다.</strong></p>

</div>
</details>



<!-- 설명 -->
<details>
<summary><span class="accordion-title">Serverless Architecture(서버리스 아키텍처)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>서버리스 아키텍처(Serverless Architecture)</b>는 개발자가 서버를 프로비저닝(할당)하거나 관리하지 않고도 애플리케이션과 서비스를 구축하고 실행할 수 있게 해주는 설계 패턴이다. 대신 이러한 애플리케이션과 서비스는 <b>AWS Lambda, Azure Functions, Google Cloud Functions</b> 같은 <b>완전히 관리되는 환경</b>에서 실행되며, 인프라 관리와 확장은 클라우드 제공자가 자동으로 처리한다.</p>
  <p>이 아키텍처 패턴은 <b>서버 관리보다 비즈니스 로직과 이벤트 기반 실행</b>에 초점을 맞춘다. 개발자는 DB의 변경이나 스트림에 새로운 데이터가 들어오는 것과 같은 <b>특정 이벤트에 의해 트리거되는 작고 단일 목적의 함수</b>를 작성하고 배포할 수 있다.</p>
  <p><strong>정리: Serverless는 서버 관리 없이 이벤트 기반으로 동작하는 단일 목적 함수 실행 아키텍처 패턴이다.</strong></p>

</div>
</details>



<!-- 설명 -->
<details>
<summary><span class="accordion-title">Message Queues & Streams(메시지 큐와 스트림)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>메시지 큐(Message Queues)와 스트림(Streams)</b>은 시스템의 서로 다른 구성 요소들을 분리(Decouple)하고, 그들 간의 <b>비동기 통신</b>을 가능하게 하는 아키텍처 패턴이다.</p>
  <p>메시지 큐(Message Queues)</p>
  <p>메시지 큐는 여러 시스템이나 애플리케이션이 서로 <b>메시지를 주고받으며 통신</b>할 수 있도록 해주는 소프트웨어 구성 요소이다. 메시지는 <b>큐(queue)</b>에 저장되고, 각 메시지는 <b>단일 소비자(consumer)</b>에 의해 처리된다. 이 패턴은 <b>메시지 생성 속도와 소비 속도의 변동이 큰 시스템이나, 송신자와 수신자가 동시에 활성 상태일 필요가 없는 경우</b>에 유용하다. 대표적인 메시지 큐 시스템으로는 <b>Apache Kafka, RabbitMQ, Amazon SQS</b>가 있다.</p>
  <p>스트림 (Streams)</p>
  <p>스트림은 메시지가 <b>실시간으로 연속적으로 전송되고 처리되는 방식</b>을 지원한다. 즉, 메시지가 큐에 쌓였다가 하나씩 처리되는 것이 아니라, 데이터가 들어오는 즉시 여러 소비자가 동시에 처리할 수 있다. 이 패턴은 <b>실시간 분석, 이벤트 처리, 로그 수집, IoT 데이터 처리</b> 같은 시나리오에서 자주 사용된다. 대표적인 스트리밍 플랫폼으로는 <b>Apache Kafka(스트리밍 모드), Apache Flink, Amazon Kinesis</b>가 있다.</p>
  <p><strong>정리: Message Queue는 메시지를 큐에 저장해 비동기적으로 처리하고 Stream은 데이터를 실시간으로 처리한다.</strong></p>

</div>
</details>


<!-- 설명 -->
<details>
<summary><span class="accordion-title">Event Sourcing</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>Event Sourcing</b>은 시간이 지나면서 발생한 <b>모든 변경 이력을 유지해야 하는 시스템</b>을 구축할 때 사용되는 아키텍처 패턴이다. 이 패턴은 시스템의 현재 상태만 저장하는 것이 아니라, <b>상태 변화의 모든 기록을 이벤트(event)의 순서로 저장</b>한다.</p>
  <p>Event Sourcing에서 시스템 상태의 모든 변경은 <b>이벤트(event)</b>로 간주되며, 이 이벤트들은 <b>추가만 가능한 로그(append-only log)</b>, 즉 <b>이벤트 저장소(event store)</b>에 저장된다. 시스템의 현재 상태는 필요할 때마다 이벤트 로그를 순차적으로 재생(replay)하여 <b>이전 시점의 상태까지 재구성</b>할 수 있다.</p>
  <p><strong>정리: Event Sourcing은 시스템 상태를 직접 저장하지 않고 모든 변경을 이벤트 로그로 기록해 언제든 재구성하는 패턴이다.</strong></p>

</div>
</details>


<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">SOA(Service-Oriented Architecture, 서비스 지향 아키텍처)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>SOA(Service-Oriented Architecture, 서비스 지향 아키텍처)</b>는 소프트웨어 시스템을 <b>네트워크를 통해 접근 가능한 서비스들의 집합</b>으로 설계하고 구성하는 데 사용되는 아키텍처 패턴이다. 이 서비스들은 <b>자율적이고(self-contained), 독립적인 기능 단위</b>이며, 재사용될 수 있고 조합되어 새로운 기능을 만들 수 있다.</p>
  <p>SOA의 서비스들은 <b>느슨하게 결합(loose coupling)</b>되도록 설계되는데, 이는 각 서비스가 다른 서비스의 구현 세부 사항에 의존하지 않음을 의미한다. 서비스 간 통신은 <b>명확하게 정의된 인터페이스</b>를 통해 이루어지며, 일반적으로 <b>HTTP나 SOAP 같은 프로토콜</b>을 사용한다.</p>
  <p>SOA는 다른 아키텍처 패턴에 비해 여러 가지 장점을 제공한다. 예: <b>재사용성, 모듈성, 상호운용성, 확장성</b></p>
  <p>SOA는 다양한 기술로 구현될 수 있으며, <b>웹 서비스(Web Services), REST, 마이크로서비스(Microservices)</b> 등이 있다.</p>
  <p><strong>정리: SOA는 네트워크로 접근 가능한 독립적 서비스들을 느슨하게 결합해 재사용성과 확장성을 높이는 아키텍처 패턴이다.</strong></p>

</div>
</details>


<!-- 설명 -->
<details>
<summary><span class="accordion-title">CQRS(Command Query Responsibility Segregation, 명령-조회 책임 분리)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>CQRS (Command Query Responsibility Segregation, 명령-조회 책임 분리)**는 소프트웨어 시스템에서 데이터 쓰기(명령)와 읽기(조회)의 책임을 분리하는 데 사용되는 아키텍처 패턴이다.</p>
  <p>CQRS 아키텍처에서는 시스템이 두 부분으로 나뉜다.</p>
  <ul>
    <li><strong>Command Side (명령 측)</strong> → 명령을 처리하고 시스템의 상태를 업데이트하는 역할</li>
    <li><strong>Query Side (조회 측)</strong> → 시스템의 현재 상태를 읽고 결과를 클라이언트에 반환하는 역할</li>
  </ul>
  <p>명령 측과 조회 측은 서로 다른 데이터 모델, 저장 방식, 심지어 다른 기술까지 사용할 수 있다.</p>
  <p><strong>정리: CQRS는 쓰기와 읽기를 분리해 성능, 확장성, 복잡한 도메인 처리를 최적화하는 아키텍처 패턴이다.</strong></p>

</div>
</details>
