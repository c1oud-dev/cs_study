---
layout: default
title: "Object Oriented Programming"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>Object Oriented Programming</h2>
  <p>
  객체 지향 프로그래밍(OOP)은 클래스의 인스턴스인 "객체"라는 개념에 기반한 프로그래밍 패러다임이다. OOP에서 클래스는 데이터(속성)와 동작(메서드)을 모두 갖는 객체를 생성하기 위한 청사진이다. OOP의 핵심 아이디어는 현실 세계의 객체와 그 상호작용을 모델링하는 것이며, 이를 통해 복잡하고 대규모 소프트웨어 시스템을 구축하는 데 적합하다.
  </p>
</section>

<!-- 설명 -->
<details open>
<summary><span class="accordion-title">Primary Principles(객체지향의 기본 원칙)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title" style="color: #000; font-weight: bold;">Inheritance(상속) </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      상속은 새로운 클래스가 기존 클래스의 속성과 메서드를 상속받을 수 있도록 한다. 상속받는 클래스를 부모 클래스 또는 슈퍼 클래스라고 하며, 상속받는 클래스를 자식 클래스 또는 하위 클래스라고 한다. 상속은 코드 재사용을 가능하게 하고 클래스의 계층적 구성을 가능하게 한다. 자식 클래스는 부모 클래스의 속성과 메서드를 상속받고, 잠재적으로 이를 추가하거나 재정의할 수 있다. 상속의 주요 장점은 코드를 재사용하고 클래스 간에 기능을 공유하는 깔끔하고 체계적인 방법을 제공한다는 것이다.
      </p>
      <p><strong>정리: 상속은 기존 클래스의 속성과 기능을 물려받아 재사용하고 확장하는 객체지향의 원칙이다.</strong></p>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title" style="color: #000; font-weight: bold;">Polymorphism(다형성) </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      다형성은 서로 다른 클래스의 객체를 공통 부모 클래스의 객체처럼 취급할 수 있도록 한다. 이는 다형적으로 처리해야 하는 모든 클래스에 공통 인터페이스를 정의함으로써 가능하다. 다형성이라는 단어는 그리스어에서 유래되었는데, "poly"는 '많음'을, "morph"는 '형태'를 의미한다.
      </p>
      <p>다형성에는 두 가지 유형이 있다.</p>
      <ul>
        <li>Compile-time 다형성(정적 다형성 또는 초기 바인딩이라고도 함)은 동작할 객체의 유형이 컴파일 타임에 결정될 때 발생한다. 이는 메서드 오버로딩을 통해 구현되는데, 메서드 오버로딩을 사용하면 동일한 클래스 내에서 여러 메서드가 이름은 같지만 매개변수는 서로 다를 수 있다.</li>
        <li>Run-time 다형성(동적 다형성 또는 지연 바인딩이라고도 함)은 객체의 유형이 런타임에 결정될 때 발생한다. 이는 메서드 오버라이딩을 통해 구현되는데, 이를 통해 자식 클래스는 부모 클래스에 이미 정의된 메서드의 특정 구현을 제공할 수 있다.</li>
      </ul>
      <p><strong>정리: 다형성은 동일한 인터페이스로 여러 객체가 각기 다른 방식으로 동작할 수 있는 성질이다.</strong></p>
      <hr><!-- 가로선 추가 -->
      <ul>
        <li><strong>메서드 오버로딩(Method Overloading):</strong> 같은 이름의 메서드를 매개변수(타입, 개수, 순서)를 다르게 정의하는 것 → 컴파일 시점(정적 바인딩)에서 결정</li>
        <li><strong>메서드 오버라이딩(Method Overriding):</strong> 상속받은 메서드를 자식 클래스에서 재정의하여 동작을 바꾸는 것 → 실행 시점(동적 바인딩)에서 결정</li>
      </ul>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title" style="color: #000; font-weight: bold;">Abstraction(추상화) </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      추상화는 객체의 구현 세부 사항을 숨기고 핵심 기능만 노출하는 과정을 의미한다. 추상화를 통해 객체의 내부 구조와 동작의 복잡성을 이해할 필요 없이 객체를 사용할 수 있다.
      </p>
      <p>
      추상화에는 두 가지 유형이 있다.
      </p>
      <ul>
        <li><strong>데이터 추상화:</strong> 데이터의 내부 표현을 숨기고 잘 정의된 인터페이스 세트를 통해 데이터에 대한 간소화된 뷰를 제공하는 것을 말한다.</li>
        <li><strong>동작 추상화:</strong> 객체의 내부 동작을 숨기고 잘 정의된 인터페이스 세트를 통해 해당 객체의 기능에 대한 단순화된 뷰를 제공하는 것을 말한다.</li>
      </ul>
      <p><strong>정리: 추상화는 불필요한 세부는 감추고 핵심적인 개념과 기능만을 드러내는 원칙이다.</strong></p>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title" style="color: #000; font-weight: bold;">Encapsulation(캡슐화) </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      캡슐화는 객체의 내부 데이터와 동작을 정의된 인터페이스로 감싸고 구현 세부 사항을 외부로부터 숨기는 방식을 의미한다. OOP의 기본 개념 중 하나이며, 데이터 은닉 및 정보 은닉 개념과 밀접한 관련이 있다.
      </p>
      <p>
      캡슐화는 접근 제한자(예: "public", "private", "protected")를 사용하여 객체의 데이터와 메서드의 가시성과 접근성을 제어함으로써 구현된다. 예를 들어, 클래스의 데이터 멤버는 private으로 선언될 수 있는데, 이는 클래스 내의 메서드에서만 접근할 수 있음을 의미한다. 반면 메서드는 public으로 선언될 수 있는데, 이는 객체를 참조하는 모든 코드에서 호출할 수 있음을 의미한다.
      </p>
      <p><strong>정리: 캡슐화는 데이터와 메서드를 하나로 묶고 외부로부터 직접 접근을 차단하여 보호하는 원칙이다.</strong></p>
    </div>
  </details>

