---
layout: default
title: "Design Principles"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>Design Principles</h2>
  <p>
  Design Principles(설계 원칙)은 SW를 설계할 때 유지보수성과 확장성을 높이고, 복잡성을 줄이며, 협업을 용이하게 하기 위한 지침이다. 설계 원칙은 개발자가 코드 구조를 체계적이고 일관성 있게 만들도록 돕고, 장기적으로 변경에 강한 시스템을 구축하는 데 중점을 둔다. 대표적인 원칙으로는 객체 지향 프로그래밍에서 널리 사용되는 SOLID 원칙이 있으며, 이는 코드 재사용성, 유연성, 테스트 용이성을 극대화하기 위한 기반이 된다.
  </p>
</section>

<!-- 설명 -->
<details open>
<summary><span class="accordion-title">SOLID</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  SOLID는 객체 지향 소프트웨어 개발의 5대 원칙을 뜻하는 약어로, 2000년대 초 로버트 C. 마틴이 처음 제시했다. 이 원칙들은 다음과 같다.
  </p>

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title">Single Responsibility Principle (SRP) </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      단일 책임 원칙은 클래스는 하나의 책임만 가져야 한다는 원칙이다. 즉, 클래스는 변경되어야 할 이유가 오직 하나뿐이어야 하며, 여러 역할을 동시에 수행하지 않아야 한다. 이를 통해 응집도를 높이고, 유지보수성을 향상시킬 수 있다.
      </p>
      <p><strong>정리: 클래스는 오직 하나의 책임만 가져야 한다는 원칙</strong></p>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title">Open/Closed Principle (OCP) </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      개방-폐쇄 원칙은 소프트웨어 엔티티(클래스, 모듈, 함수 등)는 확장에는 열려 있어야 하지만 수정에는 닫혀 있어야 한다는 원칙이다. 즉, 기존 코드를 변경하지 않고도 새로운 기능을 추가할 수 있어야 한다. 이를 통해 안정성과 유연성을 동시에 확보할 수 있다.
      </p>
      <p><strong>정리: 코드는 확장에 열려 있고, 수정에는 닫혀 있어야 한다는 원칙</strong></p>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title">Liskov Substitution Principle (LSP) </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      리스코프 치환 원칙은 상위 타입의 객체를 하위 타입으로 치환해도 프로그램의 동작이 깨지지 않아야 한다는 원칙이다. 즉, 자식 클래스는 부모 클래스의 규약을 지켜야 하며, 일관된 행위를 보장해야 한다. 이를 통해 다형성(polymorphism)을 안전하게 구현할 수 있다.
      </p>
      <p><strong>정리: 부모 타입을 자식으로 바꿔도 동작에 문제가 없어야 한다는 원칙</strong></p>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title">Interface Segregation Principle (ISP) </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      인터페이스 분리 원칙은 클라이언트는 자신이 사용하지 않는 메서드에 의존하지 않아야 한다는 원칙이다. 즉, 하나의 거대한 인터페이스보다는 여러 개의 작은 인터페이스로 나누어 설계하는 것이 바람직하다. 이를 통해 불필요한 의존성을 줄이고, 유연한 설계를 할 수 있다.
      </p>
      <p><strong>정리: 쓰지 않는 기능에 의존하지 말고, 작은 인터페이스로 나눠야 하는 원칙</strong></p>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title">Dependency Inversion Principle (DIP) </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      의존성 역전 원칙은 고수준 모듈은 저수준 모듈에 의존하지 않고, 추상화에 의존해야 한다는 원칙이다. 즉, 구체적인 구현체가 아니라 인터페이스나 추상 클래스에 의존하도록 설계해야 한다. 이를 통해 코드의 결합도를 낮추고, 확장 가능성과 테스트 용이성을 높일 수 있다.
      </p>
      <p><strong>정리: 고수준은 저수준에 의존하지 말고, 구체가 아닌 추상에 의존해야 한다는 원칙</strong></p>
    </div>
  </details>

</div>
</details>


<!-- 설명 -->
<details>
<summary><span class="accordion-title">DRY(Don't Repeat Yourself)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  DRY(Don't Repeat Yourself) 는 코드에 중복된 기능이 존재하지 않아야 한다는 소프트웨어 개발 원칙이다. 이 원칙의 핵심은 중복과 반복을 제거하여 코드베이스를 가능한 한 단순하게 유지하는 것이다. 목표는 시스템 내에서 각 지식이 단일하고 모호하지 않은 방식으로만 표현되도록 보장하여, 복잡성을 줄이고 유지보수성을 향상하는 데 있다.
  </p>
  <p>
  DRY 원칙은 SOLID 원칙 중 단일 책임 원칙(SRP) 과 개방-폐쇄 원칙(OCP) 과 밀접한 관련이 있다. DRY는 시스템 전반에 재사용할 수 있는 추상화를 만들어서 중복 코드를 줄이는 것을 지향한다.
  </p>

</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title">YAGNI (You Ain't Gonna Need It)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  YAGNI(You Ain’t Gonna Need It) 은 즉시 필요하지 않은 기능은 코드베이스에 추가하지 말라는 소프트웨어 개발 원칙이다. 이 원칙의 핵심은 실제로 필요한 기능만 추가함으로써 불필요한 복잡성을 피하는 것이다.
  </p>
  <p>
  YAGNI 원칙은 SOLID 원칙 중 단일 책임 원칙(SRP) 과 개방-폐쇄 원칙(OCP) 과 밀접한 관련이 있다. YAGNI는 불필요한 추상화나 기능 생성을 피하고, 코드베이스를 가능한 한 단순하게 유지하는 것을 목표로 한다.
  </p>

</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Law of Demeter (디미터 법칙)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  디미터 법칙은 “낯선 객체와 이야기하지 말라(Only talk to your immediate friends)”는 원칙으로, 객체는 자신과 직접적으로 연관된 객체에게만 메시지를 보내야 한다는 제약을 둔다. 이를 통해 객체 간 결합도를 줄이고 캡슐화를 강화하여 코드 변경 시 영향을 최소화한다.
  </p>

</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Tell, Don’t Ask 원칙</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  Tell, Don’t Ask 원칙은 객체의 내부 상태를 꺼내와서 외부에서 처리하지 말고, 객체에게 스스로 무엇을 하라고 요청하라는 설계 원칙이다. 이를 통해 객체는 스스로의 책임을 다하며, 응집도를 높이고 캡슐화를 지키는 객체 지향적 설계를 가능하게 한다.
  </p>

</div>
</details>


<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Hollywood Principle</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  Hollywood Principle(할리우드 원칙) 은 소프트웨어 개발 원칙으로, "우리를 호출하지 마세요. 우리가 당신을 호출하겠습니다(Don't call us, we'll call you)" 라고 요약된다. 이 원칙은 애플리케이션에서 저수준(low-level) 컴포넌트가 아니라 고수준(high-level) 컴포넌트가 제어 흐름을 지시해야 한다는 것을 의미한다.
  </p>
  <p>
  이 원칙은 종종 제어의 역전(Inversion of Control, IoC) 과 의존성 주입(Dependency Injection) 의 맥락에서 사용된다. 전통적인 소프트웨어 개발에서는 저수준 컴포넌트가 자신이 의존하는 고수준 컴포넌트를 직접 생성하고 관리한다. 하지만 IoC에서는 반대로, 고수준 컴포넌트가 제어 흐름을 주도하고, 저수준 컴포넌트는 별도의 메커니즘에 의해 생성되고 관리된다.
  </p>

</div>
</details>
