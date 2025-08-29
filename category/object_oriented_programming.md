---
layout: default
title: "객체지향 프로그래밍 완전 정리"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>객체지향 프로그래밍 완전 정리 - 면접부터 개념까지</h2>
</section>

<!-- 면접 예상 질문 및 답변 -->
<details open>
  <summary><span class="accordion-title">면접 예상 질문 및 답변</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

<details>
  <summary style="font-size:1rem;"><b>Q1: 객체지향 프로그래밍이란 무엇인지 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 객체지향 프로그래밍(OOP)은 현실 세계의 사물을 객체로 모델링하여 프로그램을 작성하는 패러다임입니다.
데이터(속성)와 그 데이터를 처리하는 함수(메서드)를 하나의 객체로 묶어서 관리합니다. 캡슐화, 상속, 다형성, 추상화라는 4대 특징을 통해 코드의 재사용성, 유지보수성, 확장성을 향상시킵니다. 클래스라는 설계도를 통해 객체를 생성하며, 객체 간의 상호작용으로 프로그램이 동작합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q2: 클래스와 객체의 차이점을 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 클래스는 객체를 생성하기 위한 설계도나 템플릿으로, 속성과 메서드를 정의한 것입니다. 객체는 클래스를 기반으로 실제 메모리에 생성된 인스턴스입니다. 클래스는 논리적인 개념이고 객체는 물리적인 실체라고 할 수 있습니다. 예를 들어, 'Car'라는 클래스가 있다면 'myCar', 'yourCar'는 Car 클래스로부터 생성된 각각의 객체입니다. 하나의 클래스로부터 여러 개의 객체를 생성할 수 있습니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q3: 캡슐화에 대해 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 캡슐화는 관련된 데이터와 메서드를 하나의 단위로 묶고, 외부에서의 직접적인 접근을 제한하는 것입니다. 접근 제어자(public, private, protected)를 사용해 정보 은닉을 구현합니다. 이를 통해 객체 내부의 구현 세부사항을 숨기고, 외부에서는 정해진 인터페이스를 통해서만 객체와 상호작용할 수 있도록 합니다. 캡슐화의 장점은 데이터 보안성 향상, 모듈성 증가, 유지보수 용이성, 코드의 재사용성 향상입니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q4: 상속의 개념과 장단점을 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 상속은 기존 클래스의 속성과 메서드를 새로운 클래스에서 재사용할 수 있게 하는 메커니즘입니다. 부모 클래스의 특성을 자식 클래스가 물려받아 코드 중복을 줄이고 계층적 구조를 만들 수 있습니다. 장점으로는 코드 재사용성, 유지보수성 향상, 계층적 분류가 있습니다. 단점으로는 부모-자식 클래스 간 강한 결합도, 상속 구조의 복잡성 증가, 다중 상속 시 발생할 수 있는 모호성 문제가 있습니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q5: 다형성에 대해 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 다형성은 같은 인터페이스나 메서드 호출이 객체의 타입에 따라 다르게 동작하는 것을 의미합니다. 오버라이딩과 오버로딩으로 구현할 수 있습니다. 런타임에 실제 객체 타입에 따라 적절한 메서드가 호출되는 동적 바인딩을 통해 구현됩니다. 다형성을 통해 코드의 유연성과 확장성을 높일 수 있으며, 새로운 클래스 추가 시 기존 코드 수정 없이 확장이 가능합니다. 인터페이스나 추상 클래스와 함께 사용하면 더욱 강력한 설계가 가능합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q6: 추상화에 대해 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 추상화는 복잡한 시스템에서 핵심적인 개념이나 기능에 집중하기 위해 불필요한 세부사항을 숨기는 것입니다. 추상 클래스와 인터페이스를 통해 구현할 수 있습니다. 공통된 특성을 추출하여 상위 레벨에서 정의하고, 구체적인 구현은 하위 클래스에서 담당합니다. 이를 통해 복잡성 감소, 코드의 이해도 향상, 설계의 일관성 유지, 변경에 대한 유연성 확보가 가능합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q7: 오버라이딩과 오버로딩의 차이점을 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 오버라이딩은 부모 클래스의 메서드를 자식 클래스에서 재정의하는 것으로, 같은 시그니처(메서드명, 매개변수)를 가져야 합니다. 런타임에 실제 객체 타입에 따라 호출될 메서드가 결정됩니다. 오버로딩은 같은 클래스 내에서 메서드명은 같지만 매개변수가 다른 여러 메서드를 정의하는 것입니다. 컴파일 타임에 매개변수 타입과 개수에 따라 호출될 메서드가 결정됩니다. 오버라이딩은 다형성 구현의 핵심이고, 오버로딩은 메서드 이름의 일관성을 위해 사용됩니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q8: 인터페이스와 추상 클래스의 차이점을 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 인터페이스는 구현되지 않은 메서드들의 집합으로, 다중 구현이 가능하며 상수와 추상 메서드만 가질 수 있습니다. 추상 클래스는 하나 이상의 추상 메서드를 포함하는 클래스로, 단일 상속만 가능하며 일반 메서드와 멤버 변수도 가질 수 있습니다. 인터페이스는 '할 수 있는 것'을 정의하고, 추상 클래스는 '무엇인가'를 정의합니다. 공통 기능의 부분적 구현이 필요하면 추상 클래스를, 단순한 규약 정의면 인터페이스를 사용하는 것이 좋습니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q9: 접근 제어자의 종류와 역할을 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> public은 어디서든 접근 가능하며 외부 인터페이스를 정의할 때 사용합니다. private은 같은 클래스 내에서만 접근 가능하며 내부 구현을 숨길 때 사용합니다. protected는 같은 패키지나 상속받은 클래스에서 접근 가능하며 상속 관계에서 사용합니다. default(package-private)는 같은 패키지 내에서만 접근 가능합니다. 접근 제어자를 통해 캡슐화를 구현하고 정보 은닉을 달성할 수 있습니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q10: 생성자와 소멸자의 역할을 설명해주세요.</b></summary>
  <div class="accordion-content>
    <p><b>A:</b> 생성자는 객체가 생성될 때 자동으로 호출되는 특수한 메서드로, 객체의 초기화를 담당합니다. 클래스명과 동일하며 반환 타입이 없습니다. 매개변수에 따라 여러 개의 생성자를 만들 수 있고, 기본 생성자가 자동으로 제공됩니다. 소멸자는 객체가 메모리에서 제거될 때 호출되어 리소스 해제나 정리 작업을 담당합니다. Java는 가비지 컬렉터가 있어 소멸자가 필요하지 않지만, C++에서는 명시적 소멸자가 중요합니다.</p>
  </div>
