---
layout: default
title: "웹 개발 완전 정리"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>웹 개발 완전 정리 - 면접부터 개념까지</h2>
</section>

<!-- 면접 예상 질문 및 답변 -->
<details open>
  <summary><span class="accordion-title">면접 예상 질문 및 답변</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">
<details>
  <summary style="font-size:1rem;"><b>Q1: 웹의 동작 원리를 설명해주세요.</b></summary>
  <div class="accordion-content">
<p><b>A:</b> 사용자가 브라우저에서 URL을 입력하면 다음 과정을 거칩니다. ① DNS를 통해 도메인을 IP 주소로 변환 ② 브라우저가 해당 서버에 HTTP 요청 전송 ③ 서버가 HTML, CSS, JavaScript 파일을 응답으로 전송 ④ 브라우저가 파일들을 파싱하여 DOM 트리 구성 ⑤ CSS와 함께 렌더링하여 화면에 표시 ⑥ JavaScript 실행으로 동적 기능 제공. 이 모든 과정이 클라이언트-서버 구조로 이루어집니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q2: HTTP와 HTTPS의 차이점을 설명해주세요.</b></summary>
  <div class="accordion-content">
<p><b>A:</b> HTTP는 평문으로 데이터를 전송하는 프로토콜로 80번 포트를 사용하며, 데이터 노출 위험이 있습니다. HTTPS는 HTTP에 SSL/TLS 암호화를 추가한 것으로 443번 포트를 사용합니다. HTTPS는 데이터 암호화, 서버 인증, 데이터 무결성을 보장하며, SEO 이점과 브라우저 신뢰도 향상 효과도 있습니다. 현재는 보안과 성능상 HTTPS가 웹 표준입니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q3: GET과 POST의 차이점을 설명해주세요.</b></summary>
  <div class="accordion-content">
<p><b>A:</b> GET은 서버에서 데이터를 조회하는 메서드로 데이터를 URL 쿼리스트링에 포함시켜 전송합니다. 캐싱 가능하고 북마크 저장이 되지만 데이터 길이 제한과 보안 문제가 있습니다. POST는 서버에 데이터를 전송하는 메서드로 데이터를 요청 본문에 포함시킵니다. 데이터 길이 제한이 없고 상대적으로 안전하지만 캐싱되지 않습니다. GET은 멱등성을 가지지만 POST는 그렇지 않습니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q4: 쿠키와 세션의 차이점을 설명해주세요.</b></summary>
  <div class="accordion-content">
<p><b>A:</b> 쿠키는 클라이언트(브라우저)에 저장되는 작은 데이터로, 서버가 생성하여 클라이언트에 전송하고 클라이언트가 이후 요청 시 함께 전송합니다. 세션은 서버에 저장되는 사용자 정보로 세션 ID를 통해 관리됩니다. 쿠키는 브라우저에 저장되어 보안에 취약하지만 서버 부담이 적고, 세션은 서버에 저장되어 안전하지만 서버 메모리를 사용합니다. 쿠키는 만료시간 설정이 가능하고, 세션은 보통 브라우저 종료 시 삭제됩니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q5: REST API의 특징과 설계 원칙을 설명해주세요.</b></summary>
  <div class="accordion-content">
<p><b>A:</b> REST는 자원(Resource), 행위(HTTP Method), 표현(Representation)으로 구성되는 아키텍처 스타일입니다. 무상태성, 캐시 가능성, 계층화된 시스템, 통일된 인터페이스를 특징으로 합니다. 설계 원칙은 ① URI는 자원을 표현(명사 사용) ② HTTP 메서드로 행위를 표현(GET, POST, PUT, DELETE) ③ 상태코드로 결과 전달 ④ JSON 형태의 데이터 전송이 일반적입니다.</p>

<h3>Frontend 기술</h3>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q6: HTML 시맨틱 요소의 중요성을 설명해주세요.</b></summary>
  <div class="accordion-content">
<p><b>A:</b> 시맨틱 HTML은 의미를 가진 HTML 요소로 문서의 구조를 명확하게 표현합니다. header, nav, main, article, section, aside, footer 등이 대표적입니다. 중요성은 ① SEO 향상: 검색엔진이 내용을 더 잘 이해 ② 접근성 개선: 스크린 리더 등 보조기술의 이해도 향상 ③ 코드 가독성: 개발자가 구조를 쉽게 파악 ④ 유지보수성: 명확한 구조로 수정이 용이합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q7: CSS의 Box Model을 설명해주세요.</b></summary>
  <div class="accordion-content">
<p><b>A:</b> CSS Box Model은 모든 HTML 요소를 직사각형 박스로 표현하는 개념입니다. 안쪽부터 ① Content: 실제 내용이 들어가는 영역 ② Padding: 내용과 테두리 사이의 여백 ③ Border: 테두리 ④ Margin: 요소 간의 외부 여백으로 구성됩니다. box-sizing 속성으로 박스 크기 계산 방식을 변경할 수 있으며, content-box(기본값)와 border-box가 있습니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q8: JavaScript의 호이스팅에 대해 설명해주세요.</b></summary>
  <div class="accordion-content">
<p><b>A:</b> 호이스팅은 변수와 함수 선언이 해당 스코프의 최상단으로 끌어올려지는 것처럼 동작하는 JavaScript의 특성입니다. var 변수는 undefined로 초기화되어 호이스팅되고, let/const는 호이스팅되지만 초기화되지 않아 일시적 사각지대(TDZ)가 발생합니다. 함수 선언문은 전체가 호이스팅되어 선언 전에도 호출 가능하지만, 함수 표현식은 변수 호이스팅 규칙을 따릅니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q9: 클로저(Closure)에 대해 설명해주세요.</b></summary>
  <div class="accordion-content">
<p><b>A:</b> 클로저는 함수가 선언될 때의 렉시컬 환경(스코프)을 기억하여, 함수가 선언된 스코프 밖에서 실행되어도 그 환경의 변수에 접근할 수 있는 기능입니다. 외부 함수의 변수를 내부 함수에서 참조할 때 발생하며, 외부 함수 실행이 끝나도 내부 함수가 외부 함수의 변수에 접근 가능합니다. 데이터 은닉, 모듈 패턴, 콜백 함수 등에 활용됩니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q10: Promise와 async/await의 차이점을 설명해주세요.</b></summary>
  <div class="accordion-content">
