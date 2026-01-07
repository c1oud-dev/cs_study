---
layout: default
title: "CS 외의 개념"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>CS 외의 개념</h2>
</section>

<!-- chapter -->
<details open>
  <summary><span class="accordion-title">1️⃣ 백엔드 개발 환경</span> <span class="indicator">펼치기</span></summary><div class="accordion-content">
  
<details open>
<summary style="font-size:1rem;"><b>프레임워크</b></summary>
<div class="accordion-content">
    <p>프레임워크는 <b>애플리케이션을 만들 때 반복해서 필요한 기본 구조와 규칙을 미리 만들어 둔 개발 뼈대</b>입니다. 쉽게 말하면, 개발자가 모든 걸 처음부터 조립하는 게 아니라, 프레임워크가 제공하는 흐름과 틀 안에서 필요한 기능만 채워 넣도록 도와주는 형태입니다.</p>
    <p>핵심은 두 가지입니다.<br>
    첫째, <b>구조와 흐름을 표준화</b>해 줍니다. 예를 들어 요청 처리 흐름, 예외 처리 방식, 계층 분리 같은 기본 아키텍처를 프레임워크가 권장하는 방식으로 잡아주기 때문에, 프로젝트가 커져도 일관성을 유지하기 쉽습니다.<br>
    둘째, <b>공통 기능을 제공</b>해 줍니다. 웹 개발이라면 라우팅, 인증/인가, 트랜잭션, 데이터 접근 같은 반복 요소를 기본으로 지원해서, 개발자는 비즈니스 로직에 더 집중할 수 있습니다.</p>
    <p>그리고 라이브러리와 자주 비교되는데, 차이는 보통 <b>제어 흐름의 주도권</b>에 있습니다. 라이브러리는 개발자가 필요할 때 호출해서 쓰는 도구에 가깝고, 프레임워크는 전체 실행 흐름을 프레임워크가 주도하면서 개발자는 그 규칙에 맞춰 확장하는 방식에 가깝습니다.</p>
</div>
</details>

<details>
<summary style="font-size:1rem;"><b>서버 사이드 로직</b></summary>
<div class="accordion-content">
    <p>서버 사이드 로직은 <b>사용자 요청을 서버에서 처리해서 결과를 만들어 주는 핵심 처리 과정</b>입니다.</p>
    <p>클라이언트가 버튼을 누르거나 API를 호출하면, 서버는 그 요청을 받아서 <b>인증·인가 확인, 입력값 검증, 비즈니스 규칙 적용, DB 조회·저장, 외부 서비스 연동</b> 같은 처리를 한 뒤, 최종적으로 <b>응답 데이터나 화면 결과</b>를 내려줍니다.</p>
    <p>예를 들면 로그인 성공 여부 판단, 게시글 등록 시 권한 체크, 주문 결제 처리, 통계 계산처럼 <b>보안과 데이터 정합성이 중요한 작업</b>은 보통 서버에서 담당합니다. 이렇게 서버에서 처리하면 규칙을 한곳에서 통제할 수 있어서 일관성이 좋아지고, 민감한 정보도 상대적으로 안전하게 다룰 수 있습니다.</p>
</div>
</details>

<details>
<summary style="font-size:1rem;"><b>ORM</b></summary>
<div class="accordion-content">
    <p>ORM은 <b>객체(Object)와 관계형 데이터베이스(Relational DB) 테이블을 매핑해서, SQL을 직접 많이 쓰지 않고도 DB를 다루게 해주는 기술</b>입니다.</p>
    <p>자바에서는 보통 엔티티 같은 객체를 만들고, ORM이 그 객체를 <b>테이블의 행(row)</b>처럼 저장·조회·수정·삭제할 수 있게 변환해 줍니다. 그래서 개발자는 SQL 작성보다 <b>도메인 로직과 객체 모델링</b>에 더 집중할 수 있고, 반복적인 CRUD 코드도 줄어듭니다.</p>
    <p>다만 ORM이 SQL을 대신 만들어 주는 만큼, <b>실제로 어떤 쿼리가 나가는지 확인하고 성능 이슈(N+1 같은 것)를 관리하는 감각</b>은 필요합니다.</p>
</div>
</details>