</div>
</details>


<!-- 설명 -->
<details open>
<summary><span class="accordion-title">Paradigm Features(객체지향 패러다임의 특징)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title" style="color: #000; font-weight: bold;">Abstract Classes(추상 클래스) </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      추상 클래스는 OOP에서 인스턴스화할 수 없는 클래스이다. 대신, 다른 클래스가 상속할 수 있는 템플릿이나 설계도 역할을 한다. 추상 클래스는 추상 메서드와 추상이 아닌 메서드를 모두 포함할 수 있다. 추상 메서드는 구현이 없고 시그니처만 있는 메서드이다.
      </p>
      <p>
      추상 클래스는 관련 클래스 그룹에 대한 공통 인터페이스와 구현을 제공하는 데 사용된다. 또한 모든 하위 클래스에서 구현해야 하는 공통 동작을 정의하는 데에도 사용된다. 추상 클래스를 상속하는 하위 클래스를 Concrete Class(구체 클래스)라고 하며, 부모 클래스에 선언된 모든 추상 메서드에 대한 구현을 제공해야 한다.
      </p>
      <p><strong>정리: 추상 클래스는 공통 속성과 메서드를 정의하되 일부는 구현하지 않아 직접 인스턴스를 만들 수 없는 클래스이다.</strong></p>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title" style="color: #000; font-weight: bold;">Concrete Classes(구체 클래스) </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      구체 클래스는 OOP에서 인스턴스화 가능한 클래스로, 객체를 생성할 수 있다. 구체 클래스는 추상 클래스를 상속하는 경우, 부모 클래스에 선언된 모든 추상 메서드에 대한 구현을 제공하는 클래스이다. 또한, 추상 클래스를 상속하지 않는 클래스도 구체 클래스가 될 수 있으며, 이 경우 모든 메서드에 대한 구현을 가질 수 있다.
      </p>
      <p>
      구체적 클래스는 공통 추상 클래스를 상속하는 관련 클래스 그룹에 대한 구체적인 구현 세부 정보를 제공하는 데 사용된다. 또한 특정 클래스의 고유한 동작을 정의하는 데에도 사용된다. 구체적 클래스는 자체 메서드와 변수를 가질 수 있으며, 부모 클래스의 메서드를 재정의할 수도 있다.
      </p>
      <p><strong>정리: 구체 클래스는 모든 메서드가 구현되어 있어 직접 객체를 생성할 수 있는 클래스이다.</strong></p>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title" style="color: #000; font-weight: bold;">Scope Visibility(범위 가시성) </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      범위 가시성은 프로그램 내 변수, 함수 및 기타 요소의 접근성 또는 가시성을 정의하는 맥락에 따라 달라진다. OOP에서 범위 가시성은 "public", "private", "protected"와 같은 접근 제한자를 사용하여 제어된다.
      </p>
      <p>
      프로그래밍 언어에 따라 범위 가시성에 차이가 있지만, 가장 일반적인 범위 가시성은 다음과 같다.
      </p>
      <hr><!-- 가로선 추가 -->
      <ul>
        <li><strong>Public:</strong> 클래스 내부와 외부 모두 프로그램의 어디에서나 접근 가능하다.</li>
        <li><strong>Private:</strong> 해당 요소가 정의된 클래스 내에서만 접근 가능, 다른 클래스에서는 접근할 수 없으며, 해당 클래스를 상속하는 클래스도 마찬가지이다.</li>
        <li><strong>Protected:</strong> 해당 클래스와 하위 클래스 내에서만 액세스할 수 있다.</li>
      </ul>
      <p><strong>정리: 범위 가시성은 변수나 메서드에 접근할 수 있는 범위를 결정하는 규칙이다.</strong></p>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title" style="color: #000; font-weight: bold;">Interfaces(인터페이스) </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      OOP에서 인터페이스는 클래스가 구현해야 하는 계약 또는 메서드 집합이다. 인터페이스는 클래스가 제공해야 하는 공통 메서드 집합을 정의하지만, 구현 세부 사항은 제공하지 않다. 인터페이스는 메서드 시그니처와 상수를 모두 포함할 수 있다.
      </p>
      <p>
      인터페이스는 관련 클래스 그룹의 공통 동작을 정의하고, 서로 다른 클래스의 객체를 다형적으로 처리할 수 있는 방법을 제공하는 데 사용된다. 인터페이스를 구현하는 클래스는 인터페이스에 선언된 모든 메서드에 대한 구현을 제공해야 한다. 클래스는 여러 인터페이스를 구현할 수 있지만, 하나의 기본 클래스에서만 상속할 수 있다.
      </p>
      <p><strong>정리: 인터페이스는 구현 없이 메서드 규약만 정의하여 클래스들이 이를 구현하도록 강제하는 구조이다.</strong></p>
    </div>
  </details>

