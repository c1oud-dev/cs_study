---
layout: default
title: "Enterprise Patterns"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>Enterprise Patterns</h2>
  <p><b>엔터프라이즈 패턴(Enterprise Patterns)</b>은 <b>엔터프라이즈 SW 애플리케이션 개발</b>에서 흔히 사용되는 일련의 디자인 패턴들이다. 이 패턴들은 대규모·복잡한 SW 시스템 개발 과정에서 발생하는 <b>공통 문제들을 해결하기 위한 공통된 용어(vocabulary)와 모범 사례(best practices)</b>를 제공한다.</p>
  <p>대표적인 엔터프라이즈 패턴의 예로는 다음이 있다.</p>
  <ul>
    <li>Domain-Driven Design (DDD)</li>
    <li>Model-View-Controller (MVC)</li>
    <li>Service Oriented Architecture (SOA)</li>
    <li>Command and Query Responsibility Segregation (CQRS)</li>
    <li>Event Sourcing</li>
    <li>Microservices</li>
    <li>Event-Driven Architecture (EDA)</li>
  </ul>
  <p>이러한 패턴들은 <b>관심사의 명확한 분리(separation of concerns)</b>를 제공하고, <b>보다 모듈화되고 유연한 아키텍처</b>를 가능하게 함으로써 SW의 <b>유지보수성과 확장성</b>을 향상시킬 수 있다.</p>
  <p><strong>정리: Enterprise Patterns는 대규모 SW의 공통 문제를 해결하기 위한 모범 사례 아키텍처 패턴 모음이다.</strong></p>
</section>

<!-- 설명 -->
<details open>
<summary><span class="accordion-title">DTOs(Data Transfer Object, 데이터 전송 객체)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>데이터 전송 객체 디자인 패턴은 엔터프라이즈 애플리케이션 아키텍처 패턴 중 하나로, 전송을 위해 데이터를 수집하고 캡슐화하는 객체를 사용한다. 데이터 전송 객체는 본질적으로 데이터 구조와 같다. 비즈니스 로직을 포함하지 않지만, 직렬화 및 역직렬화 메커니즘을 포함해야 한다.</p>
  <p><strong>정리: DTO(Data Transfer Object)는 계층 간 데이터 전달만 담당하고 비즈니스 로직은 없는 객체이다.</strong></p>

</div>
</details>


<!-- 설명 -->
<details>
<summary><span class="accordion-title"  style="color: #000; font-weight: bold;">Identity Maps</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>Identity Map</b>은 엔터프라이즈 애플리케이션 개발에서 사용되는 패턴으로, 데이터베이스에서 로드된 객체들을 그들의 <b>고유 식별자(Unique Identifier)</b>를 키로 하여 매핑(map) 형태로 유지하는 방식이다. 이 패턴은 동일한 데이터가 여러 번 접근될 때 <b>메모리에 동일한 객체가 중복 생성되지 않도록 보장</b>한다.</p>
  <p>Identity Map 패턴은 일반적으로 <b>ORM(Object-Relational Mapping) 도구</b>와 함께 사용된다. 객체가 데이터베이스에서 로드될 때, 우선 <b>Identity Map에 이미 존재하는지 확인</b>한다. 만약 존재한다면 새 복사본을 만드는 대신 기존 객체를 반환한다.</p>
  <p><strong>정리: Identity Map은 DB에서 로드된 객체를 캐싱해 중복 생성을 막는 패턴이다.</strong></p>

</div>
</details>


<!-- 설명 -->
<details>
<summary><span class="accordion-title">Use Cases(유스 케이스)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>Use Case</b>는 엔터프라이즈 애플리케이션 개발에서 시스템의 <b>기능적 요구사항</b>을 표현하는 데 사용되는 패턴이다. 유스 케이스는 <b>시스템과 사용자 간의 상호작용</b>과, 특정 목표를 달성하기 위해 필요한 단계를 설명한다. 이 방식은 개발팀과 이해관계자 모두가 쉽게 이해할 수 있는 방식으로 시스템의 요구사항을 캡처하는 방법이다.</p>
  <p>유스 케이스는 사용자가 특정 목표를 달성하기 위해 요청을 했을 때, 시스템이 수행하는 <b>일련의 동작(sequence of actions)</b>을 기술한다. 보통 유스 케이스에는 다음이 포함된다.</p>
  <ul>
    <li><strong>행위자(Actor, 사용자):</strong> 행동을 시작하는 주체<li>
    <li><strong>목표(Goal):</strong> 행위자가 이루고자 하는 것<li>
    <li><strong>단계(Steps):</strong> 목표를 달성하기 위한 과정, 대체 경로나 오류 상황 포함<li>
    <li><strong>예상 결과(Expected Outcome):</strong> 상호작용의 결과<li>
  </ul>
  <p>유스 케이스는 요구사항을 명확하고 구체적으로 이해할 수 있게 하여, 시스템의 <b>설계와 개발을 이끌어가는 기준</b>으로 자주 사용된다.</p>
  <p><strong>정리: Use Case는 사용자와 시스템의 상호작용을 통해 목표 달성 과정을 설명하는 요구사항 패턴이다.</strong></p>