<details>
<summary style="font-size:1rem;"><b>Spring Data JPA(Hibernate)</b></summary>
<div class="accordion-content">
    <p>Spring Data JPA는 <b>JPA 기반 데이터 접근을 "Repository" 추상화로 제공해서, CRUD 같은 반복 코드를 크게 줄여주는 스프링 모듈</b>입니다.</p>
    <h3>괄호 안에 Hibernate라고 적는 이유는?</h3>
    <p><b>Spring Data JPA는 "JPA 기반 Repository 추상화"</b>이고, 실제로 DB에 붙어서 SQL 생성·실행 같은 ORM 동작을 하는 <b>JPA 구현체(Provider)가 Hibernate인 경우가 많기 때문</b>입니다.</p>
    <p>특히 <b>Spring Boot에서는 JPA를 쓸 때 기본 JPA Provider로 Hibernate가 자동 설정되는 흐름</b>이 일반적이라, "우리는 Spring Data JPA를 쓰고, 그 아래 엔진은 Hibernate다"를 한 줄로 명확히 보여주려고 괄호에 Hibernate를 붙입니다.</p>
</div>
</details>

<details>
<summary style="font-size:1rem;"><b>템플릿(Thymeleaf)</b></summary>
<div class="accordion-content">
    <p><b>템플릿</b>은 <b>서버에서 HTML 화면을 만들기 위한 "화면 뼈대"</b>를 뜻합니다. 그리고 Thymeleaf 같은 <b>템플릿 엔진</b>이 그 뼈대(HTML)에 데이터를 끼워 넣어서 <b>최종 HTML을 렌더링</b>해 브라우저에 내려줍니다.</p>
    <p>필요한 상황은 보통 이렇습니다.</p>
    <ul>
        <li>서버 사이드 렌더링(SSR)으로 화면을 직접 내려줄 때</li>
        <li>로그인/관리자 페이지처럼 "페이지 단위"가 명확한 웹 화면을 빠르게 만들 때</li>
        <li>프론트가 SPA여도 "풀백 화면"이 필요할 때</li>
    </ul>
    <p>반대로, 백엔드가 <b>REST API만 제공</b>하고 화면은 <b>React 같은 SPA가 전부 담당</b>하면, 일반적인 페이지 렌더링 용도로는 템플릿 엔진이 <b>필수는 아닙니다.</b></p>
</div>
</details>

<details>
<summary style="font-size:1rem;"><b>SPA(Single Page Application, 단일 페이지 애플리케이션)</b></summary>
<div class="accordion-content">
    <p>처음에 <b>하나의 HTML 문서</b>를 로드해 두고, 이후 화면 전환은 <b>페이지를 통째로 다시 받지 않고</b> 브라우저에서 자바스크립트로 필요한 부분만 갱신하는 방식입니다.</p>
    <p>그래서 보통 서버는 "화면"을 계속 만들어 보내기보다, 화면에 필요한 <b>데이터(API 응답)</b>를 주고, 라우팅과 렌더링은 클라이언트에서 처리하는 형태가 많습니다. 장점은 화면 전환이 매끄럽고 앱처럼 빠르게 느껴질 수 있다는 점이고, 대신 <b>초기 로딩 부담</b>이나 <b>검색엔진 노출(SEO)·크롤링 대응</b> 같은 부분은 신경 써야 합니다.</p>
</div>
</details>

