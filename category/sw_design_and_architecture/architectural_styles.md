---
layout: default
title: "Architectural Styles"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>Architectural Styles</h2>
  <p>소프트웨어에서 <b>아키텍처 스타일(Architectural styles)</b>은 SW 시스템의 전체적인 설계와 조직 그리고 설계를 이끄는 원칙과 패턴을 의미한다. 이러한 스타일은 시스템 설계에 대한 일반적인 프레임워크를 제공하며, 시스템이 잘 구조화되고, 유지보수가 용이하며, 확장 가능하도록 만드는 데 사용될 수 있다.</p>
  <p>SW에서 흔히 볼 수 있는 아키텍처 스타일에는 다음과 같은 것들이 있다.</p>
  <ul>
    <li><strong>마이크로서비스(Microservices):</strong> 시스템을 작고 독립적이며 느슨하게 결합된 서비스들의 집합으로 구성하는 방식</li>
    <li><strong>이벤트 기반(Event-Driven):</strong> 시스템이 변화 여부를 지속적으로 확인(polling)하는 대신, 특정 이벤트가 발생했을 때 반응하도록 설계하는 방식</li>
    <li><strong>계층형(Layered):</strong> 시스템을 여러 계층으로 나누고, 각 계층은 특정한 책임을 가지며 잘 정의된 인터페이스를 통해 다른 계층과 통신하는 방식</li>
    <li><strong>서비스 지향(Service-Oriented):</strong> 시스템을 네트워크를 통해 접근 가능한 서비스들의 집합으로 구성하는 방식</li>
    <li><strong>데이터 중심(Data-Centric):</strong> 데이터를 처리하는 것보다 <b>저장, 검색, 조작</b>에 초점을 맞춘 방식</li>
    <li><strong>컴포넌트 기반(Component-Based):</strong> 재사용 가능하고 독립적인 소프트웨어 컴포넌트들로 시스템을 구성하는 방식</li>
    <li><strong>도메인 주도(Domain-Driven):</strong> 시스템을 핵심 비즈니스 도메인과 비즈니스 엔티티를 중심으로 조직하는 방식</li>
  </ul>
  <p><strong>정리: Architectural styles는 소프트웨어 시스템을 어떻게 구조화할지에 대한 큰 틀(프레임워크)이며, 대표적으로 Microservices, Event-Driven, Layered, SOA, Data-Centric, Component-Based, Domain-Driven 등이 있다.</strong></p>
</section>

