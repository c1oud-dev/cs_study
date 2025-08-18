---
layout: default
title: "Architectural Principles"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>Architectural Principles</h2>
  <p>Architectural Principles(아키텍처 원칙)은 소프트웨어 시스템을 설계·구축할 때 따라야 할 기본 지침이다. 큰 그림에서 시스템을 어떻게 나눌지, 어떻게 연결할지, 어떻게 확장·유지할지를 정의한다.</p>
  <p><strong>주요 Architectural Principles</strong></p>
  <ol>
    <li><strong>Separation of Concerns (관심사의 분리)</strong></li>
    <ul>
      <li>서로 다른 기능이나 역할을 분리해서 모듈화하면 복잡성을 줄이고 유지보수가 쉬워짐.</li>
      <li>예: 프레젠테이션 계층, 비즈니스 로직 계층, 데이터 계층을 나누는 3-tier 아키텍처.</li>
    </ul>
    <li><strong>Single Responsibility (단일 책임 원칙)</strong></li>
    <ul>
      <li>각 컴포넌트는 하나의 책임만 가지도록 설계.</li>
      <li>특정 기능 변경이 특정 모듈만 영향을 받도록 함.</li>
    </ul>
    <li><strong>Loose Coupling (느슨한 결합)</strong></li>
    <ul>
      <li>모듈 간의 의존성을 최소화, 서로 독립적으로 교체·확장 가능.</li>
      <li>예: 인터페이스, 의존성 주입(DI).</li>
    </ul>
    <li><strong>High Cohesion (높은 응집도)</strong></li>
    <ul>
      <li>관련된 기능들은 같은 모듈에 묶고, 서로 다른 책임은 분리.</li>
      <li>모듈 내부는 단단히 결합되어야 하고, 모듈 간에는 느슨해야 함.</li>
    </ul>
    <li><strong>Scalability (확장성)</strong></li>
    <ul>
      <li>시스템이 사용량 증가에도 잘 대응할 수 있도록 설계.</li>
      <li>예: 수평 확장(서버 추가) / 수직 확장(서버 성능 업그레이드).</li>
    </ul>
    <li><strong>Reusability (재사용성)</strong></li>
    <ul>
      <li>동일하거나 유사한 기능을 여러 곳에서 재사용 가능하도록 설계.</li>
      <li>중복 코드를 줄이고 개발 생산성을 높임.</li>
    </ul>
    <li><strong>Security (보안성)</strong></li>
    <ul>
      <li>인증, 권한, 데이터 보호 등을 아키텍처 수준에서 고려해야 함.</li>
      <li>나중에 덧붙이는 게 아니라 처음부터 내장되어야 함.</li>
    </ul>
    <li><strong>Performance & Efficiency (성능과 효율성)</strong></li>
    <ul>
      <li>리소스를 효율적으로 사용하면서 사용자에게 빠른 응답 제공.</li>
      <li>예: 캐싱, 데이터베이스 인덱싱.</li>
    </ul>
    <li><strong>Modularity & Replaceability (모듈성 & 교체 가능성)</strong></li>
    <ul>
      <li>시스템을 작은 모듈 단위로 나눠서 교체·업데이트가 용이하도록 설계.</li>
      <li>마이크로서비스 아키텍처가 대표적인 예.</li>
    </ul>
    <li><strong>Evolution & Maintainability (진화 가능성 & 유지보수성)</strong></li>
    <ul>
      <li>새로운 요구사항이나 기술 변화에 쉽게 적응 가능해야 함.</li>
      <li>코드뿐만 아니라 아키텍처 자체가 변경에 유연해야 함.</li>
    </ul>
  </ol>
</section>

<!-- 설명 -->
<details open>
<summary><span class="accordion-title">Component Principles</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>소프트웨어 아키텍처에서의 컴포넌트 원칙은 모듈화되고, 재사용 가능하며, 이해하기 쉽고, 테스트와 유지보수가 용이한 소프트웨어 컴포넌트를 설계하고 구현하기 위한 지침을 말한다.</p>
  <p>소프트웨어 아키텍처에서 핵심적인 컴포넌트 원칙에는 다음이 포함된다.</p>
  <ul>
    <li><strong>High cohesion (높은 응집도)</strong></li>
    <li><strong>Low coupling (낮은 결합도)</strong></li>
    <li><strong>Separation of concerns (관심사의 분리)</strong></li>
    <li><strong>Interface-based design (인터페이스 기반 설계)</strong></li>
    <li><strong>Reusability (재사용성)</strong></li>
    <li><strong>Testability (테스트 가능성)</strong></li>
    <li><strong>Modularity (모듈성)</strong></li>
    <li><strong>Interoperability (상호 운용성)</strong></li>
  </ul>
  <p>이러한 컴포넌트 원칙들을 따르면, 소프트웨어는 이해하기 쉽고, 유지·보수가 용이하며, 확장이 쉬운 방식으로 개발될 수 있고, 버그가 발생할 가능성도 줄어든다. 또한 더 나은 코드 재사용이 가능해지고, 코드를 테스트하고 변경하는 것이 쉬워지며, 컴포넌트가 다양한 환경에서 재사용될 수 있으므로 코드 재사용성이 더욱 향상된다.</p>