<details>
<summary style="font-size:1rem;"><b>서버 사이드 렌더링(SSR) & 클라이언트 사이드 렌더링(CSR)</b></summary>
<div class="accordion-content">
    <p>서버 사이드 렌더링은 <b>브라우저가 화면을 만들기 전에, 서버가 먼저 페이지의 HTML을 완성해서 내려주는 방식</b>입니다. 즉, 사용자가 URL로 들어오면 서버가 데이터까지 반영한 "완성된 HTML"을 만들어 응답하고, 브라우저는 그 HTML을 바로 그려서 화면을 보여줍니다.</p>
    <p>반대로 클라이언트 사이드 렌더링은 브라우저가 자바스크립트로 화면을 조립하는 방식이라, 초기에는 비교적 "빈 HTML + JS"를 받고 브라우저에서 렌더링이 진행됩니다.</p>
    <p>Spring MVC에서 <b>Thymeleaf 같은 템플릿 엔진으로 서버가 HTML을 만들어 내려주는 구조</b>가 대표적인 SSR 사례라고 보면 됩니다.</p>
    <h3>SSR이 유리한 경우</h3>
    <ul>
        <li><b>첫 화면이 빨리 보여야 할 때:</b> 서버가 HTML을 완성해서 보내므로, 사용자는 초기 화면을 더 빨리 “보는 느낌”을 받을 수 있습니다.</li>
        <li><b>SEO/공유 미리보기 같은 ‘문서 기반’ 노출이 중요할 때:</b> 처음부터 콘텐츠가 포함된 HTML을 받는 구조가 유리합니다.</li>
    </ul>
    <h3>CSR이 유리한 경우</h3>
    <ul>
        <li><b>대시보드/툴처럼 상호작용이 많은 앱:</b> 페이지 전환을 매번 서버에서 HTML로 만들 필요 없이, 브라우저에서 화면 일부만 갱신하므로 앱처럼 부드러운 UX를 만들기 좋습니다.</li>
        <li><b>로그인 후 사용자 개인 데이터 중심 화면:</b> 검색 노출보다 “빠른 화면 갱신, 풍부한 인터랙션”이 핵심이면 CSR이 맞는 경우가 많습니다.</li>
    </ul>
    <p><b>결론은 “SSR vs CSR”보다 “혼합 전략”이 흔합니다.</b> 요즘은 <b>초기 진입은 SSR/SSG로 빠르게 보여주고</b>, 이후 화면 전환·상호작용은 <b>클라이언트에서 처리</b>하는 식으로 절충하는 방식이 일반적입니다(하이드레이션/서버+클라이언트 컴포넌트 조합 등).</p>
</div>
</details>

<details>
<summary style="font-size:1rem;"><b>헬스체크(health check)</b></summary>
<div class="accordion-content">
    <p>애플리케이션이 "지금 정상 동작 중인지", 그리고 "트래픽을 받을 준비가 됐는지"를 외부에서 기계적으로 확인할 수 있게 해주는 점검 방식입니다. 보통은 아주 가벼운 HTTP 엔드포인트로 제공하고, 결과를 보고 장애를 감지하거나(모니터링), 트래픽을 차단하거나(로드밸런서), 필요하면 재시작(오케스트레이터) 같은 자동 조치를 하게 됩니다.</p>
    <h3>헬스체크를 하는 이유</h3>
    <ul>
        <li><b>장애를 빨리 감지</b>해서 운영/배포 자동화가 판단할 근거를 만들기 위해서입니다.(정상/비정상 신호)</li>
        <li><b>트래픽 제어</b>를 위해서입니다. 예를 들어 "서버는 떠 있지만 DB 연결이 안 된다"면, 사용자 요청은 받지 않게 막는게 낫습니다.(ready가 아님)</li>
        <li>컨테이너 환경에서는 보통 헬스체크를 Liveness / Readiness / Startup으로 나눠서 씁니다.</li>
    </ul>
</div>
</details>

<details>
<summary style="font-size:1rem;"><b>Spring Actuator(헬스체크와의 관계)</b></summary>
<div class="accordion-content">
    <p>Spring Boot Actuator는 <b>운영(Production) 환경에서 애플리케이션을 모니터링·관리하기 위한 기능들을 엔드포인트 형태로 제공하는 Spring Boot 모듈</b>입니다. HTTP 또는 JMX로 상태/지표를 노출할 수 있고, 기본 제공 엔드포인트도 여러 개 있습니다.</p>
    <ul>
        <li>대표적으로 <b>/actuator/health</b>가 헬스체크 엔드포인트이고, 전체 상태(status)와 구성요소별 상태(components)를 내려줄 수 있습니다.</li>
        <li>또한 Actuator는 <b>metrics 같은 지표 엔드포인트</b>를 제공하고, 내부적으로 <b>Micrometer 자동 설정</b>을 통해 Prometheus, Datadog 등 다양한 모니터링 시스템으로 내보낼 수 있게 연결해 줍니다.</li>
    </ul>
    <p>즉, "모니터링/헬스체크"는 <b>서비스가 살아있는 확인(health) + 관측 지표 제공(metrics 등)</b>을 한 패키지로 맡는 기술이 Actuator이다.</p>
</div>
</details>

 </div>
</details>


<!-- chapter -->
<details>
  <summary><span class="accordion-title">2️⃣ 프론트 개발 환경</span> <span class="indicator">펼치기</span></summary><div class="accordion-content">

