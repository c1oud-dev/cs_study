---
layout: default
title: "APIs"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>APIs</h2>
  <p>
    API(Application Programming Interface)는 서로 다른 소프트웨어 애플리케이션이 서로 통신하고 상호작용할 수 있도록 하는 정의된 규칙과 프로토콜의 집합이다. 개발자가 서비스, 애플리케이션 또는 플랫폼의 내부 작동 방식을 이해하지 않고도 해당 기능이나 데이터에 접근하고 조작할 수 있는 표준화된 방법을 제공한다. API는 공개 또는 비공개로 제공되며, 일반적으로 서로 다른 시스템을 통합하고, 타사 개발을 용이하게 하며, 애플리케이션 간 상호 운용성을 지원하는 데 사용된다. 일반적으로 API에는 엔드포인트, 요청 메서드(GET, POST, PUT 등), 그리고 상호작용할 데이터 형식(JSON 또는 XML 등)이 포함된다.
  </p>
  <p><strong>정리: API는 프로그램들이 서로 대화할 수 있게 하는 약속된 규칙집 </strong></p>
</section>

<details open>
<summary><span class="accordion-title">API Authentication</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>API 인증은 API에 액세스하려는 클라이언트의 신원을 확인하고, 권한이 있는 사용자 또는 애플리케이션만 API 리소스와 상호 작용할 수 있도록 하는 *프로세스이다. 일반적인 방법으로는 *API 키, *OAuth 2.0, *JSON 웹 토큰(JWT), *기본 인증, *OpenID Connect 등이 있다. 이러한 기술은 단순한 *토큰 기반 방식부터 인증과 권한 부여를 모두 처리하는 더욱 정교한 프로토콜까지 복잡성과 보안 수준이 다양하다. API 인증은 민감한 데이터를 보호하고, 무단 액세스를 차단하며, 사용량 추적을 지원하고, 리소스 액세스에 대한 세부적인 제어를 제공할 수 있다. 인증 방법은 보안 요구 사항, 클라이언트 유형, 구현 용이성, 확장성 요구 사항 등의 요인에 따라 달라진다. 상호 연결된 현대 소프트웨어 생태계에서 웹 서비스와 애플리케이션의 무결성, 보안 및 제어된 사용을 유지하려면 강력한 API 인증을 구현하는 것이 매우 중요하다.</p>
  <p><strong>정리: API 인증은 권한 있는 사용자만 API를 쓸 수 있게 신원을 확인하는 절차</strong></p>

  <ul>
    <li><strong>프로세스(Process):</strong> 컴퓨터에서 실행 중인 프로그램 또는 작업의 흐름. 여기서는 인증을 진행하는 절차나 단계들을 의미.</li>
    <li><strong>API 키(API Key):</strong> API 사용자를 식별하기 위한 고유 문자열. 요청 시 키를 포함해 서버가 사용자 신원을 확인.</li>
    <li><strong>OAuth 2.0:</strong> 비밀번호를 직접 주지 않고, 제3자 앱이 사용자 권한을 위임받아 API를 쓸 수 있도록 하는 인증 방식. (예: 구글 계정 로그인)</li>
    <li><strong>JSON 웹 토큰(JWT):</strong> JSON 형식으로 인코딩된 토큰. 인증·권한 정보를 담아 서명하여 위변조를 방지하고, 클라이언트-서버 간 안전하게 전달.</li>
    <li><strong>기본 인증(Basic Auth):</strong> 사용자 이름과 비밀번호를 Base64로 인코딩해 HTTP 요청 헤더에 포함하는 간단한 인증 방식. 보안에 취약해 HTTPS와 함께 사용해야 함.</li>
    <li><strong>OpenID Connect:</strong> OAuth 2.0 위에서 동작하는 인증 프로토콜로, 로그인 및 사용자 프로필 정보 제공을 표준화. (예: 소셜 로그인)</li>
    <li><strong>토큰(Token):</strong> 인증이 완료된 사용자를 식별하고 권한을 부여하기 위해 발급되는 임시 인증 정보. 일정 시간 동안만 유효.</li>
  </ul>

  <!-- 박스 추가 -->
  <details>
    <summary><span class="accordion-title">JWT </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>JWT(JSON 웹 토큰)는 당사자 간에 *JSON 객체 형태로 정보를 안전하게 전송하기 위한 *개방형 표준이다. JWT는 세 부분으로 구성된다. 헤더(토큰 유형 및 서명에 사용되는 알고리즘 지정), 페이로드(전송되는 클레임 또는 데이터 포함), 서명(토큰의 무결성 및 진위성 확인)이다. JWT는 일반적으로 인증 및 권한 부여 목적으로 사용되며, 사용자가 웹 애플리케이션과 API를 통해 신원과 권한을 안전하게 전송하고 검증할 수 있도록 한다. JWT는 작고 독립적이며 *HTTP 헤더를 통해 쉽게 전송할 수 있어 최신 웹 및 모바일 애플리케이션에서 널리 사용된다.</p>
      <p><strong>정리: JWT는 인증 정보를 JSON 형태로 담아 안전하게 주고받는 토큰</strong></p>
      <ul>
        <li><strong>JSON 객체 형태:</strong> <em>{ "key": "value" }</em>처럼 키-값 쌍으로 이루어진 데이터 구조. 중괄호 {}로 감싸고, 문자열은 큰따옴표 <em>"<em>로 감쌈.</li>
        <li><strong>개방형 표준(Open Standard):</strong> 누구나 자유롭게 사용할 수 있도록 공개된 기술 규격. 특정 회사나 조직에 종속되지 않고, 상호 호환 가능.</li>
        <li><strong>HTTP 헤더(HTTP Header):</strong> HTTP 요청·응답의 부가 정보를 담는 메타데이터 영역. (예: 요청의 인증 정보, 콘텐츠 타입, 언어 설정 등.)</li>
      </ul>
    </div>
  </details>

  <details>
    <summary><span class="accordion-title">OAuth </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>OAuth는 타사 애플리케이션이 사용자 인증 정보를 노출하지 않고 사용자 리소스에 액세스할 수 있도록 하는 개방형 권한 부여 표준이다. 사용자가 권한을 부여하면 액세스 토큰을 발급하여 애플리케이션이 사용자를 대신하여 리소스 서버와 상호 작용할 수 있도록 한다. 이 프로세스에는 리소스 소유자(사용자), 데이터를 보관하는 리소스 서버, 그리고 토큰을 발급하는 권한 부여 서버가 포함된다. OAuth는 안전한 토큰 기반 액세스 관리를 지원하며, 이는 일반적으로 애플리케이션에 소셜 미디어 계정이나 클라우드 스토리지와 같은 서비스와 상호 작용할 수 있는 권한을 부여하는 데 사용된다.</p>
      <p><strong>정리: OAuth는 비밀번호 없이 권한을 위임해 안전하게 접근하게 하는 인증 방식</strong></p>
    </div>
  </details>

  <details>
    <summary><span class="accordion-title">Basic authentication </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>Basic authentication은 HTTP 프로토콜에 내장된 간단한 HTTP 인증 체계이다. HTTP 헤더에 base64 형식으로 인코딩된 사용자 인증 정보(사용자 이름과 비밀번호)를 전송하여 작동한다. 클라이언트가 인증을 요구하는 서버에 요청을 보내면 서버는 401 상태 코드와 "WWW-Authenticate" 헤더로 응답한다. 그런 다음 클라이언트는 "Basic"이라는 단어와 base64로 인코딩된 "username:password" 문자열을 포함하는 Authorization 헤더를 사용하여 요청을 다시 전송한다. 기본 인증은 구현하기 쉽지만 심각한 보안 제약이 있다. 인증 정보는 기본적으로 일반 텍스트(base64는 쉽게 디코딩됨)로 전송되며 암호화를 제공하지 않는다. 따라서 전송 중 인증 정보가 안전하게 보호되도록 HTTPS 연결을 통해서만 사용해야 한다. 기본 인증은 단순하고 고급 보안 기능이 부족하기 때문에 일반적으로 간단하고 위험도가 낮은 시나리오 또는 대체 메커니즘으로만 권장된다.</p>
      <p><strong>정리: 아이디와 비밀번호를 HTTP 헤더에 담아 인증하는 기본 방식</strong></p>
    </div>
  </details>

  <details>
    <summary><span class="accordion-title">Token authentication </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>토큰 기반 인증은 사용자가 신원을 확인하고 그 대가로 고유한 액세스 토큰을 받을 수 있도록 하는 프로토콜이다. 토큰이 유효한 기간 동안 사용자는 동일한 웹페이지, 앱 또는 해당 토큰으로 보호되는 리소스에 다시 접속할 때마다 자격 증명을 다시 입력할 필요 없이, 토큰이 발급된 웹사이트나 앱에 액세스할 수 있다. 인증 토큰은 스탬프가 찍힌 티켓처럼 작동한다. 사용자는 토큰이 유효한 동안 액세스 권한을 유지한다. 사용자가 로그아웃하거나 앱을 종료하면 토큰은 무효화된다. 토큰 기반 인증은 기존의 비밀번호 기반 또는 서버 기반 인증 기술과 다르다. 토큰은 보안을 강화하며, 관리자는 각 작업과 트랜잭션을 세부적으로 제어할 수 있다.</p>
      <p><strong>정리: 인증 후 발급받은 토큰으로 요청마다 신원을 확인하는 방식</strong></p>
    </div>
  </details>

  <details>
    <summary><span class="accordion-title">Cookie-Based Authentication </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>쿠키 기반 인증은 웹 애플리케이션에서 사용자 세션을 유지하는 방법이다. 사용자가 로그인하면 서버는 세션을 생성하고 고유 식별자(세션 ID)를 쿠키 형태로 클라이언트에 전송한다. 이 쿠키는 이후 모든 요청과 함께 전송되어 서버가 사용자를 식별하고 인증할 수 있도록 한다. 실제 세션 데이터는 일반적으로 서버에 저장되며, 쿠키는 이 데이터에 접근하는 키 역할을 한다. 이 방식은 서버 측에서 상태를 저장하며 기존 웹 애플리케이션에 적합하다. 구현이 비교적 간단하고 브라우저에서 기본적으로 지원된다. 그러나 쿠키 기반 인증은 교차 출처 요청(Cross-Origin Request)과 관련된 문제에 직면하고, 적절하게 보호되지 않으면 CSRF 공격에 취약할 수 있으며, 최신 단일 페이지 애플리케이션이나 모바일 앱에는 적합하지 않을 수 있다. 이러한 한계에도 불구하고, 특히 서버 렌더링 웹 애플리케이션에서 여전히 널리 사용되는 인증 방법이다.</p>
      <p><strong>정리: 로그인 후 쿠키에 세션 정보를 저장해 인증을 유지하는 방식</strong></p>
    </div>
  </details>

  <details>
    <summary>OpenID <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>OpenID는 분산 인증을 위한 개방형 표준으로, 사용자가 ID 공급자(IdP)가 관리하는 단일 자격 증명 세트를 사용하여 여러 웹사이트와 애플리케이션에 로그인할 수 있도록 한다. 사용자는 외부 서비스를 통해 자신의 신원을 인증할 수 있으므로 로그인 프로세스가 간소화되고 여러 사용자 이름과 비밀번호의 필요성이 줄어든다. OpenID는 일반적으로 OAuth 2.0과 연동되어 사용자가 보안을 유지하면서 데이터 접근 권한을 부여할 수 있도록 한다. 이러한 접근 방식은 사용자 편의성을 향상시키고 다양한 플랫폼에서 ID 관리를 간소화한다.</p>
      <p><strong>정리: 하나의 계정으로 여러 서비스에 로그인할 수 있게 하는 인증 표준</strong></p>
    </div>
  </details>

  <details>
    <summary>Security Assertion Markup Language (SAML) <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>SAML(Security Assertion Markup Language)은 싱글 사인온(SSO) 및 ID 페더레이션에 사용되는 XML 기반 프레임워크로, 사용자가 한 번의 인증으로 여러 애플리케이션이나 서비스에 액세스할 수 있도록 한다. ID 공급자(IdP)와 서비스 공급자(SP) 간에 인증 및 권한 부여 데이터를 교환할 수 있도록 한다. SAML 어설션은 사용자 ID 정보와 속성을 포함하는 XML 문서로, 인증 자격 증명과 권한을 전달하는 데 사용된다. SAML을 구현함으로써 조직은 사용자 관리를 간소화하고, 중앙 집중식 인증을 통해 보안을 강화하며, 여러 시스템에서 여러 번 로그인해야 하는 번거로움을 줄여 사용자 경험을 간소화할 수 있다.</p>
      <p><strong>정리: XML 기반으로 사용자 인증·권한 정보를 교환하는 표준</strong></p>
    </div>
  </details>