<!-- 설명 -->
<details open>
<summary><span class="accordion-title">Structural(구조적 스타일)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>SW에서 구조적 아키텍처(Structural architecture)</b>는 SW 시스템의 컴포넌트들을 어떻게 조직하고 설계할 것인지, 그리고 이들이 서로 어떻게 상호작용하는지를 의미한다. 이는 시스템의 물리적 조직과 서로 다른 컴포넌트 간의 관계를 다룬다.</p>
  <p>소프트웨어 시스템을 설계할 때 사용할 수 있는 여러 가지 구조적 아키텍처 패턴과 스타일에는 다음이 있다.</p>
  <ul>
    <li><strong>모놀리식(Monolithic):</strong> 시스템을 하나의 통합되고 독립적인 단위로 구축하는 방식</li>
    <li><strong>계층형(Layered):</strong> 시스템을 여러 계층으로 나누고, 각 계층은 특정 책임을 가지며 잘 정의된 인터페이스를 통해 다른 계층과 통신하는 방식</li>
    <li><strong>마이크로서비스(Microservices):</strong> 시스템을 작고 독립적이며 느슨하게 결합된 서비스들의 집합으로 구축하는 방식</li>
    <li><strong>이벤트 기반(Event-driven):</strong> 변화 여부를 지속적으로 확인(polling)하는 대신, 특정 이벤트가 발생했을 때 반응하도록 설계하는 방식</li>
    <li><strong>클라이언트-서버(Client-Server):</strong> 클라이언트가 서버에 요청을 보내면, 서버가 그 요청에 응답하는 방식</li>
    <li><strong>피어-투-피어(Peer-to-Peer):</strong> 네트워크의 각 노드가 클라이언트이자 서버로서 동작하는 방식</li>
    <li><strong>컴포넌트 기반(Component-based):</strong> 시스템을 재사용 가능하고 독립적인 소프트웨어 컴포넌트들로 구성하는 방식</li>
    <li><strong>도메인 주도(Domain-Driven):</strong> 시스템을 핵심 비즈니스 도메인과 비즈니스 엔티티를 중심으로 조직하는 방식</li>
  </ul>
  <p><strong>정리: Structural architecture는 시스템의 물리적 구조와 컴포넌트 간의 관계를 정의하며, 대표적인 패턴으로 Monolithic, Layered, Microservices, Event-driven, Client-Server, Peer-to-Peer, Component-based, Domain-Driven 등이 있다.</strong></p>

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title">Component-Based (컴포넌트 기반) </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>소프트웨어 아키텍처에서 <b>컴포넌트 기반 설계(Component-Based Design, CBD)</b>는 소프트웨어 시스템을 <b>재사용 가능하고 독립적인 소프트웨어 컴포넌트들의 집합으로 구성</b>하여 설계하는 접근 방식이다. 이러한 컴포넌트들은 특정 기능을 캡슐화하며, 시스템의 다른 부분에 쉽게 통합될 수 있어 보다 모듈화되고 유연한 설계를 가능하게 한다.</p>
      <p>CBD에서 소프트웨어 시스템은 여러 컴포넌트로 나뉘며, 각 컴포넌트는 <b>명확히 정의된 인터페이스</b>와 <b>특정한 책임</b>을 가진다. 이 컴포넌트들은 독립적으로 개발, 테스트, 배포가 가능하므로, 새로운 기능을 추가하거나 기존 기능을 수정하고 시스템을 유지보수하는 것이 훨씬 쉬워진다.</p>
      <p><strong>정리: CBD는 명확한 인터페이스와 책임을 가진 독립적인 컴포넌트들의 조합으로 시스템을 설계해, 모듈성·유연성·유지보수성을 높이는 방법이다.</strong></p>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title">Monolithic(모놀리식) </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>소프트웨어 아키텍처에서 <b>모놀리식 아키텍처(Monolithic architecture)</b>는 소프트웨어 시스템을 <b>하나의 통합되고 독립적인 단위</b>로 구축하는 설계 방식이다. 모놀리식 아키텍처에서는 시스템의 모든 컴포넌트가 강하게 결합(tightly coupled)되어 서로 의존한다. 이는 시스템의 한 부분이 변경되면 다른 부분에도 영향을 미칠 수 있음을 의미한다.</p>
      <p>모놀리식 아키텍처는 보통 <b>작은 규모에서 중간 규모의 시스템</b>에 사용되며, 이 경우 시스템의 복잡성이 관리 가능한 수준이고 확장성과 유연성에 대한 요구가 크지 않다. 모놀리식 아키텍처에서는 전체 시스템이 일반적으로 하나의 단위로 <b>빌드, 배포, 실행</b>되며, 이는 시스템을 이해하고 관리하기 더 쉽게 만들어준다</p>
      <p><strong>정리: 모놀리식 아키텍처는 시스템을 하나의 통합된 단위로 구축하는 방식으로, 관리와 이해는 쉽지만 확장성과 유연성은 떨어진다.</strong></p>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title">Layered(계층형) </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>소프트웨어 아키텍처에서 <b>계층형 아키텍처(Layered architecture)</b>는 소프트웨어 시스템을 여러 계층(layers)으로 나누는 설계 방식이다. 각 계층은 <b>특정한 책임</b>을 가지고 있으며, <b>잘 정의된 인터페이스</b>를 통해 다른 계층과 통신한다. 이러한 접근 방식은 설계를 더 <b>모듈화(modular)</b>하고 <b>유연(flexible)</b>하게 만들어, 각 계층을 독립적으로 개발, 테스트, 배포할 수 있도록 하여 새로운 기능 추가, 기존 기능 수정, 시스템 유지보수를 더 쉽게 만든다.</p>
      <p>계층형 아키텍처는 보통 <b>규모가 크고 복잡한 시스템</b>에서 사용되며, 이 경우 확장성과 유연성에 대한 요구가 크다. 계층형 아키텍처의 각 계층은 특정 기능에 책임을 지며, <b>잘 정의된 인터페이스를 가진 블랙박스</b>로 생각할 수 있다. 계층 간에는 이 인터페이스를 통해 통신하므로, <b>관심사의 명확한 분리(Separation of Concerns)</b>가 가능하다.</p>
      <p><strong>정리: 계층형 아키텍처는 시스템을 계층별로 나눠 책임을 분리하고, 인터페이스를 통해 통신함으로써 모듈성·유연성·유지보수성을 높이는 설계 방식이다.</strong></p>
    </div>
  </details>

