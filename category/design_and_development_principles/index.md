---
layout: default
title: "Design and Development Principles"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>Design and Development Principles</h2>
  <p><b>설계 및 개발 원칙(Design and Development Principles)</b>은 소프트웨어 시스템을 만들 때 지침이 되는 근본적인 가이드라인이다. 주요 원칙들은 다음과 같다.</p>
  <ul>
    <li><strong>SOLID:</strong> 단일 책임 원칙(Single Responsibility), 개방-폐쇄 원칙(Open-Closed), 리스코프 치환 원칙(Liskov Substitution), 인터페이스 분리 원칙(Interface Segregation), 의존 역전 원칙(Dependency Inversion)</li>
    <li><strong>DRY(Don't Repeat Yourself):</strong> 동일한 코드를 반복하지 말라.</li>
    <li><strong>KISS(Keep It Simple, Stupid):</strong> 단순하게 유지하라.</li>
    <li><strong>YAGNI(You Aren't Gonna Need It):</strong> 필요하지 않은 기능은 만들지 말라.</li>
    <li><strong>Separation of Concerns(관심사 분리):</strong> 서로 다른 기능이나 역할을 분리하라.</li>
    <li><strong>Modularity(모듈성):</strong> 시스템을 독립적인 모듈 단위로 나눠라.</li>
    <li><strong>Encapsulation(캡슐화):</strong> 데이터와 동작을 하나로 묶고 외부에서 숨겨라.</li>
    <li><strong>Composition over Inheritance(상속보다 합성 우선):</strong> 코드 재사용 시 상속보다 합성을 활용하라.</li>
    <li><strong>Loose Coupling and High Cohesion(낮은 결합도와 높은 응집도):</strong> 컴포넌트 간 의존성은 줄이고 내부의 관련성은 높여라.</li>
    <li><strong>Principle of Least Astonishment(최소 놀람의 원칙):</strong> 사용자가 예상하지 못한 동작을 최소화하라.</li>
  </ul>
  <p><strong>정리: 설계·개발 원칙은 단순성, 재사용성, 유연성을 높이는 소프트웨어 지침이다.</strong></p>
</section>

<!-- 설명 -->
<details open>
<summary><span class="accordion-title">GoF Design Patterns</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>GoF(Gang of Four) 디자인 패턴</b>은 객체지향 설계에서 흔히 발생하는 문제들을 해결하기 위해 만들어진 <b>23가지 기초 소프트웨어 디자인 패턴</b>의 집합이다. 이 패턴들은 세 가지 범주로 나뉜다.</p>
  <ul>
    <li><strong>생성 패턴(Creational):</strong> 객체 생성에 초점을 맞춘 패턴(예: 싱글톤, 팩토리)</li>
    <li><strong>구조 패턴(Structural):</strong> 클래스와 객체의 구성 방식에 초점을 맞춘 패턴(예: 어댑터, 컴포지트)</li>
    <li><strong>행위 패턴(Behavioral):</strong> 객체 간의 커뮤니케이션에 초점을 맞춘 패턴(예: 옵저버, 전략)</li>
  </ul>
  <p>각 패턴은 특정 설계 문제를 해결하기 위한 검증된 템플릿을 제공하며, 코드의 <b>재사용성, 유연성, 유지보수성</b>을 향상시킨다.</p>
  <p><strong>정리: GoF 디자인 패턴은 생성·구조·행위 3가지로 나뉜 23개의 객체지향 문제 해결 템플릿이다.</strong></p>

</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title">Domain-Driven Design(DDD, 도메인 주도 설계)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>도메인 주도 설계</b>는 비즈니스 도메인에 대한 깊은 이해를 바탕으로 소프트웨어 시스템을 설계하는 개발 접근 방식이다. 이는 기술 전문가와 도메인 전문가가 긴밀히 협력하여 <b>공용 언어(Ubiquitous Language)</b>와 비즈니스의 핵심 개념 및 프로세스를 정확히 반영하는 모델을 함께 개발하는 것을 강조한다.</p>
  <p>DDD는 코드를 비즈니스 개념(경계 컨텍스트, Bounded Context)을 중심으로 조직화하고, 비즈니스 로직을 풍부하게 담은 도메인 모델을 사용하며, 도메인 로직을 인프라스트럭처 관심사와 분리하는 것을 권장한다. 대표적인 DDD 패턴으로는 <b>엔티티(Entity), 값 객체(Value Object), 애그리게이트(Aggregate), 리포지토리(Repository), 도메인 서비스(Domain Service)</b>가 있다.</p>
  <p>이 접근 방식의 목표는 <b>비즈니스 요구와 밀접하게 일치</b>하고, 변화하는 요구에도 진화할 수 있는 유지보수성과 유연성이 높은 소프트웨어 시스템을 만드는 것이다. 특히 DDD는 전통적인 CRUD 기반 아키텍처가 비즈니스의 세부 규칙과 뉘앙스를 포착하기 어려운 <b>복잡한 도메인</b>에서 큰 가치를 가진다.</p>
  <p><strong>정리: DDD는 비즈니스 도메인 이해를 중심으로 모델과 언어를 설계하는 복잡 도메인 해결 접근법이다.</strong></p>
  <!-- 가로선 추가 -->
  <hr>
  <ul>
    <li><strong>공용 언어(Ubiquitous Language):</strong> 개발자와 도메인 전문가가 공통으로 사용하는 언어로, 코드와 대화 속 용어를 일치시켜 오해를 줄이고 비즈니스 도메인을 정확히 표현한다.</li>
    <li><strong>인프라스트럭처 관심사(Infrastructure Concerns):</strong> DB, 네트워크, 메시징 같은 기술적 구현 세부사항을 가리키며, DDD에서는 도메인 로직과 분리하여 관리한다.</li>
    <li><strong>애그리게이트(Aggregate):</strong> 밀접하게 연관된 엔티티와 값 객체들을 하나로 묶은 일관성 있는 단위로, 항상 루트 엔티티(Aggregate Root)를 통해 접근·변경된다.</li>
  </ul>

</div>
</details>


<!-- 설명 -->
<details>
<summary><span class="accordion-title">Test Driven Development(TDD, 테스트 주도 개발) </span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>테스트 주도 개발</b>은 소프트웨어 요구사항에 대한 테스트를 먼저 작성하고, 이 테스트가 통과할 수 있도록 소프트웨어를 개발하는 과정이다. 처음에는 테스트가 실패하지만, 요구사항을 충족하는 코드를 작성하면 테스트가 통과한다. 이후에는 코드를 리팩토링하거나 새로운 기능·요구사항에 대한 테스트를 작성하는 사이클을 반복한다.</p>
  <p>이론적으로 TDD는 소프트웨어가 <b>가장 단순한 형태로 요구사항을 충족하도록 보장</b>하며, 코드 결함을 예방하는 데 도움이 된다.</p>
  <p><strong>정리: TDD는 테스트를 먼저 작성하고, 이를 통과시키며 개발하는 사이클이다.</strong></p>

</div>
</details>


<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">CQRS(Command Query Responsibility Segregation) </span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>CQRS</b>는 데이터 저장소의 읽기와 쓰기 작업을 분리하는 아키텍처 패턴이다. 이 패턴에서 <b>Command(명령)</b>는 데이터 수정(생성, 갱신, 삭제)을 처리하고, <b>Query(조회)</b>는 데이터 조회를 처리한다.</p>
  <p>CQRS의 핵심 원칙은 많은 시스템(특히 복잡한 시스템)에서 <b>데이터 읽기 요구사항과 쓰기 요구사항이 크게 다르다</b>는 점이다. 이러한 관심사를 분리함으로써 CQRS는 읽기와 쓰기 측면을 독립적으로 확장, 최적화, 발전시킬 수 있도록 한다. 이는 성능, 확장성, 보안성을 향상시킬 수 있다.</p>
  <p>CQRS는 이벤트 소싱(Event Sourcing) 기반 시스템에서 자주 사용되며, <b>고성능·복잡한 도메인 애플리케이션</b>에서 특히 유용하다. 하지만 추가적인 복잡성을 도입하기 때문에 시스템의 특정 요구와 제약 조건에 따라 신중하게 적용해야 한다.</p>
  <p><strong>정리: CQRS는 읽기와 쓰기를 분리해 독립적 확장과 최적화를 가능하게 하는 패턴이다.</strong></p>

</div>
</details>


<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Event Sourcing(이벤트 소싱) </span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>Event Sourcing</b>은 시스템의 상태를 시간이 지남에 따라 발생한 <b>이벤트들의 연속</b>으로 표현하는 설계 패턴이다. 이벤트 소싱 기반 시스템에서는 상태 변화가 이벤트로 기록되어 <b>이벤트 저장소(Event Store)</b>에 보관된다. 시스템의 현재 상태는 이 이벤트들을 재생(replay)하여 도출된다.</p>
  <p>이벤트 소싱의 주요 장점 중 하나는 시스템에서 발생한 모든 변경 사항에 대한 <b>명확하고 감사(audit) 가능한 기록</b>을 제공한다는 점이다. 이는 디버깅이나 시스템 진화 과정을 추적하는 데 유용하다.</p>
  <p>이벤트 소싱은 종종 <b>CQRS나 도메인 주도 설계(DDD)</b> 같은 다른 패턴과 결합되어, 복잡한 비즈니스 로직을 가진 시스템을 <b>확장 가능하고 반응성 있는 구조</b>로 만드는 데 활용된다. 또한 <b>되돌리기/다시 실행(Undo/Redo)</b> 기능이 필요한 시스템이나 외부 시스템과의 통합이 필요한 경우에도 유용하다.</p>
  <p><strong>정리: 이벤트 소싱은 이벤트 기록으로 상태를 관리해 추적성과 복잡 도메인 대응을 가능하게 한다.</strong></p>
  <!-- 가로선 추가 -->
  <hr>
  <ul>
    <li><strong>이벤트 저장소 (Event Store):</strong> 이벤트 소싱 시스템에서 발생한 모든 이벤트를 순차적으로 기록·보관하는 저장소로, 상태는 이 이벤트들을 재생하여 계산된다.</li>
    <li><strong>UNDO (되돌리기):</strong> 직전에 수행한 작업이나 변경을 취소하여 이전 상태로 되돌리는 기능</li>
      <ul><li>예: 문서 편집기에서 "Ctrl+Z"</li></ul>
    <li><strong>REDO (다시 실행):</strong> UNDO로 되돌린 작업을 다시 재적용하여 앞으로 되돌리는 기능</li>
      <ul><li>예: "Ctrl+Y" 또는 "Ctrl+Shift+Z"</li></ul>
  </ul>

</div>
</details>
