---
layout: default
title: "Clean Code Principles"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>Clean Code Principles</h2>
  <p>
    클린 코드란 읽고, 이해하고, 유지하기 쉬운 코드를 말한다. 클린 코드는 코드를 더 읽기 쉽고, 테스트하기 쉽고, 오류 발생 가능성을 낮추도록 설계된 일련의 원칙을 따릅니다. 클린 코드의 핵심 원칙은 다음과 같다.
    <ul>
    <li><strong>명확성:</strong> 코드는 읽고 이해하기 쉬워야 한다.</li>
    <li><strong>단순성:</strong> 코드는 가능한 한 단순해야 하며 불필요한 복잡성은 피해야 한다.</li>
    <li><strong>주석:</strong> 주석은 아껴서 사용해야 하며 복잡하거나 이해하기 어려운 코드를 설명하는 데 필요한 경우에만 사용해야 한다.</li>
    <li><strong>명명:</strong> 변수, 함수, 클래스는 의미 있고 설명적인 이름을 가져야 한다.</li>
    <li><strong>서식:</strong> 가독성을 높이기 위해 코드는 일관되게 서식이 지정되어야 한다.</li>
    <li><strong>기능:</strong> 코드는 작고 단일 목적의 함수와 클래스로 구성되어야 한다.</li>
    <li><strong>오류 처리:</strong> 코드는 일관되고 예측 가능한 방식으로 오류를 처리해야 한다.</li>
    <li><strong>테스트:</strong> 코드는 테스트 가능해야 하며 높은 테스트 범위를 가져야 한다.</li>
    <li><strong>재사용성:</strong> 코드는 재사용 가능하고 모듈식으로 설계되어야 한다.</li>
    <li><strong>성능:</strong> 코드는 효율적이고 성능이 뛰어나도록 설계되어야 한다.</li>
    </ul>
  </p>
</section>

<!-- 섹션 -->
<details open>
<summary>Be Consistent <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  일관성(Consistent)이란 일관된 패턴을 유지하는 것을 의미한다. 여기에는 시스템 전체에서 일관된 명명 규칙, 데이터 구조 및 인터페이스를 사용하고, 확립된 설계 원칙과 모범 사례를 준수하는 것이 포함될 수 있다. 일관성은 시스템의 유지 관리, 이해 및 확장성을 높이는 데 도움이 될 수 있다.
  </p>
</div>
</details>

<!-- 섹션 -->
<details>
<summary>Meaningful Names <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  변수, 함수, 클래스 등 시스템의 다양한 구성 요소에 명확하고 설명적인 이름을 지정하는 것이 좋다. 이렇게 하면 각 구성 요소의 목적과 용도를 명확하게 전달하여 시스템을 더 쉽게 이해하고 유지 관리할 수 있다.
  </p>
</div>
</details>

<!-- 섹션 -->
<details>
<summary>Indentation and Code Style <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  들여쓰기(Indentation)는 공백을 사용하여 관련 코드 줄을 시각적으로 그룹화하여 코드 구조를 더 쉽게 읽고 이해할 수 있도록 하는 방법이다. 코드 스타일은 명명 규칙, 주석 처리, 공백 사용 등 코드의 형식을 지정하고 구조화하는 데 사용되는 규칙과 지침을 의미한다.일관된 들여쓰기와 코드 스타일을 사용하면 코드를 더 읽기 쉽고 이해하기 쉽게 만들어 시스템의 유지 관리성을 개선할 수 있다.
  </p>
</div>
</details>