</div>
</details>


<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Distributed</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>분산 시스템(Distributed systems)</b>은 여러 장치나 위치에 분산된 소프트웨어 컴포넌트들을 네트워크로 연결하고, 이들이 함께 동작하여 <b>공통의 목표를 달성</b>하도록 설계·조직하는 것을 의미한다. 분산 시스템 설계에서의 주요 과제는 컴포넌트가 분산되어 있고 이들 간에 통신이 이루어진다는 점에서 발생하는 <b>내재된 복잡성</b>을 다루는 것이다. 이를 해결하기 위해 <b>부하 분산(load balancing), 복제(replication), 파티셔닝(partitioning)</b>과 같은 기법을 사용하여 <b>확장성, 내결함성(fault-tolerance), 성능</b>을 향상시켜야 한다. 또한, <b>보안(security)과 조율(coordination)</b> 역시 분산 시스템에서 중요한 요소이다.</p>
  <p><strong>정리: 분산 시스템은 여러 노드가 네트워크를 통해 협력하는 구조로, 확장성·내결함성·성능·보안·조율이 핵심 과제다.</strong></p>

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title" style="color: #000; font-weight: bold;">Client Server </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p><b>클라이언트-서버 아키텍처(Client-Server architecture)</b>는 분산 시스템에서 흔히 사용되는 아키텍처 패턴으로, <b>클라이언트(또는 다수의 클라이언트)</b>가 서버에 요청(request)을 보내면, 서버가 그 요청에 응답(response)하는 구조이다. 클라이언트와 서버는 별개의 개체이며, 인터넷이나 로컬 네트워크 같은 네트워크를 통해 서로 통신한다.</p>
      <p>클라이언트는 <b>사용자 인터페이스를 표시하고 사용자 입력을 처리</b>하는 역할을 맡고, 서버는 <b>요청을 처리하고 적절한 응답을 반환</b>하는 역할을 맡는다. 또한 서버는 <b>데이터 저장, 보안, 비즈니스 로직</b>과 같은 작업을 담당할 수도 있다.</p>
      <p><strong>정리: 클라이언트-서버 아키텍처는 클라이언트가 요청하고 서버가 응답하는 구조로, UI·입력은 클라이언트가, 처리·저장·보안은 서버가 담당한다.</strong></p>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title" style="color: #000; font-weight: bold;">Peer to Peer </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p><b>피어-투-피어(Peer-to-Peer, P2P) 아키텍처</b>는 분산 컴퓨팅 아키텍처의 한 형태로, 네트워크의 각 노드(peer)가 동시에 <b>클라이언트이자 서버</b> 역할을 하는 구조이다. P2P 아키텍처에서는 네트워크를 관리하는 중앙 권한이나 서버가 없으며, 각 노드는 다른 노드와 직접 통신하여 <b>정보를 교환, 자원을 공유, 연산 수행</b>을 한다.</p>
      <p>P2P 아키텍처의 주요 장점은 시스템을 더 <b>탈중앙화(decentralized)</b>하고 <b>내결함성(fault-tolerant)</b> 있게 만들 수 있다는 점이다. 중앙 권한이 없기 때문에 단일 장애 지점(single point of failure)이 존재하지 않으며, 일부 노드가 실패하더라도 네트워크는 계속 동작할 수 있다. 또한, P2P 아키텍처는 네트워크 내 노드 수가 증가할수록 <b>확장성(scalability)</b>도 향상될 수 있다.</p>
      <p><strong>정리: P2P 아키텍처는 각 노드가 클라이언트이자 서버로 동작해 중앙 서버 없이도 확장성과 내결함성을 가지는 탈중앙화 구조다.</strong></p>
    </div>
  </details>