<details>
<summary style="font-size:1rem;"><b>React 개념과 용도</b></summary>
<div class="accordion-content">
    <p>React는 <b>웹(그리고 React Native 같은 환경)에서 UI를 컴포넌트 단위로 만들고 렌더링하는 자바스크립트 라이브러리</b>입니다.</p>
    <p>라이브러리이지만 구분이 프레임워크인 이유는?<p>
    <ol>
        <li><b>React는 공식적으로 “라이브러리”</b>라서 용도를 UI 라이브러리로 쓰는 게 맞습니다.</li>
        <li>다만 실무에서 React로 앱을 만들 때 라우팅, 상태관리, 빌드/폴더 구조 같은 것까지 함께 묶어서 쓰다 보니, 스택 표의 “구분”을 크게 잡을 때 <b>관용적으로 프레임워크 칸에 넣는 경우</b>가 많습니다(분류 칸이 단순해서요).</li>
    </ol>
    <p>프레임워크와 라이브러리의 핵심 차이는 보통 <b>제어 흐름의 주도권(IOC, Inversion of Control)</b>입니다.</p>
    <ul>
        <li><b>라이브러리:</b> 내가 필요할 때 라이브러리 함수를 호출하고, 호출이 끝나면 제어가 다시 내 코드로 돌아옵니다.</li>
        <li><b>프레임워크:</b> 큰 실행 흐름을 프레임워크가 쥐고 있고, 내 코드는 정해진 지점에 “끼워 넣는” 형태로 <b>프레임워크가 내 코드를 호출</b>합니다.</li>
    </ul>
</div>
</details>

<details>
<summary style="font-size:1rem;"><b>TypeScript 개념과 용도</b></summary>
<div class="accordion-content">
    <p>TypeScript는 <b>자바스크립트에 “타입 문법”을 추가한 언어(자바스크립트의 상위집합)</b>이고, 최종적으로는 <b>일반 JavaScript로 컴파일(변환)되어 실행</b>됩니다.</p>
    <p>TypeScript의 용도는 타입 안정성이다. 이유는?</p>
    <p>용도가 <b>타입 안전성</b>인 이유는, TypeScript의 핵심 목표가 <b>코드가 실행되기 전에 정적 타입 검사로 타입 오류를 잡아주는 것</b>이라서입니다. 예를 들어 잘못된 프로퍼티 접근이나 함수 인자 타입 실수 같은 문제를 <b>개발 단계에서 미리 발견</b>하게 해 주고, 그 결과 자동완성·리팩토링 같은 도구 지원도 더 정확해집니다.</p>
    <p>정리하면, <b>“JavaScript로도 구현은 가능하지만, TypeScript는 타입을 통해 실행 전에 오류를 잡아 주고 자동완성·리팩토링 같은 도구 지원이 좋아서 유지보수성이 올라갑니다.”</b></p>
</div>
</details>

<details>
<summary style="font-size:1rem;"><b>프론트 기술 스택에 라우팅이 있는 이유</b></summary>
<div class="accordion-content">
    <p>사용자 입장에서 "URL이 바뀌면 다른 화면이 보이는" 내비게이션을 프론트에서 관리해야 하기 때문입니다. 특히 SPA에서는 페이지를 새로 받아오지 않으니, URL ↔ 화면(컴포넌트) 매핑을 해주는 라우터가 필요합니다.</p>
    <p><b>1. React Router DOM</b></p>
    <p>React 웹 앱에서 라우팅을 구현하는 라이브러리로, URL 경로에 따라 어떤 컴포넌트를 보여줄지 정하고, 브라우저의 뒤로가기/앞으로가기 같은 탐색도 자연스럽게 동작하도록 도와줍니다.</p>
    <p><b>2. React Router DOM을 사용한 이유</b></p>
    <p>React Router DOM을 선택하는 가장 흔한 이유는 “React에서 가장 표준적으로 쓰이는 라우팅 솔루션이고, 운영·유지보수 관점에서 리스크가 낮기 때문”입니다. 구체적으로는 보통 아래 이유가 큽니다.</p>
    <ul>
        <li>채택률/생태계가 압도적이라 레퍼런스가 많음</li>
        <li>React에 “자연스럽게” 붙는 설계(선언적 라우팅, 컴포넌트 기반)</li>
        <li>실전에서 필요한 기능이 기본으로 탄탄함</li>
        <li>데이터 라우팅(Loader/Action 등) 같은 확장 기능까지 커버</li>
        <li>유지보수/신뢰도(메인테이너·히스토리)</li>
    </ul>
    <p>참고로 “다른 걸” 선택하는 경우도 분명 있습니다. 예를 들어 타입 안전한 라우팅을 아주 강하게 가져가고 싶으면 TanStack Router가 매력적인 대안이 될 수 있고, 반대로 Next.js를 쓰면 라우팅이 프레임워크에 내장돼서 React Router DOM을 따로 둘 필요가 없기도 합니다.</p>
    <p><b>3. 용도가 SPA 라우팅인 이유</b></p>
    <p>용도가 “SPA 라우팅”인 이유는, React Router DOM이 서버에 새 HTML을 요청해서 페이지를 바꾸는 방식이 아니라 클라이언트에서 URL만 바꾸고 화면을 교체하는 “클라이언트 사이드 라우팅”을 제공하기 때문입니다.</p>
    <p><b>4. SPA 라우팅의 개념</b></p>
    <p>페이지 새로고침 없이 URL 변경(pushState/replaceState 등)과 화면 렌더링을 클라이언트에서 처리하는 방식입니다.</p>