<p><b>A:</b> Promise는 비동기 작업의 완료 또는 실패를 나타내는 객체로, pending, fulfilled, rejected 상태를 가집니다. then(), catch(), finally() 메서드 체이닝으로 처리하지만 여전히 콜백 지옥이 발생할 수 있습니다. async/await는 Promise를 더 동기적으로 작성할 수 있게 해주는 문법입니다. async 함수는 항상 Promise를 반환하고, await는 Promise가 resolve될 때까지 기다립니다. 코드 가독성이 크게 향상되고 try-catch로 간단한 에러 처리가 가능합니다.</p>

<h3>Backend 및 서버</h3>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q11: MVC 패턴에 대해 설명해주세요.</b></summary>
  <div class="accordion-content">
<p><b>A:</b> MVC는 애플리케이션을 Model, View, Controller로 분리하는 아키텍처 패턴입니다. Model은 데이터와 비즈니스 로직을 담당하고, View는 사용자 인터페이스를 담당하며, Controller는 사용자 입력을 처리하고 Model과 View를 연결합니다. 관심사 분리로 코드 재사용성과 유지보수성이 향상되고, 개발자들 간 역할 분담이 명확해집니다. Spring MVC, Django, Express 등에서 이 패턴을 사용합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q12: JWT(JSON Web Token)에 대해 설명해주세요.</b></summary>
  <div class="accordion-content">
<p><b>A:</b> JWT는 JSON 객체를 안전하게 전송하기 위한 토큰 기반 인증 방식입니다. Header(알고리즘 정보), Payload(사용자 정보), Signature(서명)로 구성되며, 점(.)으로 구분됩니다. 서버에서 비밀키로 서명하여 위변조를 방지합니다. Stateless하여 서버 부담이 적고 확장성이 좋지만, 토큰 크기가 크고 만료 전까지 무효화하기 어렵다는 단점이 있습니다. 주로 API 인증에 사용됩니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q13: 데이터베이스 연결 풀에 대해 설명해주세요.</b></summary>
  <div class="accordion-content">
<p><b>A:</b> 커넥션 풀은 데이터베이스 연결을 미리 생성하여 풀에 저장하고 재사용하는 기법입니다. 매번 연결을 생성/해제하는 오버헤드를 줄이고, 동시 연결 수를 제한하여 DB 서버 부하를 관리합니다. 적절한 풀 크기 설정이 중요한데, 너무 작으면 대기시간이 증가하고 너무 크면 메모리 낭비가 발생합니다. HikariCP, Apache DBCP 등의 라이브러리를 사용하며, 최대 연결 수, 최소 연결 수, 연결 대기 시간 등을 설정할 수 있습니다.</p>

<h3>성능 및 보안</h3>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q14: 웹 성능 최적화 방법을 설명해주세요.</b></summary>
  <div class="accordion-content">
<p><b>A:</b> 프론트엔드 최적화로는 ① 이미지 최적화(압축, WebP 포맷, lazy loading) ② 코드 분할과 번들 최적화 ③ CSS/JS 압축 및 최소화 ④ CDN 사용 ⑤ 브라우저 캐싱 활용이 있습니다. 백엔드 최적화로는 ① 데이터베이스 쿼리 최적화 ② 인덱스 활용 ③ 캐싱 전략(Redis, Memcached) ④ 로드 밸런싱 ⑤ 비동기 처리가 있습니다. Core Web Vitals(LCP, FID, CLS) 지표를 모니터링하여 사용자 경험을 개선합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q15: CORS에 대해 설명해주세요.</b></summary>
  <div class="accordion-content">
<p><b>A:</b> CORS(Cross-Origin Resource Sharing)는 웹 브라우저의 동일 출처 정책을 완화하여 다른 도메인의 리소스에 접근할 수 있게 해주는 메커니즘입니다. 브라우저는 보안상 같은 프로토콜, 도메인, 포트의 리소스만 접근을 허용합니다. CORS는 서버에서 Access-Control-Allow-Origin 등의 헤더를 설정하여 특정 도메인의 접근을 허용합니다. Preflight 요청으로 실제 요청 전에 서버 정책을 확인하며, 잘못 설정하면 보안 위험이 있으므로 필요한 도메인만 허용해야 합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q16: 주요 웹 보안 취약점과 대응 방법을 설명해주세요.</b></summary>
  <div class="accordion-content">
<p><b>A:</b> 주요 취약점으로는 ① XSS: 악성 스크립트 삽입 → 입력값 검증과 출력값 인코딩으로 방지 ② CSRF: 의도하지 않은 요청 → CSRF 토큰과 SameSite 쿠키로 방지 ③ SQL Injection: 악의적 SQL 삽입 → Prepared Statement와 입력값 검증으로 방지 ④ 인증 취약점 → 강력한 비밀번호 정책, HTTPS 사용, 세션 타임아웃 설정으로 대응합니다. 정기적인 보안 감사와 최신 패치 적용도 중요합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q17: SPA와 SSR의 차이점과 장단점을 설명해주세요.</b></summary>
  <div class="accordion-content">
<p><b>A:</b> SPA(Single Page Application)는 하나의 HTML 페이지에서 JavaScript로 동적으로 콘텐츠를 변경하는 방식입니다. 빠른 사용자 경험, 서버 부하 감소가 장점이지만 초기 로딩 시간이 길고 SEO에 불리합니다. SSR(Server-Side Rendering)은 서버에서 HTML을 완전히 렌더링하여 전송하는 방식입니다. 빠른 초기 로딩과 SEO 친화적이지만 서버 부하가 크고 페이지 전환 시 새로고침이 필요합니다. 현재는 Next.js, Nuxt.js 같은 프레임워크로 하이브리드 방식을 많이 사용합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q18: 캐싱 전략에 대해 설명해주세요.</b></summary>
  <div class="accordion-content">
<p><b>A:</b> 캐싱은 자주 사용되는 데이터를 빠른 저장소에 임시 보관하여 성능을 향상시키는 기법입니다. ① Cache-Aside: 애플리케이션이 캐시를 직접 관리 ② Write-Through: 캐시와 DB에 동시에 쓰기 ③ Write-Behind: 캐시에 먼저 쓰고 나중에 DB 반영 ④ Write-Around: 캐시를 거치지 않고 DB에 직접 쓰기가 있습니다. TTL 설정, 캐시 무효화 전략, 캐시 키 설계, 메모리 사용량 관리 등을 고려해야 합니다.</p>

<h3>최신 기술 동향</h3>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q19: 마이크로서비스 아키텍처의 특징을 설명해주세요.</b></summary>
  <div class="accordion-content">