</div>
</details>


<!-- 설명 -->
<details>
<summary><span class="accordion-title">Repositories(리포지토리)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>Repository</b>는 엔터프라이즈 애플리케이션 개발에서 <b>데이터 저장소에 접근하는 일관적이고 추상화된 방법</b>을 제공하는 패턴이다. 리포지토리는 애플리케이션과 데이터 저장소 사이의 <b>추상화 계층(Abstraction Layer)</b> 역할을 하며, 데이터 접근과 조작을 위한 <b>간단하고 일관된 API</b>를 제공한다.</p>
  <p>리포지토리 패턴은 데이터 접근 코드를 <b>구조화(조직화)</b>하고, 객체를 <b>조회·저장하는 로직을 캡슐화</b>하는 데 사용된다. 이를 통해 애플리케이션의 나머지 부분과 데이터 접근 로직의 <b>관심사를 분리</b>할 수 있다. 따라서 애플리케이션 코드는 특정 데이터 저장 기술에 의존하지 않고, <b>인터페이스를 기준</b>으로 작성될 수 있다.</p>
  <p><strong>정리: Repository는 데이터 접근을 추상화해 일관된 API로 제공하는 계층 패턴이다.</strong></p>

</div>
</details>


<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Mappers(매퍼)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>Mapper</b>는 엔터프라이즈 애플리케이션 개발에서 <b>서로 다른 데이터 모델 간 매핑을 일관적이고 추상화된 방식으로 제공</b>하는 패턴이다. 매퍼는 애플리케이션과 데이터 저장소 사이의 <b>추상화 계층(Abstraction Layer)</b> 역할을 하며, <b>데이터 변환을 위한 단순하고 일관된 API</b>를 제공한다.</p>
  <p>매퍼는 데이터를 한 형식 또는 모델에서 다른 형식이나 모델로 변환하는 데 사용되는 <b>컴포넌트</b>이다. 예를 들어, 매퍼는 데이터베이스 모델을 도메인 모델로 변환하거나, 도메인 모델을 DTO(Data Transfer Object)로 변환하는 데 활용될 수 있다.</p>
  <p><strong>정리: Mapper는 서로 다른 데이터 모델 간 변환을 담당하는 추상화 계층 패턴이다.</strong></p>

</div>
</details>



<!-- 설명 -->
<details>
<summary><span class="accordion-title"  style="color: #000; font-weight: bold;">Transaction Script(트랜잭션 스크립트)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>Transaction Script</b>는 엔터프라이즈 애플리케이션 개발에서 사용되는 패턴으로, <b>비즈니스 로직을 단일 절차적 스크립트</b>로 구성하는 방식이다. 이 패턴은 주로 단순한 <b>CRUD(생성, 조회, 수정, 삭제)</b> 작업에 사용되며, 특정 트랜잭션에 필요한 모든 로직이 하나의 스크립트나 함수 안에 포함된다.</p>
  <p>이 패턴은 <b>구현이 간단하고 이해하기 쉬운 장점</b>이 있지만, 애플리케이션의 복잡성이 커질수록 관리가 어렵고 비효율적일 수 있다. 따라서 복잡한 애플리케이션에는 <b>Domain-Driven Design(DDD)</b>이나 <b>Active Record 패턴</b> 같은 대안이 더 적합할 수 있다.</p>
  <p><strong>정리: Transaction Script는 단순 CRUD 로직을 하나의 스크립트로 처리하는 간단한 패턴이다.</strong></p>

</div>
</details>



<!-- 설명 -->
<details>
<summary><span class="accordion-title">Commands Queries(Command and Query Responsibility Segregation, 명령-조회 책임 분리)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>CQRS</b> 패턴은 엔터프라이즈 애플리케이션 개발에서 사용되는 기법으로, 시스템의 상태를 변경하는 작업(데이터 생성, 수정, 삭제 등)을 처리하는 <b>명령(쓰기) 작업</b>과, 데이터를 단순히 가져오는 조회(읽기) 작업의 책임을 분리하는 것이다.</p>
  <ul>
    <li><strong>Command(명령)</strong> 작업은 Command Handler에 의해 처리되며, 이들은 데이터를 검증하고 적절한 비즈니스 로직을 실행하는 역할을 한다.</li>
    <li><strong>Query(조회)</strong> 작업은 시스템에서 데이터를 읽어오는 데 사용되며(예: 데이터베이스나 캐시에서 읽기), 이는 Query Handler에 의해 처리되고, 적절한 쿼리를 실행한 후 호출자에게 데이터를 반환한다.</li>
  </ul>
  <p><strong>정리: CQRS는 쓰기와 읽기를 Command Handler와 Query Handler로 분리해 책임을 나누는 패턴이다.</strong></p>