</details>

  </div>
</details>

<!-- 추가 면접 예상 질문 및 답변 -->
<details>
  <summary><span class="accordion-title">추가 면접 예상 질문 및 답변</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

<p>설계 원칙 관련</p>

<details>
  <summary style="font-size:1rem;"><b>Q11: SOLID 원칙에 대해 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> SOLID는 객체지향 설계의 5가지 원칙입니다. S(Single Responsibility): 클래스는 하나의 책임만 가져야 합니다. O(Open/Closed): 확장에는 열려있고 수정에는 닫혀있어야 합니다. L(Liskov Substitution): 하위 타입은 상위 타입을 대체할 수 있어야 합니다. I(Interface Segregation): 클라이언트는 사용하지 않는 인터페이스에 의존하면 안됩니다. D(Dependency Inversion): 추상화에 의존해야 하며 구체화에 의존하면 안됩니다. 이 원칙들을 따르면 유지보수가 쉽고 확장 가능한 코드를 작성할 수 있습니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q12: 결합도와 응집도에 대해 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 결합도는 모듈 간의 의존성 정도를 나타내며, 낮을수록 좋습니다. 높은 결합도는 한 모듈의 변경이 다른 모듈에 영향을 미쳐 유지보수를 어렵게 합니다. 응집도는 모듈 내 요소들이 하나의 목적을 위해 얼마나 밀접하게 연관되어 있는지를 나타내며, 높을수록 좋습니다. 높은 응집도는 모듈의 책임이 명확하고 이해하기 쉽게 만듭니다. 좋은 설계는 낮은 결합도와 높은 응집도를 가집니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q13: 의존성 주입(Dependency Injection)이란 무엇인가요?</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 의존성 주입은 객체가 직접 의존 객체를 생성하는 대신 외부에서 주입받는 설계 패턴입니다. 생성자 주입, 메서드 주입, 필드 주입 방식이 있습니다. 이를 통해 객체 간 결합도를 낮추고, 테스트 용이성을 높이며, 코드의 유연성과 재사용성을 향상시킵니다. Spring Framework에서 IoC 컨테이너를 통해 구현되며, Mock 객체를 쉽게 주입할 수 있어 단위 테스트가 용이해집니다.</p>
  </div>
</details>

<p>디자인 패턴 관련</p>

<details>
  <summary style="font-size:1rem;"><b>Q14: 싱글톤 패턴에 대해 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 싱글톤 패턴은 클래스의 인스턴스가 오직 하나만 생성되도록 보장하는 패턴입니다. 전역적으로 접근 가능한 인스턴스를 제공하며, 생성자를 private으로 만들고 static 메서드를 통해 인스턴스에 접근합니다. 데이터베이스 연결, 로거, 설정 정보 등에 사용되지만, 전역 상태를 만들어 테스트를 어렵게 하고 결합도를 높일 수 있습니다. 멀티스레드 환경에서는 동기화 처리가 필요합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q15: 팩토리 패턴에 대해 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 팩토리 패턴은 객체 생성을 담당하는 별도의 클래스나 메서드를 만들어 객체 생성 로직을 캡슐화하는 패턴입니다. 단순 팩토리, 팩토리 메서드, 추상 팩토리 패턴이 있습니다. 클라이언트는 구체적인 클래스를 알 필요 없이 팩토리를 통해 객체를 생성할 수 있습니다. 객체 생성 코드의 중복을 제거하고, 생성 로직 변경 시 한 곳만 수정하면 되는 장점이 있습니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q16: 옵저버 패턴에 대해 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 옵저버 패턴은 한 객체의 상태 변화에 따라 다른 객체들이 자동으로 알림을 받고 업데이트되는 패턴입니다. Subject(주체)와 Observer(관찰자)로 구성되며, Subject는 Observer들의 목록을 관리하고 상태 변화 시 모든 Observer에게 알립니다. GUI 이벤트 처리, MVC 패턴, 발행-구독 시스템에 사용됩니다. 느슨한 결합을 유지하면서 일대다 의존관계를 관리할 수 있습니다.</p>
  </div>
