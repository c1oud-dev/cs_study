---
layout: default
title: "Design Patterns"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>Design Patterns</h2>
  <p>
  디자인 패턴(Design Patterns) 은 SW 개발에서 자주 발생하는 문제들에 대한 일반적인 해결책이다. 이는 검증된 설계 문제의 해결 방식을 설명하고 전달할 수 있는 방법을 제공하며, 설계를 위한 공통된 어휘를 제공한다. 디자인 패턴은 특정 프로그래밍 언어나 기술에 종속되지 않고, 문제와 해결책을 다양한 맥락에 적용할 수 있도록 기술한다.
  </p>
  <p>
  디자인 패턴에는 여러 가지 유형이 있으며, 그 예시는 다음과 같다.
  <ul>
    <li><strong>생성 패턴(Creational patterns)</strong></li>
    <li><strong>구조 패턴(Structural patterns)</strong></li>
    <li><strong>행위 패턴(Behavioral patterns)</strong></li>
    <li><strong>아키텍처 패턴(Architectural patterns)</strong></li>
  </ul>
  </p>
</section>

<!-- 설명 -->
<details open>
<summary><span class="accordion-title">GoF Design Patterns</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  Gang of Four (GoF) 디자인 패턴은 객체 지향 소프트웨어 개발을 위한 디자인 패턴 모음으로, 에리히 감마(Erich Gamma), 리처드 헬름(Richard Helm), 랄프 존슨(Ralph Johnson), 존 블리시디스(John Vlissides) ― 일명 Gang of Four(GoF) ― 가 집필한 책 『Design Patterns: Elements of Reusable Object-Oriented Software』 에서 처음 소개되었다.
  </p>
  <p>
  GoF 디자인 패턴은 크게 세 가지 범주로 나눌 수 있다.
  </p>

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title">생성 패턴 (Creational Patterns) </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      생성 패턴은 객체 생성 방식에 대한 패턴으로, 객체 생성 과정을 캡슐화하여 코드가 구체적인 클래스에 의존하지 않도록 돕는다. 이를 통해 객체 생성 로직을 유연하게 하고, 재사용성과 확장성을 높일 수 있다. 대표적인 예시로는 싱글턴(Singleton), 팩토리 메서드(Factory Method), 추상 팩토리(Abstract Factory), 빌더(Builder), 프로토타입(Prototype) 패턴이 있다.
      </p>
      <p><strong>정리: 생성 패턴은 객체 생성 과정을 캡슐화해 유연하고 독립적인 생성 방법을 제공한다.</strong></p>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title">구조 패턴 (Structural Patterns) </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      구조 패턴은 클래스나 객체를 조합해 더 큰 구조를 만드는 방법에 관한 패턴이다. 객체 간의 관계를 효율적으로 설계하여 재사용성을 극대화하고, 복잡한 시스템을 단순한 구조로 표현할 수 있게 한다. 대표적인 예시는 어댑터(Adapter), 브리지(Bridge), 컴포지트(Composite), 데코레이터(Decorator), 퍼사드(Facade), 플라이웨이트(Flyweight), 프록시(Proxy) 패턴이 있다.
      </p>
      <p><strong>정리: 구조 패턴은 객체와 클래스를 조합해 더 큰 구조를 만들고 재사용성을 높인다.</strong></p>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title">행위 패턴 (Behavioral Patterns) </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      행위 패턴은 객체 간의 상호작용과 책임 분배 방식에 관한 패턴이다. 객체들이 서로 메시지를 주고받으며 협력하는 방법을 정의하여 유연하고 확장 가능한 동작을 구현할 수 있게 한다. 대표적인 예시는 책임 연쇄(Chain of Responsibility), 커맨드(Command), 인터프리터(Interpreter), 반복자(Iterator), 중재자(Mediator), 메멘토(Memento), 옵서버(Observer), 상태(State), 전략(Strategy), 템플릿 메서드(Template Method), 방문자(Visitor) 패턴이 있다.
      </p>
      <p><strong>정리: 행위 패턴은 객체 간 상호작용과 책임 분배를 정의해 유연한 협력을 가능하게 한다.</strong></p>
    </div>
  </details>

</div>
</details>


<!-- 설명 -->
<details>
<summary><span class="accordion-title">POSA Patterns</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  POSA (Pattern-Oriented Software Architecture) 는 변화하는 요구사항에 맞춰 확장 가능하고 적응할 수 있는 소프트웨어 시스템을 개발하기 위한 디자인 패턴 집합이다. 이 패턴들은 Kevin Hoffman이 집필한 책 『Patterns of Scalable, Reliable Services』 에서 처음 소개되었다.
  </p>
  <p>
  POSA 패턴은 크게 네 가지 범주로 나눌 수 있다.
  </p>

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title">Partitioning Patterns (분할 패턴) </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      분할 패턴은 시스템을 더 작은 단위로 나누는 방법을 다룬다. 대규모 시스템을 기능, 데이터, 책임 단위로 분할하여 확장성과 병렬 처리 효율을 높인다. 예를 들어, 샤딩(Sharding), 계층 분할(Layered Architecture) 같은 개념이 포함된다.
      </p>
      <p><strong>정리: 분할 패턴은 시스템을 쪼개어 확장성과 병렬성을 높인다.</strong></p>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title">Placement Patterns (배치 패턴) </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      배치 패턴은 분할된 컴포넌트를 어디에, 어떻게 배치할지를 다룬다. 즉, 어떤 서버, 프로세스, 노드에 기능을 배치할지 결정하여 성능, 가용성, 비용을 최적화한다. 예시로는 리소스 풀링(Resource Pooling), 데이터베이스 복제(Replication) 전략이 있다.
      </p>
      <p><strong>정리: 배치 패턴은 분할된 요소를 어디에 배치할지 결정한다.</strong></p>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title">Routing Patterns (라우팅 패턴) </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      라우팅 패턴은 사용자의 요청을 올바른 컴포넌트나 서비스로 전달하는 방법을 다룬다. 트래픽을 분산하고, 올바른 처리 단위로 연결시켜 신뢰성과 부하 분산을 보장한다. 대표적인 예시는 로드 밸런서(Load Balancer), 메시지 라우터(Message Router) 가 있다.
      </p>
      <p><strong>정리: 라우팅 패턴은 요청을 올바른 컴포넌트로 전달한다.</strong></p>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title">Federation Patterns (연합 패턴) </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      연합 패턴은 여러 독립된 시스템이나 서비스가 하나의 통합된 시스템처럼 동작하도록 하는 방법을 다룬다. 각 서비스가 자율성을 가지면서도 협력할 수 있도록 하여 확장성과 유연한 통합을 가능하게 한다. 예시로는 API 게이트웨이, 서비스 연합(Service Federation) 같은 개념이 있다.
      </p>
      <p><strong>정리: 연합 패턴은 여러 시스템을 연합해 하나처럼 동작시킨다.</strong></p>
    </div>
  </details>

</div>
</details>