</div>
</details>

<details open>
<summary><span class="accordion-title">REST API </span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>REST API(Representational State Transfer Application Programming Interface)는 *네트워크 애플리케이션을 설계하는 아키텍처 스타일이다. 표준 HTTP 메서드(GET, POST, PUT, DELETE)를 사용하여 리소스와 상호 작용하며, 리소스는 *URI(Uniform Resource Identifier)로 표현된다. REST API는 상태를 저장하지 않으므로 클라이언트에서 서버로 보내는 각 요청에는 요청을 이해하고 처리하는 데 필요한 모든 정보가 포함되어야 한다. 표준 HTTP 상태 코드를 사용하여 요청 결과를 나타내며, *JSON이나 *XML과 같은 형식으로 통신하는 경우가 많다. REST API는 단순성, 확장성, 그리고 웹 서비스 및 애플리케이션과의 통합 용이성으로 인해 널리 사용된다.
  </p>
  <p><strong>정리: REST API는 HTTP 규칙으로 리소스를 주고받는 상태 없는 설계 방식</strong></p>

  <ul>
    <li><strong>네트워크 애플리케이션:</strong> 인터넷이나 로컬 네트워크를 통해 다른 컴퓨터나 서버와 통신하며 동작하는 프로그램 (예: 웹 브라우저, 메신저 앱)</li>
    <li><strong>URI(Uniform Resource Identifier):</strong> 인터넷에서 자원(리소스)을 식별하는 주소 체계(예: https://example.com/users/1)</li>
    <li><strong>JSON (JavaScript Object Notation):</strong> 데이터를 사람이 읽기 쉽고 기계가 처리하기 쉬운 텍스트 형식으로 표현하는 방법</li>
      <ul>
        <li>주로 {: 값} 구조를 사용</li>
      </ul>
    <li><strong>XML (eXtensible Markup Language):</strong> 태그(<tag>내용</tag>)를 이용해 데이터를 구조적으로 표현하는 마크업 언어</li>
      <ul>
        <li>HTML과 비슷하지만 데이터 저장·전송에 초점</li>
      </ul>
  </ul>

</div>
</details>

<details>
<summary><span class="accordion-title">JSON API </span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>JSON(JavaScript Object Notation)은 정의된 방식으로 통신하는 서버와 각 애플리케이션이 통신할 때 *임시 코드가 필요 없도록 설계된 *인코딩 체계이다. JSON API 모듈은 엔티티 유형, 번들, 필드와 같은 데이터 저장소 및 데이터 구조에 대한 구현을 제공한다.
  </p>
  <p><strong>정리: JSON은 서버와 앱이 간단하고 표준화된 방식으로 데이터를 주고받게 하는 형식</strong></p>

  <ul>
    <li><strong>임시 코드:</strong> 특정 상황이나 문제를 해결하기 위해 급하게 작성한, 재사용성·유지보수성이 떨어지는 코드. 흔히 "하드코딩"과 비슷한 개념으로, 표준화된 형식이 없으면 이런 코드를 많이 쓰게 됨.</li>
    <li><strong>인코딩(Encoding):</strong> 데이터를 저장하거나 전송하기 위해 다른 형식으로 변환하는 과정 (예: 텍스트를 UTF-8로 변환, 이미지를 JPG로 저장)</li>
  </ul>

</div>
</details>

<details>
<summary>SOAP <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>SOAP(Simple Object Access Protocol)는 시스템과 애플리케이션 간의 정보 교환을 위한 메시지 프로토콜이다. 애플리케이션 프로그래밍 인터페이스(API)의 경우, SOAP API는 더욱 체계적이고 정형화된 방식으로 개발된다. SOAP 메시지는 웹 관련 하이퍼텍스트 전송 프로토콜(HTTP)을 포함한 다양한 하위 수준 프로토콜을 통해 전송될 수 있다.
  </p>
  <p><strong>정리: SOAP는 정형화된 규칙으로 메시지를 주고받는 API 통신 프로토콜</strong></p>

</div>
</details>

<details>
<summary>gRPC <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>gRPC는 고성능 오픈 소스 범용 RPC 프레임워크이다. RPC는 원격 프로시저 호출(Remote Procedure Call)의 약자이다. g가 무엇을 의미하는지에 대한 논쟁이 계속되고 있다. RPC는 프로그램이 다른 컴퓨터에 있는 다른 프로그램의 프로시저를 실행할 수 있도록 하는 프로토콜이다. 가장 큰 장점은 개발자가 원격 상호 작용의 세부 사항을 코딩할 필요가 없다는 것이다. 원격 프로시저는 다른 함수와 마찬가지로 호출된다. 하지만 클라이언트와 서버는 서로 다른 언어로 코딩할 수 있다.
  </p>
  <p><strong>정리: gRPC는 빠르고 효율적으로 서버 간 데이터를 주고받는 원격 호출 프로토콜</strong></p>

</div>
</details>

<details>
<summary>GraphQL <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>GraphQL은 페이스북에서 개발한 API용 쿼리 언어이자 해당 쿼리를 실행하는 런타임이다. 고정된 엔드포인트가 미리 정의된 데이터를 반환하는 REST와 달리, GraphQL은 클라이언트가 필요한 데이터를 정확하게 요청할 수 있도록 하여 API 상호작용을 더욱 유연하고 효율적으로 만든다. GraphQL은 단일 엔드포인트를 사용하고 사용 가능한 데이터의 유형과 구조를 정의하는 스키마를 사용한다. 이러한 접근 방식은 데이터 오버페칭(overfetching)과 언더페칭(underfetching)을 줄여 여러 플랫폼(예: 웹, 모바일)에서 다양한 데이터 요구 사항을 가진 복잡한 애플리케이션에 이상적이다.
  </p>
  <p><strong>정리: GraphQL은 클라이언트가 필요한 데이터만 선택해 요청할 수 있는 쿼리 언어</strong></p>

</div>
</details>

<details>
<summary>HATEOAS <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>HATEOAS(Hypermedia As The Engine Of Application State)는 RESTful 아키텍처의 제약 조건으로, 클라이언트가 응답에 제공된 하이퍼미디어 링크를 통해 API를 동적으로 탐색할 수 있도록 한다. URL이나 엔드포인트를 하드코딩하는 대신, 클라이언트는 웹 브라우저가 웹페이지의 링크를 따라가는 것처럼 이러한 링크를 통해 사용 가능한 작업을 탐색한다. 이를 통해 유연성이 향상되고 클라이언트가 서버 측 변경 사항으로부터 분리되어 기존 클라이언트를 중단시키지 않고도 시스템의 적응성과 확장성이 향상된다. 이는 REST의 무상태성(stateless) 원칙과 자체 기술적 메시지(self-descriptive messages) 원칙의 핵심 요소이다.
  </p>
  <p><strong>정리: API 응답에 다음 행동 링크를 포함해 클라이언트가 탐색하도록 돕는 REST 원칙</strong></p>

</div>
</details>

<details>
<summary>Open API Spec <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>OpenAPI 사양(OAS, 이전 명칭: Swagger)은 RESTful API를 정의하고 문서화하는 표준이다. API 엔드포인트, 요청 및 응답 형식, 인증 방법 및 기타 메타데이터를 설명하는 YAML 또는 JSON 형식의 구조화된 형식을 제공한다. 개발자는 OAS를 사용하여 클라이언트 생성, 자동화된 문서화 및 테스트를 용이하게 하는 포괄적이고 기계가 읽을 수 있는 API 설명을 작성할 수 있다. 이 사양은 API 설계의 일관성과 명확성을 높이고, 서로 다른 시스템 간의 상호 운용성을 향상시키며, 클라이언트 라이브러리, 서버 스텁 및 대화형 API 문서를 생성하는 도구를 지원한다.
  </p>
  <p><strong>정리: API의 구조와 사용법을 표준 형식으로 문서화한 사양</strong></p>

</div>
</details>