</div>
</details>


<!-- 설명 -->
<details>
<summary><span class="accordion-title">Value Object(값 객체)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>Value Object</b>는 엔터프라이즈 애플리케이션 개발에서 사용되는 패턴으로, 도메인 개념을 모델링하기 위해 사용되는 <b>단순하고 불변(immutable)한 값</b>을 표현한다. 이는 엔터티(Entity)는 아니지만 도메인에서 중요한 데이터를 캡슐화하는 데 활용된다.</p>
  <p>Value Object는 <b>정체성(identity)이 아니라 값(value)으로 정의</b>된다. 즉, 두 Value Object의 값이 같다면, 그들이 동일한 객체인지 여부와 관계없이 <b>동등(equal)</b>하다고 간주된다.</p>
  <p><strong>정리: Value Object는 값 자체로 정의되는 불변 객체, 동일 값이면 동일한 것으로 간주한다.</strong></p>

</div>
</details>


<!-- 설명 -->
<details>
<summary><span class="accordion-title">Domain Model(도메인 모델)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>Domain Model</b>은 엔터프라이즈 애플리케이션 개발에서 사용되는 패턴으로, 특정 도메인의 <b>비즈니스 개념과 규칙</b>을 표현한다. 주로 문제 도메인(Problem Domain), 즉 특정 비즈니스의 전문 영역을 모델링하는 데 활용된다.</p>
  <p>도메인 모델은 도메인의 <b>현실 세계 개념과 엔터티를 표현하는 객체들의 집합</b>이다. 이 객체들은 보통 클래스나 타입으로 모델링되며, 해당 도메인에 특화된 <b>데이터와 행위(behavior)</b>를 캡슐화한다.</p>
  <p>도메인 모델은 자신이 표현하는 비즈니스 개념의 <b>상태(state)와 행위(behavior)</b>를 책임지고, 도메인의 규칙과 제약 사항을 <b>강제(enforce)</b>하는 역할을 한다.</p>
  <p><strong>정리: Domain Model은 비즈니스 개념과 규칙을 객체로 표현해 상태와 행위를 캡슐화하는 패턴이다.</strong></p>

</div>
</details>


<!-- 설명 -->
<details>
<summary><span class="accordion-title">Entity(엔터티)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>Entity</b>는 엔터프라이즈 애플리케이션 개발에서 사용되는 패턴으로, <b>고유한 정체성(identity)과 생명주기(lifetime)를 가지는 비즈니스 개념</b>을 표현한다. 주로 고객(Customer), 주문(Order), 계좌(Account)와 같이 <b>구별 가능한 정체성과 라이프사이클</b>을 가진 현실 세계의 객체나 개념을 모델링하는 데 사용된다.</p>
  <p>엔터티는 <b>정체성(identity)으로 정의</b>된다. 즉, 두 엔터티의 상태(state)가 다르더라도 <b>동일한 정체성</b>을 가진다면 같은 엔터티로 간주된다. 엔터티는 보통 <b>Primary Key(기본 키)</b> 같은 <b>고유 식별자(unique identifier)</b>를 가지고 있으며, 그 상태를 설명하는 속성(properties)이나 특성(attributes)을 함께 가진다.</p>
  <p><strong>정리: Entity는 고유 식별자로 구분되는 비즈니스 객체, 상태와 속성을 가지며 생명주기를 갖는다.</strong></p>

</div>
</details>


<!-- 설명 -->
<details>
<summary><span class="accordion-title">ORM(Object-Relational Mapping, 객체-관계 매핑)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>ORM</b>은 엔터프라이즈 애플리케이션 개발에서 사용되는 기법으로, <b>객체 지향 프로그래밍 모델과 관계형 데이터베이스 모델 간 매핑</b>을 제공한다. 이를 통해 개발자는 코드에서 객체로 작업할 수 있고, ORM 도구가 그 객체들을 적절한 데이터베이스 연산으로 변환해 처리한다.</p>
  <p>ORM은 관계형 데이터베이스를 다루는 복잡성을 <b>추상화(Abstraction)</b>하여, 개발자가 더 높은 수준의 객체 지향 API로 데이터베이스와 상호작용할 수 있게 설계되었다. ORM은 코드 속의 객체를 데이터베이스의 <b>테이블과 행(row)</b>에 매핑하고, 반대로도 변환해주는 라이브러리와 도구들을 제공한다.</p>
  <p>이를 통해 개발자는 복잡한 SQL 쿼리를 작성하지 않고도, <b>익숙한 객체 지향 방식</b>으로 데이터를 다룰 수 있다.</p>
  <p><strong>정리: ORM은 객체와 관계형 DB를 매핑해 SQL 대신 객체 지향 방식으로 DB를 다루게 하는 기술이다.</strong></p>

</div>
</details>