<!-- 섹션 -->
<details>
<summary>Keep it Small <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  모든 기능을 수행하려는 크고 단일한 컴포넌트보다는 특정 목적에 맞춰 작고 집중된 컴포넌트를 설계하고 구현해야 한다. 이렇게 하면 개별 컴포넌트를 더 쉽게 이해하고, 테스트하고, 수정할 수 있어 시스템의 유지 관리성과 확장성을 향상시킬 수 있다.
  </p>
  <ul>
    <li><strong>컴포넌트:</strong> UI나 기능을 독립적으로 묶어 재사용할 수 있도록 만든 모듈 단위</li>
    <ul>
    <li>하나의 컴포넌트는 자체적인 데이터(상태)와 표현(뷰), 동작(로직)을 포함할 수 있으며, 다른 컴포넌트와 조합해 더 큰 애플리케이션을 구성할 수 있다.</li>
    </ul>
  </ul>

</div>
</details>

<!-- 섹션 -->
<details>
<summary>Pure Functions <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  순수 함수(Pure Functions)는 다음 기준을 충족하는 특정 유형의 함수이다.
    <ul>
        <li>인수라고 하는 입력을 받아 값이나 출력을 반환한다.</li>
        <li>시스템 상태를 수정하거나 외부 리소스와 상호 작용하는 등 관찰 가능한 부작용을 일으키지 않는다.</li>
        <li>동일한 입력이 주어지면 항상 동일한 출력이 반환된다.</li>
        <li>이는 범위를 벗어나는 상태나 변수에 의존하지 않는다.</li>
    </ul>
  순수 함수는 입력과 내부 논리에 의해서만 동작이 결정되므로 예측 가능성이 높고 테스트하기 쉬운 것으로 간주된다. 또한 순수 함수의 출력은 외부 요인의 영향을 받지 않으므로 프로그램의 동작을 추론하기가 더 쉽다. 순수 함수는 함수형 프로그래밍에서 자주 사용되며, 핵심 원칙으로 간주된다. 또한 경쟁 조건 및 기타 동시성 관련 문제가 덜 발생하기 때문에 동시 및 병렬 프로그래밍에도 유용하다.
  </p>
  <ul>
    <li><strong>동시 프로그래밍(Concurrency):</strong> 여러 작업이 논리적으로 동시에 진행되는 것처럼 보이도록 설계하는 방식으로, 한 번에 하나씩 실행되지만, 작업 간 빠른 전환(스위칭)으로 병행 처리처럼 느껴짐.</li>
    <li><strong>병렬 프로그래밍(Parallelism):</strong> 여러 작업을 물리적으로 동시에 실행하는 방식으로, 여러 CPU 코어 또는 프로세서를 활용해 진짜 동시에 연산 수행.</li>
  </ul>
</div>
</details>

<!-- 섹션 -->
<details>
<summary>Minimize Cyclomatic Complexity <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  순환 복잡도(Cyclomatic Complexity)는 프로그램의 구조적 복잡도를 측정하는 지표로, 프로그램 제어 흐름을 통과하는 선형적으로 독립적인 경로의 수에 따라 결정된다. 높은 순환 복잡도는 프로그램을 이해하고, 테스트하고, 유지 관리하기 어렵게 만들 수 있으므로, 시스템 아키텍처에서 순환 복잡도를 최소화하는 것이 바람직한 경우가 많다.</p>
  <p>시스템 아키텍처에서 순환적 복잡도를 최소화하는 방법은 다음과 같다.</p>
  <ul>
    <li>복잡한 기능을 특정 작업을 수행하는 더 작고 간단한 기능으로 분해한다.</li>
    <li>if-else 문과 루프와 같은 제어 구조를 일관되고 예측 가능한 방식으로 사용한다.</li>
    <li>불변성 및 순수 함수와 같은 함수형 프로그래밍 개념과 기술을 사용하면 복잡한 제어 흐름의 필요성을 줄일 수 있다.</li>
    <li>상태 패턴과 같은 디자인 패턴을 사용하여 복잡한 제어 흐름을 단순화한다.</li>
    <li>정기적으로 코드를 검토하고 리팩토링하여 제어 흐름을 단순화한다.</li>
    <li>코드에서 높은 순환 복잡도를 감지하고 보고할 수 있는 정적 코드 분석 도구를 사용한다.</li>
  </ul>
  <p>이러한 모범 사례를 따르면 시스템 아키텍처가 더욱 강력해지고 오류가 줄어들 것이다.</p>