</div>
</details>

<!-- 설명 -->
<details open>
<summary><span class="accordion-title">Model Driven Design(모델 기반 설계)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  MDD는 시스템 설계를 일련의 모델로 표현하고, 이 모델을 사용하여 시스템 개발을 추진하는 소프트웨어 개발 방법론이다. MDD는 시스템 설계를 일련의 모델로 표현할 수 있으며, 이 모델을 사용하여 시스템 코드를 생성할 수 있다는 생각에 기반한다.
  </p>
  <p>
  MDD의 주요 장점은 시스템 설계와 구현 간의 관심사를 명확하게 분리할 수 있다는 것이다. 모델은 시스템 설계를 나타내고, 코드는 모델에서 생성되므로 시스템 유지 관리 및 개선이 용이해진다. 또한, MDD는 코드를 생성하기 전에 모델을 사용하여 설계 오류와 불일치를 확인할 수 있으므로 코드 품질도 향상시킬 수 있다.
  </p>

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title" style="color: #000; font-weight: bold;">Domain Models(도메인 모델)</span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      도메인 모델은 특정 지식이나 비즈니스 영역을 표현하는 것으로, 해당 도메인 내의 객체와 개념을 모델링하고 이들 간의 관계와 제약 조건을 파악하는 데 사용된다. OOP에서 도메인 모델은 일반적으로 클래스와 인터페이스의 집합으로 표현되며, 각 클래스 또는 인터페이스는 도메인 내의 특정 개념이나 객체를 나타낸다.
      </p>
      <p>
      도메인 모델은 문제 도메인을 명확하고 일관되게 표현하고 시스템의 비즈니스 요구 사항과 제약 조건을 파악하는 데 사용된다. 또한 시스템 설계를 안내하고 시스템이 해결하려는 실제 문제를 정확하게 반영하도록 보장하는 데에도 사용된다.
      </p>
      <p><strong>정리: 도메인 모델은 문제 영역의 개념과 규칙을 코드로 표현한 설계 모델이다.</strong></p>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title" style="color: #000; font-weight: bold;">Anemic Models(빈약한 모델)</span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      빈약한 모델은 빈혈 도메인 모델이라고도 하며, 도메인 객체가 데이터(속성)만 포함하고 동작은 없는 도메인 모델 유형이다. 빈약한 모델은 동작을 처리하기 위해 *데이터 전송 객체(DTO)와 *서비스 계층을 사용하는 경우가 많다.
      </p>
      <p>
      빈약한 모델은 캡슐화와 관심사 분리 원칙을 위반하기 때문에 OOP에서 *안티 패턴으로 간주된다. 빈약한 모델에서는 동작이 데이터와 분리되어 일반적으로 별도의 서비스 계층에서 구현되므로 복잡하고 긴밀하게 결합되어 유지 관리가 어려운 코드베이스가 될 수 있다.
      </p>
      <p><strong>정리: Anemic 모델은 데이터만 있고 도메인 로직이 거의 없는, 객체지향적이지 못한 모델이다.</strong></p>
      <hr><!-- 가로선 추가 -->
      <ul>
        <li><strong>데이터 전송 객체 (DTO, Data Transfer Object):</strong> 계층 간(특히 Controller ↔ Service ↔ Repository) 데이터 교환을 단순화하기 위해 사용하는 객체.</li>
        <ul>
          <li>로직 없이 순수히 데이터 전달만 담당 (getter/setter, 필드만 존재).</li>
        </ul>
        <li><strong>서비스 계층 (Service Layer):</strong> 비즈니스 로직을 담당하는 계층으로, Controller와 Repository 사이에서 동작.</li>
        <ul>
          <li>트랜잭션 관리, 도메인 규칙 실행, 재사용 가능한 비즈니스 기능을 제공.</li>
        </ul>
        <li><strong>안티 패턴 (Anti-Pattern):</strong> 자주 쓰이지만 실제로는 유지보수성, 성능, 확장성 등에 부정적인 영향을 주는 잘못된 설계 방식.</li>
        <ul>
          <li>God Object(모든 책임을 한 클래스가 가짐), Spaghetti Code(구조 없는 뒤엉킨 코드), Anemic Domain Model(빈약한 도메인 모델).</li>
        </ul>
      </ul>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title" style="color: #000; font-weight: bold;">Domain Language(도메인 언어) </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      도메인 언어는 특정 지식 영역이나 비즈니스를 설명하고 소통하는 데 사용되는 특정 어휘와 개념 집합이다. SW 개발에서 도메인 언어는 특정 도메인 내의 객체와 개념을 모델링하고, 이들 간의 관계와 제약 조건을 파악하는 데 사용된다.
      </p>
      <p>
      도메인 언어는 개발자, 비즈니스 분석가, 도메인 전문가를 포함한 모든 이해관계자가 문제 도메인에 대한 공통된 이해를 갖도록 하는 데 사용된다. 또한 SW 시스템이 해결하려는 실제 문제를 정확하게 반영하도록 보장하는 데에도 사용된다.
      </p>
      <p><strong>정리: 도메인 언어는 개발자와 도메인 전문가가 공유하는 문제 영역의 공통 언어이다.</strong></p>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title" style="color: #000; font-weight: bold;">Class Invariants(클래스 불변식) </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      클래스 불변식은 특정 시점에 클래스의 모든 객체에 대해 반드시 충족되어야 하는 조건들의 집합이다. OOP에서 클래스 불변식은 객체의 유효한 상태를 정의하고 객체가 항상 유효한 상태를 유지하도록 하는 데 사용된다.
      </p>
      <p>
      클래스 불변식은 일반적으로 클래스 생성자에서 정의되며, 객체의 상태를 검증하는 데 사용되는 private 메서드와 데이터 멤버를 통해 적용된다. 또한 객체의 상태를 변경할 수 있는 모든 연산 전후에 클래스 메서드에서 확인된다.
      </p>
      <p><strong>정리: 클래스 불변식은 객체가 항상 만족해야 하는 조건이나 규칙이다.</strong></p>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details class="nested-details">
    <summary><span class="accordion-title" style="color: #000; font-weight: bold;">Layered Architectures(계층형 아키텍처) </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      계층형 아키텍처는 시스템의 기능을 여러 계층으로 나누고, 각 계층이 특정 역할을 수행하며 위아래 계층과 상호 작용하는 소프트웨어 설계 패턴이다. 계층형 아키텍처의 핵심 아이디어는 시스템의 관심사를 서로 다르고 독립적인 계층으로 분리하여 코드를 더욱 모듈화하고, 이해, 테스트 및 수정을 용이하게 하는 것이다.
      </p>
      <p>
      계층적 아키텍처에는 여러 유형이 있지만, 가장 흔한 것은 다음으로 구성된 3계층 아키텍처이다.
      </p>
      <hr><!-- 가로선 추가 -->
      <ul>
        <li><strong>프레젠테이션 계층(Presentation Layer):</strong> 사용자와 직접 상호작용하는 계층으로, 화면(UI)이나 API 응답을 담당한다.</li>
        <li><strong>비즈니스 계층(Business Layer / Service Layer):</strong> 도메인 규칙과 비즈니스 로직을 처리하며, 프레젠테이션과 데이터 계층 사이의 중간 역할을 한다.</li>
        <li><strong>데이터 액세스 계층(Data Access Layer, DAL):</strong> DB와의 직접적인 입출력을 처리하며, 쿼리 실행과 영속성 관리를 담당한다.</li>
      </ul>
      <p><strong>정리: 계층형 아키텍처는 책임을 계층별로 나누어 유연성과 유지보수를 높이는 구조이다.</strong></p>
    </div>
  </details>

</div>
</details>