<p><b>A:</b> 마이크로서비스는 애플리케이션을 작고 독립적인 서비스들로 분해하는 아키텍처 패턴입니다. 각 서비스는 특정 비즈니스 기능을 담당하고, 독립적으로 배포 및 확장 가능합니다. 장점으로는 독립적 개발/배포, 기술 다양성, 확장성, 장애 격리가 있습니다. 단점으로는 복잡성 증가, 네트워크 통신 오버헤드, 분산 시스템 관리의 어려움이 있습니다. API Gateway, 서비스 디스커버리, 로드 밸런싱 등의 지원 도구가 필요합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q20: PWA(Progressive Web App)의 특징을 설명해주세요.</b></summary>
  <div class="accordion-content">
<p><b>A:</b> PWA는 웹 기술로 개발되지만 네이티브 앱과 같은 사용자 경험을 제공하는 웹 애플리케이션입니다. Service Worker를 통한 오프라인 지원, 웹 매니페스트로 홈 화면 추가, 푸시 알림, 백그라운드 동기화 등의 기능을 제공합니다. 반응형 디자인, HTTPS 필수, 앱과 같은 인터랙션이 특징입니다. 하나의 코드베이스로 여러 플랫폼 배포 가능하고 앱 스토어 승인 없이 업데이트할 수 있지만, 일부 네이티브 기능 제약과 브라우저 지원 차이가 있습니다.</p>

<p>---</p>
  </div>
</details>

  </div>
</details>

<!-- 개념 정리: 전체를 HTML로 상세 변환 -->
<details>
  <summary><span class="accordion-title">웹 개발 개념 정리 (전체)</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">
<h2>웹 개발 기초 개념</h2>

<h2>1. 웹의 기본 구조</h2>

<h3>1.1 웹의 동작 원리</h3>
<p>웹은 클라이언트-서버 모델을 기반으로 동작합니다.</p>

<h4>기본 흐름</h4>
<ol>
<li><b>URL 입력</b> → 브라우저 주소창에 URL 입력</li>
<li><b>DNS 조회</b> → 도메인명을 IP 주소로 변환</li>
<li><b>HTTP 요청</b> → 서버에 리소스 요청</li>
<li><b>서버 처리</b> → 요청 처리 후 응답 생성</li>
<li><b>HTTP 응답</b> → HTML, CSS, JS 파일 전송</li>
<li><b>렌더링</b> → 브라우저에서 페이지 렌더링</li>
</ol>

<h3>1.2 프로토콜</h3>
<h4>HTTP (HyperText Transfer Protocol)</h4>
<ul>
<li>웹에서 데이터를 주고받는 프로토콜</li>
<li>무상태성(Stateless): 각 요청이 독립적</li>
<li>요청-응답 구조</li>
</ul>

<h4>HTTPS (HTTP Secure)</h4>
<ul>
<li>HTTP에 SSL/TLS 보안 계층 추가</li>
<li>데이터 암호화, 인증, 무결성 보장</li>
<li>443 포트 사용</li>
</ul>

<h3>1.3 HTTP 메서드</h3>
<ul>
<li><b>GET</b>: 리소스 조회</li>
<li><b>POST</b>: 데이터 전송/생성</li>
<li><b>PUT</b>: 리소스 전체 수정</li>
<li><b>PATCH</b>: 리소스 부분 수정</li>
<li><b>DELETE</b>: 리소스 삭제</li>
</ul>

<h3>1.4 HTTP 상태 코드</h3>
<ul>
<li><b>2xx</b>: 성공 (200 OK, 201 Created)</li>
<li><b>3xx</b>: 리다이렉션 (301 Moved Permanently)</li>
<li><b>4xx</b>: 클라이언트 오류 (404 Not Found)</li>
<li><b>5xx</b>: 서버 오류 (500 Internal Server Error)</li>
</ul>

<h2>2. Frontend 개발</h2>

<h3>2.1 HTML (HyperText Markup Language)</h3>
<p>웹페이지의 구조와 콘텐츠를 정의하는 마크업 언어입니다.</p>

<h4>HTML 기본 구조</h4>
<pre><code class="language-html">
&lt;!DOCTYPE html&gt;
&lt;html lang=&quot;ko&quot;&gt;
&lt;head&gt;
    &lt;meta charset=&quot;UTF-8&quot;&gt;
    &lt;meta name=&quot;viewport&quot; content=&quot;width=device-width, initial-scale=1.0&quot;&gt;
    &lt;title&gt;페이지 제목&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;h1&gt;메인 제목&lt;/h1&gt;
    &lt;p&gt;문단 내용&lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt;
</code></pre>

<h4>시맨틱 HTML</h4>
<p>의미를 가진 HTML 요소로 구조를 명확하게 표현합니다.</p>
<ul>
<li><code><header></code>: 페이지/섹션 헤더</li>
<li><code><nav></code>: 내비게이션</li>
<li><code><main></code>: 주요 콘텐츠</li>
<li><code><article></code>: 독립적 콘텐츠</li>
<li><code><section></code>: 문서 구역</li>
<li><code><aside></code>: 사이드바</li>
<li><code><footer></code>: 페이지/섹션 푸터</li>
</ul>

<h3>2.2 CSS (Cascading Style Sheets)</h3>
<p>HTML 요소의 스타일을 정의하는 언어입니다.</p>

<h4>CSS 선택자</h4>
<pre><code class="language-css">
/* 요소 선택자 */
h1 { color: blue; }

/* 클래스 선택자 */
.header { background: red; }

/* ID 선택자 */
#main { width: 100%; }

/* 속성 선택자 */
input[type=&quot;text&quot;] { border: 1px solid gray; }
</code></pre>

<h4>Box Model</h4>
<p>모든 HTML 요소는 박스 모델을 가집니다.</p>
<ul>
<li><b>Content</b>: 실제 내용</li>
<li><b>Padding</b>: 내용과 테두리 사이 여백</li>
<li><b>Border</b>: 테두리</li>
<li><b>Margin</b>: 요소 간 외부 여백</li>
</ul>

<h4>CSS 레이아웃</h4>
<p><b>Flexbox</b>: 1차원 레이아웃</p>
<pre><code class="language-css">
.container {
    display: flex;
    justify-content: center;
    align-items: center;
}
</code></pre>