</div>
</details>

<!-- 섹션 -->
<details>
<summary>Avoid Passing Nulls Booleans <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>null이나 부울 값을 전달하면 프로그램에서 예기치 않은 동작과 디버깅하기 어려운 오류가 발생할 수 있다.</p> <p>시스템 아키텍처에서 null이나 부울 값을 전달하지 않도록 하는 몇 가지 방법은 다음과 같다.</p>
  <ul>
    <li>null 대신 Optionals 또는 Maybe 타입을 사용하여 값이 없음을 나타낼 수 있다. 이렇게 하면 값이 없음을 명확하게 알 수 있고 null 참조 예외를 방지할 수 있다.</li>
    <li>함수 인수에 null 또는 Boolean 값을 허용하는 대신 기본값을 사용하면 null 또는 Boolean 값을 확인할 필요가 없어 오류 발생 가능성이 줄어든다.</li>
    <li>Null 객체 패턴을 사용하여 null 값을 정의된 동작을 가진 특수 객체로 대체하면 null 값을 확인할 필요가 없어지고 코드의 가독성이 향상된다.</li>
    <li>부울 값을 다룰 때는 if-else 문 대신 삼항 연산자(?:)를 사용하면 코드가 더 간결해지고 읽기 쉬워진다.</li>
    <li>assert 함수를 사용하여 함수 인수의 유효성을 검사하고 유효하지 않으면 예외를 발생시킨다.</li>
  </ul>
  <p>이러한 모범 사례를 따르면 시스템 아키텍처가 더욱 강력해지고 오류가 줄어들 것이다.</p>
</div>
</details>


<!-- 섹션 -->
<details>
<summary>Keep Framework Code Distant <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  프레임워크 코드를 분리한다는 것은 애플리케이션 코드와 프레임워크 코드를 분리하는 것을 의미한다. 이렇게 하면 애플리케이션 코드베이스와 프레임워크를 독립적으로 유지 관리, 테스트 및 업그레이드하기가 더 쉬워진다.시스템 아키텍처에서 프레임워크 코드를 분리하는 몇 가지 방법은 다음과 같다.
  <ol>
    <li>추상화 계층을 사용하여 애플리케이션 코드와 프레임워크 코드를 분리한다. 이를 통해 프레임워크의 세부 사항을 몰라도 애플리케이션 코드를 작성할 수 있다.</li>
    <li>의존성 주입을 사용하여 애플리케이션 코드와 프레임워크 코드를 분리한다. 이를 통해 애플리케이션 코드는 프레임워크 객체를 직접 인스턴스화하지 않고도 프레임워크의 기능을 사용할 수 있다.</li>
    <li>애플리케이션 코드에서 특정 프레임워크에 특화된 라이브러리나 클래스를 사용하지 않는다. 이렇게 하면 나중에 필요할 때 다른 프레임워크로 쉽게 전환할 수 있다.</li>
    <li>애플리케이션 코드가 프레임워크와 상호 작용할 수 있도록 표준 인터페이스를 사용한다. 이를 통해 프레임워크의 세부 사항을 몰라도 애플리케이션 코드를 작성할 수 있다.</li>
    <li>애플리케이션과 프레임워크 코드를 별도의 프로젝트 및/또는 저장소에 보관한다.</li>
  </ol>
  이러한 모범 사례를 따르면 시스템 아키텍처는 유지 관리와 테스트가 더 용이해지고 오류가 덜 발생하며, 필요한 경우 프레임워크를 업그레이드하거나 전환하기가 더 쉬워진다.
  </p>
</div>
</details>