</div>
</details>

<details>
<summary style="font-size:1rem;"><b>Next.js</b></summary>
<div class="accordion-content">
    <p>Next.js는 <b>React로 풀스택 웹 애플리케이션을 만들기 위한 프레임워크</b>입니다. React 컴포넌트로 UI를 만들고, Next.js가 그 위에서 <b>라우팅, 렌더링(SSR/정적 생성 등), 빌드·번들링 같은 개발/운영에 필요한 기능과 최적화</b>를 함께 제공합니다.</p>
    <ul>
        <li><b>파일 기반 라우팅:</b> 폴더/파일 구조로 URL 경로를 정의하는 방식(특히 App Router).</li>
        <li><b>서버 사이드 렌더링(SSR) 등 다양한 렌더링 전략 지원:</b> 페이지를 요청마다 서버에서 HTML로 만들어 주는 SSR 같은 방식을 공식적으로 지원합니다.</li>
        <li><b>React 개발에 필요한 툴링을 추상화/자동 설정:</b> 번들링·컴파일 등 설정 부담을 줄여 애플리케이션 개발에 집중하게 해줍니다.</li>
    </ul>
</div>
</details>

<details>
<summary style="font-size:1rem;"><b>Axios</b></summary>
<div class="accordion-content">
    <p>Axios(액시오스)는 <b>브라우저와 Node.js에서 HTTP 요청(GET/POST 등)을 보내기 위한 Promise 기반 HTTP 클라이언트 라이브러리</b>입니다. 요청/응답을 공통 API로 다루면서, <b>인터셉터(요청·응답 가로채기), 데이터 변환, 타임아웃/취소 처리</b> 같은 기능을 제공해 API 통신 코드를 깔끔하게 관리하는 데 자주 사용합니다.</p>
</div>
</details>

<details>
<summary style="font-size:1rem;"><b>Node.js 개념</b></summary>
<div class="accordion-content">
    <p>Node.js는 <b>브라우저 밖에서 JavaScript를 실행할 수 있게 해주는 런타임 환경</b>입니다. Chrome의 V8 엔진을 기반으로 하고, 서버 개발에 필요한 파일 시스템, 네트워크 같은 기능을 제공합니다.</p>
    <p>TypeScript로 만든 React 프로젝트에서 Node.js가 자주 같이 언급되는 이유</p>
    <ol>
        <li><b>Axios가 “브라우저 + Node.js” 모두에서 동작하는(isomorphic) HTTP 클라이언트</b>라서요.<br> Axios 문서 자체가 “node.js와 브라우저용”이라고 설명하고, 브라우저에서는 XHR을 쓰고 서버(Node.js)에서는 Node의 http 모듈을 쓴다고 명시합니다.<br> 즉, React 프론트에서는 보통 브라우저에서 Axios를 쓰지만, Axios가 원래 양쪽 환경을 지원하다 보니 Node.js가 설명에 같이 나옵니다.</li>
        <li>프론트엔드 개발 과정에서 <b>빌드/개발 서버/패키지 설치 같은 “도구”가 Node.js 위에서 돌아가서</b>입니다.<br>
        React 공식 문서도 Vite 같은 빌드 도구를 설치해서 개발 서버와 빌드를 한다고 안내하는데, 이런 도구들은 통상 Node 환경에서 실행됩니다.<br>
        그리고 TypeScript도 결국 JavaScript로 변환되어 실행되는데, 그 JavaScript가 실행되는 환경이 <b>브라우저일 수도, Node.js일 수도</b> 있다고 공식 사이트에서 설명합니다.</li>
    </ol>
    <p>정리하면, <b>React+TypeScript 앱 자체는 브라우저에서 실행되지만, 개발·빌드 도구와 일부 서버 사이드 코드에서 Node.js가 쓰이기 때문에</b> 기술 스택 설명에서 함께 등장하는 경우가 많습니다.</p>