</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title">Policy vs Detail</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>소프트웨어 아키텍처에서 Policy(정책)와 Detail(세부사항)의 구분은 고수준 의사결정과 저수준 구현 세부사항을 분리하는 것을 의미한다.</p>
  <p>Policy(정책)는 시스템의 전체적인 동작과 구조를 정의하는 고수준 의사결정을 의미한다. 여기에는 전체 아키텍처, 시스템 인터페이스, 주요 컴포넌트와 그 상호작용 등이 포함된다.이러한 정책 결정은 주로 아키텍트나 설계자가 내리며, 시스템의 전반적인 방향을 설정한다.</p>
  <p>Detail(세부사항)은 정책 결정을 실제로 구현하기 위해 필요한 저수준 구현 세부사항을 의미한다. 여기에는 구체적인 알고리즘, 자료 구조, 그리고 시스템 컴포넌트를 구성하는 코드 등이 포함된다. 세부사항은 주로 개발자가 구현하며, 시스템이 실제로 동작하도록 책임진다.</p>
  <p><strong>정리: Policy는 큰 그림(아키텍처, 인터페이스, 구조)을 결정하는 원칙이고, Detail은 그것을 실제로 구현하는 코드와 알고리즘이다.</strong></p>
</div>
</details>


<!-- 설명 -->
<details>
<summary><span class="accordion-title">Coupling and Cohesion(결합도와 응집도)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>결합도(Coupling)와 응집도(Cohesion)는 소프트웨어 아키텍처에서 시스템 내 컴포넌트 간의 상호 의존성을 측정하는 두 가지 원칙이다.</p>
    <ul><li>결합도(Coupling)는 한 컴포넌트가 다른 컴포넌트에 얼마나 의존하는지를 나타낸다.</li>
      <ul>
        <li><strong>높은 결합도(High coupling):</strong> 한 컴포넌트가 변경되면 다른 컴포넌트에도 영향을 미치므로 시스템을 이해·테스트·유지보수하기 어려워진다.</li>
        <li><strong>낮은 결합도(Low coupling):</strong> 한 컴포넌트의 변경이 다른 컴포넌트에 거의 영향을 주지 않아, 시스템이 더 모듈화되고 이해·테스트·유지보수가 쉬워진다.</li>
      </ul>
    </ul>
    <ul><li>응집도(Cohesion)는 한 컴포넌트가 맡고 있는 책임들이 서로 얼마나 관련이 있는지를 나타낸다.</li>
      <ul>
        <li><strong>높은 응집도(High cohesion):</strong> 컴포넌트가 하나의 명확한 목적을 가지고, 그 목적과 관련된 기능과 데이터만 포함한다.</li>
        <li><strong>낮은 응집도(Low cohesion):</strong> 컴포넌트가 여러 가지 서로 관련 없는 책임을 가지고 있어 이해·테스트·유지보수가 어렵다.</li>
      </ul>
    </ul>
</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title">Boundaries(경계)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>소프트웨어 아키텍처에서 경계(boundaries)란 서로 다른 컴포넌트나 시스템 사이의 인터페이스 또는 분리 지점을 의미한다. 이러한 경계는 물리적인 것일 수도 있고(예: 분산 시스템에서 서로 다른 마이크로서비스 간의 경계), 논리적인 것일 수도 있다(예: 애플리케이션 내의 서로 다른 계층 간의 경계).</p>
  <p>경계가 중요한 이유는, 그것이 서로 다른 컴포넌트나 시스템 간의 상호작용 지점을 정의하고, 이들이 서로 어떻게 통신할지를 규정하기 때문이다. 명확한 경계를 정의하면, 컴포넌트나 시스템 간의 상호작용이 잘 정의되고 이해하기 쉬워지므로 시스템을 이해·테스트·유지보수하기가 더 쉬워진다.</p>
  <p><strong>정리: Boundaries는 시스템 내 컴포넌트/계층/서비스 사이의 구분선이며, 명확히 정의하면 이해·테스트·유지보수가 쉬워진다.</strong></p>
</div>
</details>