<!-- 섹션 -->
<details>
<summary>Use Correct Constructs <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>깔끔한 코드 원칙의 맥락에서 "올바른 구조를 사용한다"는 것은 루프, 조건문, 함수와 같은 적절한 프로그래밍 구조를 사용하여 코드를 쉽게 이해하고 유지 관리하고 수정할 수 있도록 하는 것을 의미한다.</p>
  <p>올바른 구문을 사용할 경우, 코드는 논리적이고 직관적인 방식으로 구성되어야 하며, 적절한 제어 흐름 명령문과 데이터 구조를 활용하여 해당 작업을 수행해야 한다. 또한, 불필요하거나 지나치게 복잡한 구문은 코드를 이해하거나 추론하기 어렵게 만들어서는 안 된다.</p>
  <p>또한, 올바른 구조란 문제에 맞는 올바른 구조를 사용하는 것을 의미한다. 예를 들어, 배열을 반복하려면 재귀 대신 for 루프를 사용해야 하며, 전역 변수는 사용하지 말고 대신 함수 인수와 반환 값을 사용하여 코드의 다른 부분 간에 데이터를 전달해야 한다.</p>
  <p>올바른 구조를 사용하면 코드의 가독성과 유지 관리가 더 좋아지고 버그가 덜 발생하여 다른 개발자가 코드를 이해하고 디버깅하고 확장하기가 더 쉬워진다.</p>
</div>
</details>

<!-- 섹션 -->
<details>
<summary>Tests should be fast and independent <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  테스트 코드는 실행 속도가 빨라야 하며 서로 간에 의존성이 없어야 한다. 빠른 테스트는 개발자가 코드 변경 시 자주 실행하게 만들고, 문제를 조기에 발견할 수 있게 한다. 또한 테스트가 독립적이어야 한 테스트의 실패가 다른 테스트의 결과에 영향을 주지 않아 문제 원인을 명확히 파악할 수 있다. 이를 위해 각 테스트는 실행 전 동일한 초기 상태를 준비하고, 외부 시스템(네트워크, 데이터베이스 등)에 의존하지 않도록 설계하는 것이 좋다. 이러한 접근은 테스트 신뢰성을 높이고 유지보수를 쉽게 만들어준다.
  </p>
</div>
</details>

<!-- 섹션 -->
<details>
<summary>Organize code by actor it belongs to <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  코드는 기능과 책임이 명확한 주체(Actor) 단위로 구성하는 것이 좋다. 이렇게 하면 관련된 코드가 한곳에 모여 유지보수가 쉬워지고, 불필요한 의존성을 줄일 수 있다. 예를 들어 웹 애플리케이션에서는 Controller, Service, Repository 계층을 분리해 각 계층이 맡은 역할만 수행하도록 구성한다. 이렇게 책임 기반으로 코드를 구조화하면 다른 개발자가 해당 기능을 빠르게 이해하고 수정할 수 있으며, 프로젝트의 확장성도 높아진다.
  </p>
</div>
</details>

<!-- 섹션 -->
<details>
<summary>Command Query Separation <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  명령-쿼리 분리(CQS)는 메서드 또는 함수의 역할을 명령과 쿼리, 두 가지 범주로 분리하는 소프트웨어 설계 원칙이다. 명령은 시스템 상태를 변경하는 메서드이고, 쿼리는 정보를 반환하지만 시스템 상태를 변경하지 않는 메서드이다.
  </p>
</div>
</details>

<!-- 섹션 -->
<details>
<summary>Keep it simple and refactor often <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  코드는 가능한 한 단순하게 유지해야 하며, 필요할 때마다 리팩토링하여 품질을 관리해야 한다. 복잡한 구조나 불필요한 추상화는 버그를 만들고 유지보수를 어렵게 한다. KISS 원칙(Keep It Simple, Stupid)을 따르며, 중복 코드를 제거하고, 메서드를 작게 나누고, 명확한 이름을 사용해야 한다. 기능을 추가하거나 수정할 때는 리팩토링을 병행하여 기술 부채를 줄이고 코드 가독성을 높여야 한다. 이를 통해 장기적으로 안정적이고 확장 가능한 코드를 유지할 수 있다.
  </p>
</div>
</details>