</div>
</details>

<details>
<summary style="font-size:1rem;"><b>Tailwind CSS + 유틸리티 기반 스타일링이란?</b></summary>
<div class="accordion-content">
    <p>Tailwind CSS는 <b>utility-first(유틸리티 우선) CSS 프레임워크</b>로, 미리 준비된 작은 스타일 클래스들을 <b>마크업에 조합해서</b> 원하는 디자인을 만드는 방식입니다. “필요한 스타일을 HTML/JSX 안에서 클래스 조합으로 만든다”가 핵심입니다.</p>
    <p>유틸리티 기반 스타일링이란?</p>
    <p><b>한 클래스가 하나의 역할(예: 여백, 색, 정렬 등)을 담당하는 ‘단일 목적’ 클래스(utility class)</b>를 여러 개 붙여서 최종 UI를 만드는 방식입니다. 그래서 별도 CSS를 많이 작성하지 않고도, 클래스 조합만으로 화면을 빠르게 구성할 수 있습니다.</p>
</div>
</details>

  </div>
</details>


<!-- chapter -->
<details>
  <summary><span class="accordion-title">3️⃣ 데이터베이스 개발 환경</span> <span class="indicator">펼치기</span></summary><div class="accordion-content">

  <details>
    <summary style="font-size:1rem;"><b>H2 Database와 용도</b></summary>
    <div class="accordion-content">
        <p>H2는 <b>자바로 만들어진 경량 SQL 관계형 데이터베이스</b>로, 애플리케이션에 <b>내장(embedded)</b> 해서 쓰거나 서버 모드로도 사용할 수 있고 <b>메모리(in-memory) 또는 디스크(파일) 저장</b>을 지원합니다.</p>
        <p>"파일 기반" 용도의 의미</p>
        <p>“파일 기반”은 DB 데이터를 <b>메모리가 아니라 디스크의 파일로 저장</b>한다는 뜻입니다. 그래서 애플리케이션을 껐다 켜도 <b>데이터가 파일에 남아 유지(영속)</b> 됩니다. 반대로 <b>in-memory 방식</b>은 실행 중 메모리에만 올라가서, 종료하면 데이터가 사라지는 형태입니다.</p>
        <p>파일 기반 (./data/booktine) 의미</p>
        <p>./data/booktine 같은 표기는 <b>DB 파일을 저장할 위치(상대 경로)</b>를 의미합니다. 즉, 프로젝트(또는 실행 디렉터리) 기준으로 data 폴더 아래에 booktine 이름으로 DB 파일들이 만들어지고, 그 파일을 통해 데이터가 유지되는 구조라고 보시면 됩니다.</p>
    </div>
  </details>

  </div>
</details>


<!-- chapter -->
<details>
  <summary><span class="accordion-title">4️⃣ DevOps & 배포 개발 환경</span> <span class="indicator">펼치기</span></summary><div class="accordion-content">

  <details>
    <summary style="font-size:1rem;"><b>Docker</b></summary>
    <div class="accordion-content">
        <p>컨테이너를 만들고(이미지 빌드), 배포하고(레지스트리), 실행·관리하는(컨테이너 런) 과정을 지원하는 컨테이너 플랫폼/도구 생태계입니다. 컨테이너 이미지를 “코드+의존성”까지 포함한 실행 패키지로 만들어서, 서로 다른 환경 간 이식성을 높이는 데 목적이 있습니다.</p>
    </div>
  </details>


  </div>
</details>