</details>

<p>실무 관련</p>

<details>
  <summary style="font-size:1rem;"><b>Q17: 객체지향과 절차지향 프로그래밍의 차이점을 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 절차지향은 함수 중심으로 순차적 실행에 초점을 맞춘 패러다임이고, 객체지향은 객체 중심으로 객체 간 상호작용에 초점을 맞춘 패러다임입니다. 절차지향은 구현이 빠르고 간단한 문제에 적합하지만, 코드 재사용성과 유지보수성이 떨어집니다. 객체지향은 복잡한 시스템에 적합하고 코드 재사용성이 높지만, 설계 복잡도가 높고 실행 속도가 상대적으로 느립니다. 현대 소프트웨어에서는 대부분 객체지향 패러다임을 사용합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q18: 클래스 다이어그램을 설명할 수 있나요?</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 클래스 다이어그램은 UML의 한 종류로, 시스템의 클래스들과 그들 간의 관계를 시각적으로 표현합니다. 클래스는 세 부분(클래스명, 속성, 메서드)으로 구성되고, 관계는 연관, 집합, 구성, 일반화(상속), 의존, 실현으로 나타냅니다. +는 public, -는 private, #은 protected를 의미합니다. 시스템 설계 시 구조를 명확히 하고 개발팀 간 의사소통을 원활하게 하는 데 사용됩니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q19: 객체지향 프로그래밍의 단점이 있나요?</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 객체지향의 주요 단점으로는 설계 복잡도 증가, 학습 곡선이 높음, 실행 속도 오버헤드, 메모리 사용량 증가가 있습니다. 과도한 추상화로 인한 이해도 저하, 잘못된 상속 설계 시 유지보수 어려움, 객체 간 의존관계 복잡성도 문제가 될 수 있습니다. 간단한 프로그램에서는 오히려 복잡도만 증가시킬 수 있어, 프로젝트 특성에 따른 적절한 패러다임 선택이 중요합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q20: 리팩토링에서 객체지향 원칙을 어떻게 적용하나요?</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 리팩토링 시 단일 책임 원칙에 따라 큰 클래스를 작은 클래스로 분할하고, 중복 코드를 상위 클래스로 추출하여 상속을 활용합니다. 긴 매개변수 목록을 객체로 치환하고, 조건문을 다형성으로 대체합니다. 데이터와 메서드를 함께 이동시켜 캡슐화를 강화하고, 인터페이스를 도입하여 추상화 수준을 높입니다. 이러한 원칙들을 적용하면 더 유지보수하기 쉽고 확장 가능한 코드로 개선할 수 있습니다.</p>
  </div>
</details>

  </div>
</details>