</div>
</details>


<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Messaging(메시징)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>Messaging</b>은 이벤트 주도 아키텍처(EDA), 마이크로서비스, 메시지 주도 아키텍처(MDA) 등 여러 아키텍처 스타일에서 핵심 개념이다.</p>
  <ul>
    <li><strong>이벤트 주도 아키텍처(Event-Driven Architecture, EDA)</strong> </li>
    <li><strong>마이크로서비스(Microservices)</strong> </li>
    <li><strong>메시지 주도 아키텍처(Message-Driven Architecture, MDA)</strong> </li>
  </ul>
  <p>일반적으로 메시징은 시스템을 <b>디커플링(decoupling, 결합도 낮추기)</b>하고 <b>확장성(scalability)</b>을 높일 수 있게 해주는 강력한 개념이다. 메시징은 다양한 아키텍처 스타일에서 활용되며, 컴포넌트 간의 <b>느슨한 결합(loose coupling)</b>을 가능하게 하고, 새로운 기능을 추가하거나 기존 기능을 수정하는 것을 더 쉽게 만들어 시스템의 <b>유연성(flexibility)</b>과 확장성을 개선한다.</p>
  <p><strong>정리: 메시징은 EDA, 마이크로서비스, MDA 등에서 컴포넌트 간 결합도를 낮춰 시스템의 유연성과 확장성을 높이는 핵심 개념이다.</strong></p>
  

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title" style="color: #000; font-weight: bold;">Event Driven </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p><b>이벤트 주도 아키텍처(EDA)</b>는 시스템이 변화를 계속 폴링(polling)하는 대신, 발생하는 <b>특정 이벤트에 반응</b>하도록 설계하는 소프트웨어 패턴이다. EDA에서 <b>이벤트는 컴포넌트 사이에 비동기적으로 전달되는 메시지</b>이며, 각 컴포넌트는 자신이 관심 있는 이벤트에 반응한다. </p>
      <p>EDA의 주요 장점은 <b>컴포넌트 간 관심사의 명확한 분리</b>를 가능하게 하고, <b>확장성과 내결함성</b>을 향상시킨다는 점이다. 또한 컴포넌트 간 <b>느슨한 결합(Loose Coupling)</b>을 제공하여, 서로의 존재를 알 필요 없이 <b>독립적으로 개발·배포·확장</b>할 수 있게 한다.</p>
      <p><strong>정리: EDA(Event-Driven Architecture)는 이벤트를 비동기 메시지로 전달해 컴포넌트 간 결합도를 낮추고, 확장성과 내결함성을 높이는 아키텍처다.</strong></p>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title" style="color: #000; font-weight: bold;">Publish Subscribe </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p><b>퍼블리시-서브스크라이브 패턴(Publish-Subscribe pattern)</b>은 메시징 패턴의 하나로, 퍼블리셔(publisher)가 메시지를 특정 <b>토픽(topic)</b>에 발행하면, 그 토픽을 구독한(subscribe) 임의의 수의 구독자(subscriber)들이 해당 메시지를 수신하는 방식이다. 퍼블리시-서브스크라이브 패턴은 <b>옵저버 패턴(Observer pattern)</b>이라고도 불리며, 애플리케이션의 서로 다른 부분 간에 <b>디커플링된 방식</b>으로 통신을 구현하는 방법이다.</p>
      <p>이 패턴을 사용할 때의 주요 장점은 퍼블리셔와 구독자 간의 <b>관심사 분리(Separation of Concerns)</b>를 명확하게 할 수 있고, 시스템의 <b>유연성(flexibility)</b>과 <b>확장성(scalability)</b>을 향상시킬 수 있다는 점이다. 또한, 퍼블리셔와 구독자가 서로의 존재를 알 필요가 없으므로 <b>느슨한 결합(loose coupling)</b>을 가능하게 하며, 각자가 독립적으로 <b>개발, 배포, 확장</b>될 수 있다.</p>
      <p><strong>정리: Publish-Subscribe 패턴은 퍼블리셔와 구독자가 토픽을 매개로 메시지를 주고받아, 느슨한 결합과 확장성을 보장하는 메시징 패턴이다.</strong></p>
    </div>
  </details>

</div>
</details>