<p><b>Grid</b>: 2차원 레이아웃</p>
<pre><code class="language-css">
.grid {
    display: grid;
    grid-template-columns: 1fr 2fr 1fr;
    gap: 20px;
}
</code></pre>

<h3>2.3 JavaScript</h3>
<p>웹페이지에 동적 기능을 추가하는 프로그래밍 언어입니다.</p>

<h4>기본 문법</h4>
<pre><code class="language-javascript">
// 변수 선언
let name = &quot;홍길동&quot;;
const age = 25;

// 함수 선언
function greet(name) {
    return `안녕하세요, ${name}님!`;
}

// 화살표 함수
const add = (a, b) =&gt; a + b;
</code></pre>

<h4>DOM 조작</h4>
<pre><code class="language-javascript">
// 요소 선택
const element = document.getElementById(&#x27;myId&#x27;);
const elements = document.querySelectorAll(&#x27;.myClass&#x27;);

// 내용 변경
element.textContent = &#x27;새로운 내용&#x27;;
element.innerHTML = &#x27;&lt;strong&gt;강조된 내용&lt;/strong&gt;&#x27;;

// 이벤트 처리
element.addEventListener(&#x27;click&#x27;, function() {
    alert(&#x27;클릭되었습니다!&#x27;);
});
</code></pre>

<h4>비동기 처리</h4>
<pre><code class="language-javascript">
// Promise
fetch(&#x27;/api/data&#x27;)
    .then(response =&gt; response.json())
    .then(data =&gt; console.log(data))
    .catch(error =&gt; console.error(error));

// async/await
async function fetchData() {
    try {
        const response = await fetch(&#x27;/api/data&#x27;);
        const data = await response.json();
        return data;
    } catch (error) {
        console.error(error);
    }
}
</code></pre>

<h3>2.4 프론트엔드 프레임워크</h3>

<h4>React</h4>
<p>컴포넌트 기반 JavaScript 라이브러리입니다.</p>

<p><b>특징</b>:</p>
<ul>
<li>Virtual DOM</li>
<li>단방향 데이터 흐름</li>
<li>JSX 문법</li>
<li>Hooks (useState, useEffect 등)</li>
</ul>

<pre><code class="language-javascript">
import React, { useState } from &#x27;react&#x27;;

function Counter() {
    const [count, setCount] = useState(0);

    return (
        &lt;div&gt;
            &lt;p&gt;Count: {count}&lt;/p&gt;
            &lt;button onClick={() =&gt; setCount(count + 1)}&gt;
                증가
            &lt;/button&gt;
        &lt;/div&gt;
    );
}
</code></pre>

<h4>Vue.js</h4>
<p>점진적 도입이 가능한 프레임워크입니다.</p>

<p><b>특징</b>:</p>
<ul>
<li>반응형 데이터 바인딩</li>
<li>템플릿 문법</li>
<li>컴포넌트 기반</li>
<li>낮은 학습 곡선</li>
</ul>

<h2>3. Backend 개발</h2>

<h3>3.1 서버의 역할</h3>
<ul>
<li>클라이언트 요청 처리</li>
<li>비즈니스 로직 실행</li>
<li>데이터베이스 연동</li>
<li>API 제공</li>
</ul>

<h3>3.2 Node.js</h3>
<p>Chrome V8 엔진 기반의 JavaScript 런타임입니다.</p>

<h4>특징</h4>
<ul>
<li>이벤트 기반 비동기 I/O</li>
<li>단일 스레드 (이벤트 루프)</li>
<li>npm 생태계</li>
<li>크로스 플랫폼</li>
</ul>

<h4>Express.js</h4>
<p>Node.js를 위한 웹 프레임워크입니다.</p>

<pre><code class="language-javascript">
const express = require(&#x27;express&#x27;);
const app = express();

// 미들웨어
app.use(express.json());

// 라우트
app.get(&#x27;/api/users&#x27;, (req, res) =&gt; {
    res.json({ users: [] });
});

app.post(&#x27;/api/users&#x27;, (req, res) =&gt; {
    const user = req.body;
    // 사용자 생성 로직
    res.status(201).json(user);
});

app.listen(3000, () =&gt; {
    console.log(&#x27;서버가 3000번 포트에서 실행 중입니다.&#x27;);
});
</code></pre>

<h3>3.3 데이터베이스 연동</h3>
<h4>관계형 데이터베이스 (MySQL, PostgreSQL)</h4>
<pre><code class="language-javascript">
const mysql = require(&#x27;mysql2&#x27;);

const connection = mysql.createConnection({
    host: &#x27;localhost&#x27;,
    user: &#x27;user&#x27;,
    password: &#x27;password&#x27;,
    database: &#x27;mydb&#x27;
});

// 데이터 조회
app.get(&#x27;/users&#x27;, async (req, res) =&gt; {
    const [rows] = await connection.execute(&#x27;SELECT * FROM users&#x27;);
    res.json(rows);
});
</code></pre>

<h4>NoSQL (MongoDB)</h4>
<pre><code class="language-javascript">
const mongoose = require(&#x27;mongoose&#x27;);

const userSchema = new mongoose.Schema({
    name: String,
    email: String,
    createdAt: { type: Date, default: Date.now }
});

const User = mongoose.model(&#x27;User&#x27;, userSchema);

// 사용자 생성
app.post(&#x27;/users&#x27;, async (req, res) =&gt; {
    const user = new User(req.body);
    await user.save();
    res.status(201).json(user);
});
</code></pre>

<h3>3.4 API 설계</h3>

<h4>RESTful API</h4>
<pre><code class="language-javascript">
// 리소스 기반 URL 설계
GET    /api/users      // 사용자 목록 조회
POST   /api/users      // 사용자 생성
GET    /api/users/:id  // 특정 사용자 조회
PUT    /api/users/:id  // 사용자 전체 수정
DELETE /api/users/:id  // 사용자 삭제
</code></pre>

<h4>GraphQL</h4>
<p>단일 엔드포인트에서 필요한 데이터만 요청하는 쿼리 언어입니다.</p>

<pre><code class="language-javascript">
const typeDefs = `
    type User {
        id: ID!
        name: String!
        email: String!
    }

    type Query {
        users: [User!]!
        user(id: ID!): User
    }
`;

const resolvers = {
    Query: {
        users: () =&gt; User.find(),
        user: (_, { id }) =&gt; User.findById(id)
    }
};
</code></pre>

<h2>4. 웹 보안</h2>

<h3>4.1 주요 보안 취약점</h3>

<h4>XSS (Cross-Site Scripting)</h4>
<p>악성 스크립트를 웹페이지에 삽입하는 공격입니다.</p>

<p><b>방어 방법</b>:</p>
<ul>
<li>입력값 검증 및 필터링</li>
<li>출력값 HTML 인코딩</li>
<li>CSP(Content Security Policy) 적용</li>
</ul>

<pre><code class="language-javascript">
// 입력값 검증
function sanitizeInput(input) {
    return input.replace(/&lt;script\b[^&lt;]*(?:(?!&lt;\/script&gt;)&lt;[^&lt;]*)*&lt;\/script&gt;/gi, &#x27;&#x27;);
}

// HTML 인코딩
function escapeHtml(text) {
    return text
        .replace(/&amp;/g, &#x27;&amp;amp;&#x27;)
        .replace(/&lt;/g, &#x27;&amp;lt;&#x27;)
        .replace(/&gt;/g, &#x27;&amp;gt;&#x27;)
        .replace(/&quot;/g, &#x27;&amp;quot;&#x27;)
        .replace(/&#x27;/g, &#x27;&amp;#39;&#x27;);
}
</code></pre>

<h4>CSRF (Cross-Site Request Forgery)</h4>
<p>사용자 모르게 의도하지 않은 요청을 보내는 공격입니다.</p>

<p><b>방어 방법</b>:</p>
<ul>
<li>CSRF 토큰 사용</li>
<li>SameSite 쿠키 설정</li>
<li>Referer 헤더 검증</li>
</ul>

<pre><code class="language-javascript">
// CSRF 토큰 생성 및 검증
const csrf = require(&#x27;csurf&#x27;);
const csrfProtection = csrf({ cookie: true });

app.use(csrfProtection);

app.get(&#x27;/form&#x27;, (req, res) =&gt; {
    res.render(&#x27;form&#x27;, { csrfToken: req.csrfToken() });
});
</code></pre>

<h4>SQL Injection</h4>
<p>악의적인 SQL 코드를 삽입하여 데이터베이스를 조작하는 공격입니다.</p>

<p><b>방어 방법</b>:</p>
<ul>
<li>Prepared Statement 사용</li>
<li>입력값 검증</li>
<li>최소 권한 원칙</li>
</ul>

<pre><code class="language-javascript">
// 취약한 코드 (하지 말 것)
const query = `SELECT * FROM users WHERE id = &#x27;${userId}&#x27;`;

// 안전한 코드 (Prepared Statement)
const query = &#x27;SELECT * FROM users WHERE id = ?&#x27;;
connection.execute(query, [userId]);
</code></pre>

<h3>4.2 인증과 인가</h3>

<h4>세션 기반 인증</h4>
<pre><code class="language-javascript">
const session = require(&#x27;express-session&#x27;);

app.use(session({
    secret: &#x27;your-secret-key&#x27;,
    resave: false,
    saveUninitialized: false,
    cookie: {
        secure: false, // HTTPS에서는 true
        maxAge: 1000 * 60 * 60 // 1시간
    }
}));

// 로그인
app.post(&#x27;/login&#x27;, (req, res) =&gt; {
    // 사용자 인증 로직
    if (isValidUser) {
        req.session.userId = user.id;
        res.json({ message: &#x27;로그인 성공&#x27; });
    }
});
</code></pre>

<h4>JWT 기반 인증</h4>
<pre><code class="language-javascript">
const jwt = require(&#x27;jsonwebtoken&#x27;);

// 토큰 생성
app.post(&#x27;/login&#x27;, (req, res) =&gt; {
    // 사용자 인증 로직
    if (isValidUser) {
        const token = jwt.sign(
            { userId: user.id, email: user.email },
            &#x27;your-secret-key&#x27;,
            { expiresIn: &#x27;1h&#x27; }
        );
        res.json({ token });
    }
});

// 토큰 검증 미들웨어
function authenticateToken(req, res, next) {
    const authHeader = req.headers[&#x27;authorization&#x27;];
    const token = authHeader &amp;&amp; authHeader.split(&#x27; &#x27;)[1];

    if (!token) {
        return res.sendStatus(401);
    }

    jwt.verify(token, &#x27;your-secret-key&#x27;, (err, user) =&gt; {
        if (err) return res.sendStatus(403);
        req.user = user;
        next();
    });
}

// 보호된 라우트
app.get(&#x27;/protected&#x27;, authenticateToken, (req, res) =&gt; {
    res.json({ message: &#x27;인증된 사용자만 접근 가능&#x27; });
});
</code></pre>

<h2>5. 웹 성능 최적화</h2>

<h3>5.1 프론트엔드 최적화</h3>

<h4>이미지 최적화</h4>
<pre><code class="language-html">
&lt;!-- 반응형 이미지 --&gt;
&lt;picture&gt;
    &lt;source media=&quot;(max-width: 768px)&quot; srcset=&quot;image-mobile.webp&quot;&gt;
    &lt;source media=&quot;(min-width: 769px)&quot; srcset=&quot;image-desktop.webp&quot;&gt;
    &lt;img src=&quot;image-fallback.jpg&quot; alt=&quot;설명&quot;&gt;
&lt;/picture&gt;

&lt;!-- 지연 로딩 --&gt;
&lt;img src=&quot;image.jpg&quot; alt=&quot;설명&quot; loading=&quot;lazy&quot;&gt;
</code></pre>

<h4>코드 분할 (Code Splitting)</h4>
<pre><code class="language-javascript">
// React에서 동적 import
const LazyComponent = React.lazy(() =&gt; import(&#x27;./LazyComponent&#x27;));

function App() {
    return (
        &lt;React.Suspense fallback={&lt;div&gt;Loading...&lt;/div&gt;}&gt;
            &lt;LazyComponent /&gt;
        &lt;/React.Suspense&gt;
    );
}

// Webpack 코드 분할
import(/* webpackChunkName: &quot;my-chunk&quot; */ &#x27;./myModule&#x27;)
    .then(module =&gt; {
        // 모듈 사용
    });
</code></pre>

<h4>브라우저 캐싱</h4>
<pre><code class="language-javascript">
// Express.js에서 정적 파일 캐싱
app.use(&#x27;/static&#x27;, express.static(&#x27;public&#x27;, {
    maxAge: &#x27;1d&#x27;, // 1일 캐싱
    etag: true
}));

// 캐시 컨트롤 헤더 설정
app.get(&#x27;/api/data&#x27;, (req, res) =&gt; {
    res.set(&#x27;Cache-Control&#x27;, &#x27;public, max-age=3600&#x27;); // 1시간 캐싱
    res.json(data);
});
</code></pre>

<h3>5.2 백엔드 최적화</h3>

<h4>데이터베이스 최적화</h4>
<pre><code class="language-sql">
-- 인덱스 생성
CREATE INDEX idx_user_email ON users(email);
CREATE INDEX idx_post_created ON posts(created_at);

-- 쿼리 최적화
SELECT u.name, p.title 
FROM users u
INNER JOIN posts p ON u.id = p.user_id
WHERE u.active = 1
ORDER BY p.created_at DESC
LIMIT 10;
</code></pre>

<h4>캐싱 전략</h4>
<pre><code class="language-javascript">
const redis = require(&#x27;redis&#x27;);
const client = redis.createClient();

// Cache-Aside 패턴
async function getUser(userId) {
    // 캐시에서 먼저 확인
    const cachedUser = await client.get(`user:${userId}`);
    if (cachedUser) {
        return JSON.parse(cachedUser);
    }

    // 캐시에 없으면 DB에서 조회
    const user = await User.findById(userId);
    
    // 캐시에 저장 (TTL: 1시간)
    await client.setex(`user:${userId}`, 3600, JSON.stringify(user));
    
    return user;
}
</code></pre>

<h4>API 응답 최적화</h4>
<pre><code class="language-javascript">
// 페이지네이션
app.get(&#x27;/api/posts&#x27;, async (req, res) =&gt; {
    const page = parseInt(req.query.page) || 1;
    const limit = parseInt(req.query.limit) || 10;
    const offset = (page - 1) * limit;

    const posts = await Post.find()
        .limit(limit)
        .skip(offset)
        .sort({ createdAt: -1 });

    const totalCount = await Post.countDocuments();
    const totalPages = Math.ceil(totalCount / limit);

    res.json({
        posts,
        pagination: {
            currentPage: page,
            totalPages,
            totalCount,
            hasNext: page &lt; totalPages
        }
    });
});

// 필드 선택 (Projection)
app.get(&#x27;/api/users&#x27;, async (req, res) =&gt; {
    const users = await User.find({}, &#x27;name email createdAt&#x27;); // 필요한 필드만 선택
    res.json(users);
});
</code></pre>

<h2>6. 개발 도구와 환경</h2>

<h3>6.1 패키지 관리자</h3>

<h4>npm (Node Package Manager)</h4>
<pre><code class="language-bash">
# 패키지 설치
npm install express
npm install -D nodemon  # 개발 의존성

# 스크립트 실행
npm run dev
npm run build
npm test

# package.json
{
  &quot;scripts&quot;: {
    &quot;dev&quot;: &quot;nodemon server.js&quot;,
    &quot;build&quot;: &quot;webpack --mode production&quot;,
    &quot;test&quot;: &quot;jest&quot;
  }
}
</code></pre>

<h3>6.2 빌드 도구</h3>

<h4>Webpack</h4>
<p>모듈 번들러로 여러 파일을 하나로 묶어주는 도구입니다.</p>

<pre><code class="language-javascript">
// webpack.config.js
const path = require(&#x27;path&#x27;);
const HtmlWebpackPlugin = require(&#x27;html-webpack-plugin&#x27;);

module.exports = {
    entry: &#x27;./src/index.js&#x27;,
    output: {
        path: path.resolve(__dirname, &#x27;dist&#x27;),
        filename: &#x27;bundle.[contenthash].js&#x27;,
        clean: true
    },
    module: {
        rules: [
            {
                test: /\.css$/,
                use: [&#x27;style-loader&#x27;, &#x27;css-loader&#x27;]
            },
            {
                test: /\.(png|jpg|gif)$/,
                type: &#x27;asset/resource&#x27;
            }
        ]
    },
    plugins: [
        new HtmlWebpackPlugin({
            template: &#x27;./src/index.html&#x27;
        })
    ]
};
</code></pre>

<h4>Vite</h4>
<p>빠른 빌드 도구로 개발 서버가 매우 빠릅니다.</p>

<pre><code class="language-javascript">
// vite.config.js
import { defineConfig } from &#x27;vite&#x27;;
import react from &#x27;@vitejs/plugin-react&#x27;;

export default defineConfig({
    plugins: [react()],
    build: {
        outDir: &#x27;dist&#x27;,
        sourcemap: true
    },
    server: {
        port: 3000,
        open: true
    }
});
</code></pre>

<h3>6.3 테스팅</h3>

<h4>Jest (JavaScript 테스트 프레임워크)</h4>
<pre><code class="language-javascript">
// math.js
function add(a, b) {
    return a + b;
}

function multiply(a, b) {
    return a * b;
}

module.exports = { add, multiply };

// math.test.js
const { add, multiply } = require(&#x27;./math&#x27;);

test(&#x27;2 + 3 equals 5&#x27;, () =&gt; {
    expect(add(2, 3)).toBe(5);
});

test(&#x27;3 * 4 equals 12&#x27;, () =&gt; {
    expect(multiply(3, 4)).toBe(12);
});
</code></pre>

<h4>React Testing Library</h4>
<pre><code class="language-javascript">
import { render, screen, fireEvent } from &#x27;@testing-library/react&#x27;;
import Counter from &#x27;./Counter&#x27;;

test(&#x27;counter increments when button is clicked&#x27;, () =&gt; {
    render(&lt;Counter /&gt;);
    
    const button = screen.getByText(&#x27;증가&#x27;);
    const count = screen.getByText(&#x27;Count: 0&#x27;);
    
    fireEvent.click(button);
    
    expect(screen.getByText(&#x27;Count: 1&#x27;)).toBeInTheDocument();
});
</code></pre>

<h2>7. 현대 웹 개발 트렌드</h2>

<h3>7.1 JAMstack</h3>
<p>JavaScript, APIs, Markup으로 구성된 현대적 웹 아키텍처입니다.</p>

<h4>Next.js (React 기반)</h4>
<pre><code class="language-javascript">
// pages/index.js
export default function Home({ posts }) {
    return (
        &lt;div&gt;
            &lt;h1&gt;블로그&lt;/h1&gt;
            {posts.map(post =&gt; (
                &lt;article key={post.id}&gt;
                    &lt;h2&gt;{post.title}&lt;/h2&gt;
                    &lt;p&gt;{post.excerpt}&lt;/p&gt;
                &lt;/article&gt;
            ))}
        &lt;/div&gt;
    );
}

// Static Site Generation (SSG)
export async function getStaticProps() {
    const posts = await fetchPosts();
    
    return {
        props: { posts },
        revalidate: 60 // 1분마다 재생성
    };
}
</code></pre>

<h4>Nuxt.js (Vue 기반)</h4>
<pre><code class="language-javascript">
// pages/index.vue
&lt;template&gt;
  &lt;div&gt;
    &lt;h1&gt;블로그&lt;/h1&gt;
    &lt;article v-for=&quot;post in posts&quot; :key=&quot;post.id&quot;&gt;
      &lt;h2&gt;{{ post.title }}&lt;/h2&gt;
      &lt;p&gt;{{ post.excerpt }}&lt;/p&gt;
    &lt;/article&gt;
  &lt;/div&gt;
&lt;/template&gt;

&lt;script&gt;
export default {
  async asyncData() {
    const posts = await $http.$get(&#x27;/api/posts&#x27;);
    return { posts };
  }
}
&lt;/script&gt;
</code></pre>

<h3>7.2 서버리스 아키텍처</h3>

<h4>AWS Lambda</h4>
<pre><code class="language-javascript">
// lambda 함수
exports.handler = async (event) =&gt; {
    const { name } = JSON.parse(event.body);
    
    // 비즈니스 로직
    const greeting = `Hello, ${name}!`;
    
    return {
        statusCode: 200,
        headers: {
            &#x27;Content-Type&#x27;: &#x27;application/json&#x27;,
            &#x27;Access-Control-Allow-Origin&#x27;: &#x27;*&#x27;
        },
        body: JSON.stringify({ message: greeting })
    };
};
</code></pre>

<h4>Vercel Functions</h4>
<pre><code class="language-javascript">
// api/hello.js
export default function handler(req, res) {
    const { name } = req.query;
    
    res.status(200).json({
        message: `Hello, ${name || &#x27;World&#x27;}!`
    });
}
</code></pre>

<h3>7.3 마이크로프론트엔드</h3>
<p>여러 팀이 독립적으로 프론트엔드를 개발할 수 있는 아키텍처입니다.</p>

<pre><code class="language-javascript">
// Module Federation (Webpack 5)
const ModuleFederationPlugin = require(&#x27;@module-federation/webpack&#x27;);

module.exports = {
    plugins: [
        new ModuleFederationPlugin({
            name: &#x27;shell&#x27;,
            remotes: {
                productApp: &#x27;productApp@http://localhost:3001/remoteEntry.js&#x27;,
                cartApp: &#x27;cartApp@http://localhost:3002/remoteEntry.js&#x27;
            }
        })
    ]
};

// 동적 로딩
const ProductApp = React.lazy(() =&gt; import(&#x27;productApp/ProductList&#x27;));
</code></pre>

<h2>8. DevOps와 배포</h2>

<h3>8.1 Git 워크플로우</h3>

<h4>Git Flow</h4>
<pre><code class="language-bash">
# 기능 개발
git checkout -b feature/user-authentication
git add .
git commit -m &quot;Add user authentication&quot;
git push origin feature/user-authentication

# Pull Request 생성 후 병합
git checkout develop
git pull origin develop
git merge feature/user-authentication
</code></pre>

<h3>8.2 CI/CD (Continuous Integration/Continuous Deployment)</h3>

<h4>GitHub Actions</h4>
<pre><code class="language-yaml">
# .github/workflows/deploy.yml
name: Deploy to Production

on:
  push:
    branches: [main]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Setup Node.js
        uses: actions/setup-node@v3
        with:
          node-version: &#x27;18&#x27;
      - name: Install dependencies
        run: npm install
      - name: Run tests
        run: npm test
      
  deploy:
    needs: test
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Deploy to server
        run: |
          echo &quot;Deploying to production server&quot;
          # 배포 스크립트 실행
</code></pre>

<h3>8.3 컨테이너화</h3>

<h4>Docker</h4>
<pre><code class="language-dockerfile">
# Dockerfile
FROM node:18-alpine

WORKDIR /app

COPY package*.json ./
RUN npm install --only=production

COPY . .

EXPOSE 3000

CMD [&quot;node&quot;, &quot;server.js&quot;]
</code></pre>

<pre><code class="language-yaml">
# docker-compose.yml
version: &#x27;3.8&#x27;

services:
  app:
    build: .
    ports:
      - &quot;3000:3000&quot;
    environment:
      - NODE_ENV=production
      - DB_HOST=db
    depends_on:
      - db

  db:
    image: postgres:13
    environment:
      - POSTGRES_DB=myapp
      - POSTGRES_USER=user
      - POSTGRES_PASSWORD=password
    volumes:
      - postgres_data:/var/lib/postgresql/data

volumes:
  postgres_data:
</code></pre>

<h2>9. 모니터링과 로깅</h2>

<h3>9.1 애플리케이션 모니터링</h3>

<h4>로깅</h4>
<pre><code class="language-javascript">
const winston = require(&#x27;winston&#x27;);

const logger = winston.createLogger({
    level: &#x27;info&#x27;,
    format: winston.format.combine(
        winston.format.timestamp(),
        winston.format.json()
    ),
    transports: [
        new winston.transports.File({ filename: &#x27;error.log&#x27;, level: &#x27;error&#x27; }),
        new winston.transports.File({ filename: &#x27;combined.log&#x27; })
    ]
});

// 사용 예시
app.get(&#x27;/api/users&#x27;, async (req, res) =&gt; {
    try {
        logger.info(&#x27;Fetching users&#x27;, { userId: req.user.id });
        const users = await User.find();
        res.json(users);
    } catch (error) {
        logger.error(&#x27;Failed to fetch users&#x27;, { error: error.message });
        res.status(500).json({ error: &#x27;Internal server error&#x27; });
    }
});
</code></pre>

<h4>성능 모니터링</h4>
<pre><code class="language-javascript">
// 응답 시간 측정
app.use((req, res, next) =&gt; {
    const start = Date.now();
    
    res.on(&#x27;finish&#x27;, () =&gt; {
        const duration = Date.now() - start;
        logger.info(&#x27;Request completed&#x27;, {
            method: req.method,
            url: req.url,
            statusCode: res.statusCode,
            duration: `${duration}ms`
        });
    });
    
    next();
});
</code></pre>

<h3>9.2 에러 처리</h3>

<h4>글로벌 에러 핸들러</h4>
<pre><code class="language-javascript">
// Express.js 에러 핸들러
app.use((err, req, res, next) =&gt; {
    logger.error(&#x27;Unhandled error&#x27;, {
        error: err.message,
        stack: err.stack,
        url: req.url,
        method: req.method
    });

    if (err.name === &#x27;ValidationError&#x27;) {
        return res.status(400).json({
            error: &#x27;Validation Error&#x27;,
            details: err.details
        });
    }

    res.status(500).json({
        error: &#x27;Internal Server Error&#x27;,
        message: process.env.NODE_ENV === &#x27;production&#x27; 
            ? &#x27;Something went wrong&#x27; 
            : err.message
    });
});

// 처리되지 않은 Promise rejection 처리
process.on(&#x27;unhandledRejection&#x27;, (reason, promise) =&gt; {
    logger.error(&#x27;Unhandled Rejection&#x27;, { reason, promise });
    process.exit(1);
});
</code></pre>

<h2>10. 웹 접근성과 SEO</h2>

<h3>10.1 웹 접근성 (Web Accessibility)</h3>

<h4>ARIA 활용</h4>
<pre><code class="language-html">
&lt;!-- 버튼 역할을 하는 div --&gt;
&lt;div role=&quot;button&quot; 
     aria-label=&quot;메뉴 열기&quot; 
     tabindex=&quot;0&quot;
     onclick=&quot;openMenu()&quot;&gt;
    ☰
&lt;/div&gt;

&lt;!-- 폼 라벨링 --&gt;
&lt;label for=&quot;email&quot;&gt;이메일 주소&lt;/label&gt;
&lt;input type=&quot;email&quot; 
       id=&quot;email&quot; 
       aria-describedby=&quot;email-help&quot;
       required&gt;
&lt;div id=&quot;email-help&quot;&gt;이메일 형식: user@example.com&lt;/div&gt;
</code></pre>

<h4>키보드 네비게이션</h4>
<pre><code class="language-css">
/* 포커스 스타일 */
button:focus,
input:focus {
    outline: 2px solid #007bff;
    outline-offset: 2px;
}

/* 포커스가 보이지 않을 때만 아웃라인 숨기기 */
.js-focus-visible button:focus:not(.focus-visible) {
    outline: none;
}
</code></pre>

<h3>10.2 SEO (Search Engine Optimization)</h3>

<h4>메타 태그 최적화</h4>
<pre><code class="language-html">
&lt;head&gt;
    &lt;!-- 기본 메타 태그 --&gt;
    &lt;title&gt;페이지 제목 - 사이트명&lt;/title&gt;
    &lt;meta name=&quot;description&quot; content=&quot;페이지에 대한 간결한 설명&quot;&gt;
    &lt;meta name=&quot;keywords&quot; content=&quot;키워드1, 키워드2, 키워드3&quot;&gt;
    
    &lt;!-- Open Graph (소셜 미디어) --&gt;
    &lt;meta property=&quot;og:title&quot; content=&quot;페이지 제목&quot;&gt;
    &lt;meta property=&quot;og:description&quot; content=&quot;페이지 설명&quot;&gt;
    &lt;meta property=&quot;og:image&quot; content=&quot;https://example.com/image.jpg&quot;&gt;
    &lt;meta property=&quot;og:url&quot; content=&quot;https://example.com/page&quot;&gt;
    
    &lt;!-- Twitter Card --&gt;
    &lt;meta name=&quot;twitter:card&quot; content=&quot;summary_large_image&quot;&gt;
    &lt;meta name=&quot;twitter:title&quot; content=&quot;페이지 제목&quot;&gt;
    &lt;meta name=&quot;twitter:description&quot; content=&quot;페이지 설명&quot;&gt;
    
    &lt;!-- 정규 URL --&gt;
    &lt;link rel=&quot;canonical&quot; href=&quot;https://example.com/page&quot;&gt;
&lt;/head&gt;
</code></pre>

<h4>구조화된 데이터</h4>
<pre><code class="language-html">
&lt;script type=&quot;application/ld+json&quot;&gt;
{
  &quot;@context&quot;: &quot;https://schema.org&quot;,
  &quot;@type&quot;: &quot;Article&quot;,
  &quot;headline&quot;: &quot;웹 개발 가이드&quot;,
  &quot;author&quot;: {
    &quot;@type&quot;: &quot;Person&quot;,
    &quot;name&quot;: &quot;홍길동&quot;
  },
  &quot;datePublished&quot;: &quot;2023-01-01&quot;,
  &quot;dateModified&quot;: &quot;2023-01-15&quot;,
  &quot;description&quot;: &quot;웹 개발에 대한 종합적인 가이드&quot;
}
&lt;/script&gt;
</code></pre>

<h2>웹 개발 학습 로드맵</h2>

<h3>1단계: 기초 (2-3개월)</h3>
<ul>
<li>HTML/CSS 기초</li>
<li>JavaScript 기초</li>
<li>Git 기본 사용법</li>
<li>브라우저 개발자 도구</li>
</ul>

<h3>2단계: 프론트엔드 심화 (3-4개월)</h3>
<ul>
<li>JavaScript ES6+ 문법</li>
<li>DOM 조작과 이벤트 처리</li>
<li>반응형 웹 디자인</li>
<li>CSS 전처리기 (Sass)</li>
</ul>

<h3>3단계: 백엔드 기초 (3-4개월)</h3>
<ul>
<li>Node.js와 Express.js</li>
<li>데이터베이스 (MySQL, MongoDB)</li>
<li>REST API 설계와 구현</li>
<li>인증과 보안 기초</li>
</ul>

<h3>4단계: 프레임워크 (2-3개월)</h3>
<ul>
<li>React 또는 Vue.js</li>
<li>상태 관리 (Redux, Vuex)</li>
<li>컴포넌트 기반 개발</li>
<li>SPA 개발</li>
</ul>

<h3>5단계: 고급 개념 (지속적)</h3>
<ul>
<li>TypeScript</li>
<li>테스팅 (Jest, Cypress)</li>
<li>DevOps 기초 (Docker, CI/CD)</li>
<li>성능 최적화</li>
<li>웹 보안</li>
</ul>

<p>웹 개발은 계속 발전하는 분야이므로, 기초를 탄탄히 하고 꾸준히 학습하는 것이 중요합니다. 실제 프로젝트를 만들어보면서 경험을 쌓아가시길 추천합니다!</p>
  </div>
</details>