<!-- 개념 정리: 전체를 HTML로 상세 변환 -->
<details>
  <summary><span class="accordion-title">객체지향 프로그래밍 개념 정리 (전체)</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <h2>1. 객체지향 프로그래밍 개요</h2>

  <h3>1.1 객체지향 프로그래밍이란?</h3>
  <p>객체지향 프로그래밍(Object-Oriented Programming, OOP)은 현실 세계의 사물을 프로그래밍에서 객체로 모델링하여 개발하는 방법론입니다. 데이터와 그 데이터를 처리하는 함수를 하나의 객체로 묶어서 관리합니다.</p>

  <h3>1.2 객체지향 프로그래밍의 등장 배경</h3>
  <ul>
    <li>소프트웨어 복잡도 증가</li>
    <li>코드 재사용성 필요</li>
    <li>유지보수의 어려움</li>
    <li>모듈화의 필요성</li>
    <li>현실 세계 모델링의 자연스러움</li>
  </ul>

  <h3>1.3 객체지향 vs 절차지향</h3>
  <h4>절차지향 프로그래밍</h4>
  <ul>
    <li>함수 중심의 프로그래밍</li>
    <li>순차적 실행</li>
    <li>데이터와 함수의 분리</li>
    <li>간단하고 직관적</li>
    <li>작은 프로그램에 적합</li>
  </ul>

  <h4>객체지향 프로그래밍</h4>
  <ul>
    <li>객체 중심의 프로그래밍</li>
    <li>객체 간 상호작용</li>
    <li>데이터와 함수의 결합</li>
    <li>복잡하지만 확장성 높음</li>
    <li>큰 프로그램에 적합</li>
  </ul>

  <h2>2. 기본 개념</h2>

  <h3>2.1 클래스 (Class)</h3>
  <p>객체를 생성하기 위한 설계도 또는 틀입니다.</p>
  <h4>클래스 구성 요소</h4>
  <ul>
    <li>속성 (Attribute/Field): 객체의 상태를 나타내는 데이터</li>
    <li>메서드 (Method): 객체의 행동을 나타내는 함수</li>
    <li>생성자 (Constructor): 객체 생성 시 초기화를 담당</li>
    <li>소멸자 (Destructor): 객체 소멸 시 정리 작업을 담당</li>
  </ul>

  <h3>2.2 객체 (Object)</h3>
  <p>클래스를 기반으로 생성된 실체입니다. 인스턴스(Instance)라고도 합니다.</p>
  <h4>객체의 특징</h4>
  <ul>
    <li>고유한 식별자를 가짐</li>
    <li>상태와 행동을 가짐</li>
    <li>다른 객체와 메시지를 주고받음</li>
    <li>생명주기를 가짐</li>
  </ul>

  <h3>2.3 메시지 (Message)</h3>
  <p>객체 간의 상호작용 방식으로, 한 객체가 다른 객체의 메서드를 호출하는 것입니다.</p>

  <h2>3. 객체지향 4대 특징</h2>

  <h3>3.1 캡슐화 (Encapsulation)</h3>
  <h4>개념</h4>
  <p>관련된 데이터와 메서드를 하나의 클래스로 묶고, 외부에서의 접근을 제한하는 것입니다.</p>
  <h4>정보 은닉 (Information Hiding)</h4>
  <p>객체 내부의 구현 세부사항을 외부에서 볼 수 없도록 숨기는 것입니다.</p>
  <h4>접근 제어자</h4>
  <ul>
    <li>public: 어디서든 접근 가능</li>
    <li>protected: 같은 패키지나 상속받은 클래스에서 접근 가능</li>
    <li>default (package-private): 같은 패키지 내에서만 접근 가능</li>
    <li>private: 같은 클래스 내에서만 접근 가능</li>
  </ul>
  <h4>캡슐화의 장점</h4>
  <ul>
    <li>데이터 보안성 향상</li>
    <li>모듈의 독립성 증가</li>
    <li>인터페이스 단순화</li>
    <li>유지보수 용이성</li>
  </ul>
  <h4>Getter와 Setter</h4>
  <p>private 멤버에 안전하게 접근하기 위한 메서드입니다.</p>

  <h3>3.2 상속 (Inheritance)</h3>
  <h4>개념</h4>
  <p>기존 클래스의 속성과 메서드를 새로운 클래스가 물려받아 재사용하는 것입니다.</p>
  <h4>상속 관계</h4>
  <ul>
    <li>부모 클래스 (Parent Class): 상위 클래스, 슈퍼 클래스</li>
    <li>자식 클래스 (Child Class): 하위 클래스, 서브 클래스</li>
  </ul>
  <h4>상속의 종류</h4>
  <ul>
    <li>단일 상속: 하나의 부모 클래스만 상속</li>
    <li>다중 상속: 여러 부모 클래스를 상속 (Java는 지원하지 않음)</li>
    <li>다단계 상속: 상속의 상속</li>
    <li>계층적 상속: 여러 자식이 하나의 부모를 상속</li>
  </ul>
  <h4>상속의 장점</h4>
  <ul>
    <li>코드 재사용성 향상</li>
    <li>중복 코드 제거</li>
    <li>계층적 분류 가능</li>
    <li>유지보수 효율성</li>
  </ul>
  <h4>상속의 단점</h4>
  <ul>
    <li>부모-자식 클래스 간 강한 결합</li>
    <li>상속 구조 복잡성</li>
    <li>잘못된 상속 시 문제 발생</li>
  </ul>

  <h3>3.3 다형성 (Polymorphism)</h3>
  <h4>개념</h4>
  <p>같은 인터페이스나 메서드 호출이 객체에 따라 다르게 동작하는 것입니다.</p>
  <h4>다형성의 종류</h4>
  <ul>
    <li>컴파일 타임 다형성: 오버로딩, 템플릿</li>
    <li>런타임 다형성: 오버라이딩, 동적 바인딩</li>
  </ul>
  <h4>메서드 오버라이딩 (Method Overriding)</h4>
  <p>부모 클래스의 메서드를 자식 클래스에서 재정의하는 것입니다.</p>
  <ul>
    <li>메서드 시그니처가 동일해야 함</li>
    <li>접근 제어자는 부모보다 넓거나 같아야 함</li>
    <li>예외는 부모보다 좁은 범위여야 함</li>
  </ul>
  <h4>메서드 오버로딩 (Method Overloading)</h4>
  <p>같은 클래스 내에서 같은 이름의 메서드를 여러 개 정의하는 것입니다.</p>
  <ul>
    <li>메서드명은 동일</li>
    <li>매개변수 타입, 개수, 순서가 달라야 함</li>
    <li>반환 타입은 관계없음</li>
  </ul>
  <h4>동적 바인딩 (Dynamic Binding)</h4>
  <p>런타임에 실제 객체 타입에 따라 호출될 메서드가 결정되는 것입니다.</p>

  <h3>3.4 추상화 (Abstraction)</h3>
  <h4>개념</h4>
  <p>복잡한 시스템에서 핵심적인 개념이나 기능에 집중하기 위해 불필요한 세부사항을 숨기는 것입니다.</p>
  <h4>추상 클래스 (Abstract Class)</h4>
  <p>하나 이상의 추상 메서드를 포함하는 클래스입니다.</p>
  <ul>
    <li>인스턴스 생성 불가</li>
    <li>상속을 통해서만 사용</li>
    <li>일반 메서드도 포함 가능</li>
    <li>생성자 가질 수 있음</li>
  </ul>
  <h4>인터페이스 (Interface)</h4>
  <p>구현되지 않은 메서드들의 집합입니다.</p>
  <ul>
    <li>모든 메서드가 추상 메서드 (Java 8부터 default, static 메서드 허용)</li>
    <li>상수만 가질 수 있음</li>
    <li>다중 구현 가능</li>
    <li>인스턴스 생성 불가</li>
  </ul>
  <h4>추상 클래스 vs 인터페이스</h4>
  <table>
    <thead><tr><th>구분</th><th>추상 클래스</th><th>인터페이스</th></tr></thead>
    <tbody>
      <tr><td>다중 상속</td><td>불가능</td><td>가능</td></tr>
      <tr><td>메서드 구현</td><td>가능</td><td>불가능 (Java 8부터 일부 가능)</td></tr>
      <tr><td>변수</td><td>일반 변수 가능</td><td>상수만 가능</td></tr>
      <tr><td>접근 제어자</td><td>모든 종류 가능</td><td>public만 가능</td></tr>
      <tr><td>목적</td><td>is-a 관계</td><td>can-do 관계</td></tr>
    </tbody>
  </table>

  <h2>4. 생성자와 소멸자</h2>

  <h3>4.1 생성자 (Constructor)</h3>
  <h4>개념</h4>
  <p>객체가 생성될 때 자동으로 호출되는 특수한 메서드입니다.</p>
  <h4>생성자 특징</h4>
  <ul>
    <li>클래스명과 동일한 이름</li>
    <li>반환 타입 없음</li>
    <li>오버로딩 가능</li>
    <li>상속되지 않음</li>
  </ul>
  <h4>생성자 종류</h4>
  <ul>
    <li>기본 생성자 (Default Constructor): 매개변수가 없는 생성자</li>
    <li>매개변수 생성자 (Parameterized Constructor): 매개변수를 받는 생성자</li>
    <li>복사 생성자 (Copy Constructor): 다른 객체를 복사해서 생성</li>
  </ul>
  <h4>생성자 체이닝 (Constructor Chaining)</h4>
  <p>한 생성자에서 다른 생성자를 호출하는 것입니다.</p>

  <h3>4.2 소멸자 (Destructor)</h3>
  <p>객체가 메모리에서 해제될 때 호출되는 메서드입니다. (Java에서는 finalize 메서드, C++에서는 ~클래스명)</p>

  <h2>5. SOLID 원칙</h2>
  <h3>5.1 SRP (Single Responsibility Principle)</h3>
  <p>단일 책임 원칙: 클래스는 하나의 책임만 가져야 합니다.</p>
  <h3>5.2 OCP (Open/Closed Principle)</h3>
  <p>개방-폐쇄 원칙: 확장에는 열려있고, 수정에는 닫혀있어야 합니다.</p>
  <h3>5.3 LSP (Liskov Substitution Principle)</h3>
  <p>리스코프 치환 원칙: 하위 타입은 언제나 상위 타입을 대체할 수 있어야 합니다.</p>
  <h3>5.4 ISP (Interface Segregation Principle)</h3>
  <p>인터페이스 분리 원칙: 클라이언트는 자신이 사용하지 않는 메서드에 의존관계를 맺으면 안됩니다.</p>
  <h3>5.5 DIP (Dependency Inversion Principle)</h3>
  <p>의존관계 역전 원칙: 추상화에 의존해야 하며, 구체화에 의존하면 안됩니다.</p>

  <h2>6. 주요 디자인 패턴</h2>

  <h3>6.1 생성 패턴</h3>
  <h4>싱글톤 패턴 (Singleton Pattern)</h4>
  <p>클래스의 인스턴스가 오직 하나만 생성되도록 보장하는 패턴입니다.</p>
  <h5>구현 방법</h5>
  <ul>
    <li>Eager Initialization: 클래스 로딩 시 인스턴스 생성</li>
    <li>Lazy Initialization: 처음 사용할 때 인스턴스 생성</li>
    <li>Thread-Safe: 멀티스레드 환경에서 안전한 구현</li>
    <li>Enum 사용: Java에서 권장되는 방법</li>
  </ul>
  <h5>장점</h5>
  <ul>
    <li>메모리 절약</li>
    <li>전역 접근점 제공</li>
    <li>초기화 제어</li>
  </ul>
  <h5>단점</h5>
  <ul>
    <li>전역 상태로 인한 결합도 증가</li>
    <li>테스트 어려움</li>
    <li>멀티스레드 환경에서 주의 필요</li>
  </ul>

  <h4>팩토리 패턴 (Factory Pattern)</h4>
  <p>객체 생성을 담당하는 별도의 클래스나 메서드를 만드는 패턴입니다.</p>
  <h5>종류</h5>
  <ul>
    <li>Simple Factory: 단순한 팩토리 클래스</li>
    <li>Factory Method: 추상 팩토리 메서드</li>
    <li>Abstract Factory: 관련 객체들의 패밀리를 생성</li>
  </ul>
  <h5>장점</h5>
  <ul>
    <li>객체 생성 로직 캡슐화</li>
    <li>코드 재사용성 향상</li>
    <li>유연성 증가</li>
  </ul>

  <h4>빌더 패턴 (Builder Pattern)</h4>
  <p>복잡한 객체를 단계적으로 생성하는 패턴입니다.</p>
  <ul>
    <li>생성 과정과 표현 방법 분리</li>
    <li>체이닝 방식으로 가독성 향상</li>
    <li>불변 객체 생성에 유용</li>
  </ul>

  <h3>6.2 구조 패턴</h3>
  <h4>어댑터 패턴 (Adapter Pattern)</h4>
  <p>서로 호환되지 않는 인터페이스를 가진 클래스들이 함께 작동할 수 있도록 하는 패턴입니다.</p>
  <h5>구현 방식</h5>
  <ul>
    <li>Object Adapter: 구성을 사용</li>
    <li>Class Adapter: 상속을 사용</li>
  </ul>

  <h4>데코레이터 패턴 (Decorator Pattern)</h4>
  <p>기존 객체에 새로운 기능을 동적으로 추가하는 패턴입니다.</p>
  <ul>
    <li>상속의 대안</li>
    <li>런타임에 기능 추가/제거</li>
    <li>단일 책임 원칙 준수</li>
  </ul>

  <h4>퍼사드 패턴 (Facade Pattern)</h4>
  <p>복잡한 서브시스템에 대한 단순한 인터페이스를 제공하는 패턴입니다.</p>
  <h5>장점</h5>
  <ul>
    <li>클라이언트와 서브시스템 간의 결합도 감소</li>
    <li>사용 편의성 증가</li>
    <li>복잡성 숨김</li>
  </ul>

  <h3>6.3 행위 패턴</h3>

  <h4>옵저버 패턴 (Observer Pattern)</h4>
  <p>한 객체의 상태 변화에 따라 다른 객체들이 자동으로 알림을 받는 패턴입니다.</p>
  <h5>구성 요소</h5>
  <ul>
    <li>Subject: 관찰 대상</li>
    <li>Observer: 관찰자</li>
    <li>ConcreteSubject: 구체적인 관찰 대상</li>
    <li>ConcreteObserver: 구체적인 관찰자</li>
  </ul>
  <h5>장점</h5>
  <ul>
    <li>느슨한 결합</li>
    <li>동적인 관계 형성</li>
    <li>일대다 의존관계 지원</li>
  </ul>

  <h4>전략 패턴 (Strategy Pattern)</h4>
  <p>알고리즘을 캡슐화하고 상호 교환 가능하게 만드는 패턴입니다.</p>
  <h5>구성 요소</h5>
  <ul>
    <li>Strategy: 전략 인터페이스</li>
    <li>ConcreteStrategy: 구체적인 전략</li>
    <li>Context: 전략을 사용하는 컨텍스트</li>
  </ul>
  <h5>장점</h5>
  <ul>
    <li>알고리즘 변경 용이</li>
    <li>조건문 제거</li>
    <li>확장성 증가</li>
  </ul>

  <h4>템플릿 메서드 패턴 (Template Method Pattern)</h4>
  <p>알고리즘의 구조를 정의하고, 일부 단계를 하위 클래스에서 구현하도록 하는 패턴입니다.</p>
  <ul>
    <li>상속 기반</li>
    <li>알고리즘 골격 정의</li>
    <li>공통 코드 재사용</li>
  </ul>

  <h4>커맨드 패턴 (Command Pattern)</h4>
  <p>요청을 객체의 형태로 캡슐화하는 패턴입니다.</p>
  <h5>장점</h5>
  <ul>
    <li>요청과 실행의 분리</li>
    <li>요청 저장/로깅 가능</li>
    <li>되돌리기 기능 구현 용이</li>
  </ul>

  <h2>7. 관계와 의존성</h2>

  <h3>7.1 클래스 간 관계</h3>
  <h4>연관 (Association)</h4>
  <p>두 클래스 간의 일반적인 관계를 나타냅니다.</p>
  <h5>종류</h5>
  <ul>
    <li>단방향 연관</li>
    <li>양방향 연관</li>
    <li>일대일 연관</li>
    <li>일대다 연관</li>
    <li>다대다 연관</li>
  </ul>

  <h4>집합 (Aggregation)</h4>
  <p>전체와 부분의 관계이지만, 부분이 전체에 속하지 않아도 독립적으로 존재할 수 있는 관계입니다.</p>
  <ul>
    <li>"has-a" 관계</li>
    <li>약한 소유 관계</li>
    <li>부분 객체가 독립적으로 존재 가능</li>
  </ul>

  <h4>구성/합성 (Composition)</h4>
  <p>전체와 부분의 관계이며, 부분이 전체에 완전히 종속되는 관계입니다.</p>
  <ul>
    <li>강한 소유 관계</li>
    <li>전체가 소멸되면 부분도 소멸</li>
    <li>생명주기 공유</li>
  </ul>

  <h4>일반화 (Generalization)</h4>
  <p>상속 관계를 나타냅니다.</p>
  <ul>
    <li>"is-a" 관계</li>
    <li>자식이 부모의 특수화</li>
    <li>부모가 자식의 일반화</li>
  </ul>

  <h4>의존 (Dependency)</h4>
  <p>한 클래스가 다른 클래스를 사용하는 관계입니다.</p>
  <h5>종류</h5>
  <ul>
    <li>매개변수 의존</li>
    <li>지역변수 의존</li>
    <li>메서드 호출 의존</li>
  </ul>

  <h4>실현 (Realization)</h4>
  <p>인터페이스와 구현 클래스 간의 관계입니다.</p>

  <h3>7.2 결합도 (Coupling)</h3>
  <p>모듈 간의 의존성 정도를 나타냅니다.</p>
  <h4>결합도 종류 (높음 → 낮음)</h4>
  <ul>
    <li>내용 결합도: 다른 모듈의 내부를 직접 수정</li>
    <li>공통 결합도: 전역 데이터 공유</li>
    <li>외부 결합도: 외부에서 도입된 데이터 형식 공유</li>
    <li>제어 결합도: 제어 신호 전달</li>
    <li>스탬프 결합도: 데이터 구조 전달</li>
    <li>자료 결합도: 단순한 데이터만 전달</li>
  </ul>

  <h3>7.3 응집도 (Cohesion)</h3>
  <p>모듈 내부 요소들 간의 연관성 정도를 나타냅니다.</p>
  <h4>응집도 종류 (낮음 → 높음)</h4>
  <ul>
    <li>우연적 응집도: 관련 없는 요소들이 모여 있음</li>
    <li>논리적 응집도: 논리적으로 유사한 기능들이 모여 있음</li>
    <li>시간적 응집도: 시간적으로 연관된 기능들이 모여 있음</li>
    <li>절차적 응집도: 순서에 따라 실행되는 기능들이 모여 있음</li>
    <li>교환적 응집도: 동일한 입출력 데이터를 사용</li>
    <li>순차적 응집도: 한 요소의 출력이 다른 요소의 입력</li>
    <li>기능적 응집도: 하나의 기능을 수행</li>
  </ul>

  <h2>8. 객체지향 분석 및 설계</h2>

  <h3>8.1 객체지향 분석 (OOA)</h3>
  <p>문제 영역을 이해하고 요구사항을 분석하여 개념적 모델을 만드는 과정입니다.</p>
  <h4>단계</h4>
  <ol>
    <li>요구사항 분석</li>
    <li>문제 도메인 이해</li>
    <li>객체 식별</li>
    <li>클래스 추출</li>
    <li>관계 정의</li>
  </ol>

  <h3>8.2 객체지향 설계 (OOD)</h3>
  <p>분석 결과를 바탕으로 구현 가능한 설계를 만드는 과정입니다.</p>
  <h4>단계</h4>
  <ol>
    <li>아키텍처 설계</li>
    <li>상세 설계</li>
    <li>인터페이스 설계</li>
    <li>데이터 구조 설계</li>
    <li>알고리즘 설계</li>
  </ol>

  <h3>8.3 UML (Unified Modeling Language)</h3>
  <p>객체지향 시스템을 시각적으로 표현하기 위한 표준 모델링 언어입니다.</p>
  <h4>다이어그램 종류</h4>
  <ul>
    <li>구조 다이어그램: 클래스, 객체, 컴포넌트, 배치 등</li>
    <li>행위 다이어그램: 유스케이스, 순서, 협력, 상태 등</li>
  </ul>

  <h2>9. 메모리 관리</h2>

  <h3>9.1 객체 생성과 소멸</h3>
  <p>객체는 힙 메모리에 생성되며, 참조가 없어지면 가비지 컬렉션의 대상이 됩니다.</p>

  <h3>9.2 가비지 컬렉션 (Garbage Collection)</h3>
  <p>더 이상 사용되지 않는 객체를 자동으로 메모리에서 해제하는 메커니즘입니다.</p>
  <h4>GC 알고리즘</h4>
  <ul>
    <li>Mark and Sweep</li>
    <li>Generational GC</li>
    <li>Incremental GC</li>
  </ul>

  <h3>9.3 메모리 누수 방지</h3>
  <ul>
    <li>불필요한 참조 제거</li>
    <li>리스너/콜백 해제</li>
    <li>스레드 정리</li>
    <li>자원 해제 (try-with-resources)</li>
  </ul>

  <h2>10. 테스트와 객체지향</h2>

  <h3>10.1 단위 테스트 (Unit Test)</h3>
  <p>개별 클래스나 메서드의 동작을 검증하는 테스트입니다.</p>
  <h4>특징</h4>
  <ul>
    <li>독립성</li>
    <li>반복 가능성</li>
    <li>자동화</li>
    <li>빠른 실행</li>
  </ul>

  <h3>10.2 Mock 객체</h3>
  <p>테스트 시 실제 객체 대신 사용하는 가짜 객체입니다.</p>
  <h4>장점</h4>
  <ul>
    <li>의존성 제거</li>
    <li>테스트 속도 향상</li>
    <li>예외 상황 테스트 용이</li>
  </ul>

  <h3>10.3 TDD (Test-Driven Development)</h3>
  <p>테스트를 먼저 작성하고 코드를 작성하는 개발 방법론입니다.</p>
  <h4>과정</h4>
  <ol>
    <li>실패하는 테스트 작성 (Red)</li>
    <li>테스트를 통과하는 최소 코드 작성 (Green)</li>
    <li>코드 개선 (Refactor)</li>
  </ol>

  <h2>11. 현대 객체지향 프로그래밍</h2>

  <h3>11.1 함수형 프로그래밍과의 결합</h3>
  <p>현대 언어들은 객체지향과 함수형 패러다임을 모두 지원합니다.</p>
  <h4>예시</h4>
  <ul>
    <li>Lambda 표현식</li>
    <li>Stream API</li>
    <li>불변 객체</li>
    <li>고차 함수</li>
  </ul>

  <h3>11.2 제네릭 (Generics)</h3>
  <p>타입을 매개변수화하여 타입 안전성과 재사용성을 높이는 기능입니다.</p>
  <h4>장점</h4>
  <ul>
    <li>컴파일 타임 타입 체크</li>
    <li>형변환 제거</li>
    <li>코드 재사용성</li>
  </ul>

  <h3>11.3 애노테이션 (Annotation)</h3>
  <p>코드에 메타데이터를 제공하는 기능입니다.</p>
  <h4>용도</h4>
  <ul>
    <li>컴파일러 정보 제공</li>
    <li>런타임 처리</li>
    <li>코드 자동 생성</li>
  </ul>

  <h2>12. 베스트 프랙티스</h2>

  <h3>12.1 클래스 설계 원칙</h3>
  <ul>
    <li>단일 책임 원칙 준수</li>
    <li>작은 클래스 유지</li>
    <li>명확한 인터페이스 제공</li>
    <li>불변 객체 선호</li>
    <li>적절한 캡슐화</li>
  </ul>

  <h3>12.2 상속 사용 가이드</h3>
  <ul>
    <li>"is-a" 관계일 때만 사용</li>
    <li>깊은 상속 계층 피하기</li>
    <li>구성을 상속보다 선호</li>
    <li>리스코프 치환 원칙 준수</li>
  </ul>

  <h3>12.3 인터페이스 활용</h3>
  <ul>
    <li>구현보다 인터페이스에 의존</li>
    <li>작고 응집력 있는 인터페이스</li>
    <li>적절한 추상화 수준 유지</li>
  </ul>

  <h3>12.4 코드 품질</h3>
  <ul>
    <li>의미 있는 네이밍</li>
    <li>일관된 코딩 스타일</li>
    <li>적절한 주석</li>
    <li>리팩토링 지속적 수행</li>
  </ul>

  <h2>13. 실무 적용</h2>

  <h3>13.1 프레임워크와 객체지향</h3>
  <p>대부분의 현대 프레임워크는 객체지향 원칙을 기반으로 설계됩니다.</p>
  <h4>예시</h4>
  <ul>
    <li>Spring Framework: 의존성 주입, AOP</li>
    <li>Hibernate: ORM, 영속성 관리</li>
    <li>Android: 생명주기, 컴포넌트 기반</li>
  </ul>

  <h3>13.2 아키텍처 패턴</h3>
  <ul>
    <li>MVC: Model-View-Controller</li>
    <li>MVP: Model-View-Presenter</li>
    <li>MVVM: Model-View-ViewModel</li>
    <li>Clean Architecture: 계층 분리</li>
  </ul>

  <h3>13.3 리팩토링</h3>
  <p>코드의 외부 동작은 유지하면서 내부 구조를 개선하는 작업입니다.</p>
  <h4>주요 리팩토링 기법</h4>
  <ul>
    <li>Extract Method: 메서드 추출</li>
    <li>Move Method: 메서드 이동</li>
    <li>Extract Class: 클래스 추출</li>
    <li>Replace Conditional with Polymorphism: 조건문을 다형성으로 치환</li>
  </ul>

  <h3>13.4 성능 고려사항</h3>
  <ul>
    <li>객체 생성 비용 고려</li>
    <li>불필요한 상속 피하기</li>
    <li>적절한 자료구조 선택</li>
    <li>메모리 누수 방지</li>
  </ul>

  </div>
</details>
