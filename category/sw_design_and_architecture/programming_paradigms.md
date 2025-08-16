---
layout: default
title: "Programming Paradigms"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>Programming Paradigms</h2>
  <p>
    프로그래밍 패러다임은 프로그래밍 언어를 사용하여 문제를 해결하는 기본적인 스타일 또는 접근 방식이다. 프로그래밍 패러다임마다 코드를 구성하고 구조화하는 방식이 다르며, 각기 다른 강점과 약점을 가지고 있습니다. 가장 일반적인 프로그래밍 패러다임은 다음과 같다.
    <ul>
      <li>명령형 프로그래밍</li>
      <li>함수형 프로그래밍</li>
      <li>객체 지향 프로그래밍</li>
      <li>논리 프로그래밍</li>
      <li>선언적 프로그래밍</li>
    </ul>
  </p>
</section>

<!-- 섹션 -->
<details open>
<summary><span class="accordion-title" style="font-weight: bold;">Structured Programming</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  구조적 프로그래밍은 루프, 조건문, 서브루틴과 같은 잘 구조화된 제어 흐름 구조의 사용을 강조하는 프로그래밍 패러다임이다. 1960년대와 1970년대에 goto 문이 널리 사용되면서 생겨난 "스파게티 코드"에 대한 대응으로 개발되었다.
  </p>
  <!-- 가로선 추가 -->
  <hr>
  <ul>
    <li><strong>서브루틴(Subroutine):</strong> 특정 작업을 수행하는 독립된 코드 블록으로, 필요할 때 호출해 사용. (함수, 메서드 포함)</li>
    <li><strong>goto 문:</strong> 코드 실행을 지정한 위치로 바로 점프시키는 명령문. (가독성과 유지보수에 악영향 가능)</li>
    <li><strong>스파게티 코드(Spaghetti Code):</strong> 제어 흐름이 복잡하고 뒤엉켜서 이해·수정이 어려운 코드. 주로 goto 남용, 구조 부재로 발생.</li>
  </ul>

</div>
</details>

<!-- 섹션 -->
<details>
<summary><span class="accordion-title" style="font-weight: bold;">Functional Programming</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  함수형 프로그래밍은 계산을 수학 함수의 계산으로 취급하고 상태 변화나 변경 가능한 데이터를 사용하지 않는 프로그래밍 패러다임이다. 함수형 프로그래밍은 고차 함수, 불변성, 재귀를 활용하여 문제를 해결하는 함수를 강조한다. 데이터를 수정하는 대신, 함수형 프로그래밍은 새로운 데이터 구조를 생성한다.
  </p>
  <!-- 가로선 추가 -->
  <hr>
  <ul>
    <li><strong>고차 함수(Higher-Order Function):</strong> 함수를 인자로 받거나 결과로 함수를 반환하는 함수.</li>
    <ul>
        <li>예: map, filter, reduce — 다른 함수를 매개변수로 받아 동작</li>
    </ul>
    <li><strong>재귀(Recursion):</strong> 함수가 자기 자신을 호출하여 문제를 반복적으로 해결하는 방식.</li>
    <ul>
        <li>예: 팩토리얼 계산, 트리 탐색</li>
    </ul>
  </ul>

</div>
</details>

<!-- 섹션 -->
<details>
<summary><span class="accordion-title" style="font-weight: bold;">Object Oriented Programming</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  객체 지향 프로그래밍(OOP)은 객체와 클래스를 사용하여 코드를 구조화하고 구성하는 프로그래밍 패러다임이다. OOP에서 객체는 클래스의 인스턴스이며, 클래스는 객체의 속성과 동작을 정의하는 템플릿이다. OOP는 캡슐화, 상속, 다형성의 원칙을 기반으로 한다.
  </p>
  <!-- 가로선 추가 -->
  <hr>
  <ul>
    <li><strong>캡슐화(Encapsulation):</strong> 데이터와 그 데이터를 처리하는 메서드를 하나로 묶고, 외부에는 필요한 부분만 공개하여 정보 은닉을 구현하는 원칙.</li>
    <li><strong>상속(Inheritance):</strong> 기존 클래스의 속성과 동작을 자식 클래스가 물려받아 재사용하고, 필요에 따라 확장·변경할 수 있는 원칙.</li>
    <li><strong>다형성(Polymorphism):</strong> 같은 메서드 호출이 객체의 타입에 따라 다른 동작을 수행하도록 하는 원칙. (오버로딩·오버라이딩 포함)</li>
  </ul>

</div>
</details>
