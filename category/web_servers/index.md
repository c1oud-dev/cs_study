---
layout: default
title: "Web Servers"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>Web Servers</h2>
  <p>웹 서버(Web Server)는 <b>클라이언트(주로 웹 브라우저)</b>로부터 요청을 받아 <b>HTML 페이지, 이미지, 기타 리소스 같은 웹 콘텐츠를 제공</b>하는 소프트웨어 또는 하드웨어 시스템이다. 웹 서버는 들어오는 <b>HTTP/HTTPS 요청을 처리</b>하고, 필요할 경우 <b>애플리케이션 서버나 데이터베이스와 상호작용</b>한 뒤, 적절한 응답을 클라이언트에게 반환한다.</p>
  <p>대표적인 웹 서버로는 <b>Apache HTTP Server, Nginx, Microsoft IIS</b>가 있으며, 웹 서버는 <b>웹사이트와 웹 애플리케이션 호스팅, 트래픽 관리, 동시 연결 처리, 정적·동적 콘텐츠 제공, SSL/TLS 암호화와 같은 보안 기능</b>을 통해 안정적인 온라인 자원 접근을 보장한다.</p>
  <p><strong style="color: #555555;">📝 정리: 웹 서버는 클라이언트의 요청을 받아 정적·동적 콘텐츠를 제공하고, 보안과 트래픽 관리를 통해 웹사이트와 애플리케이션을 안정적으로 운영하는 핵심 시스템이다.</strong></p>
</section>

<!-- 설명 -->
<details open>
<summary><span class="accordion-title">Nginx </span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
    <p>Nginx는 <b>고성능 오픈 소스 웹 서버이자 리버스 프록시 서버로, 효율성, 확장성, 낮은 자원 소모</b>로 잘 알려져 있다. 원래는 웹 서버로 개발되었지만, 오늘날에는 <b>로드 밸런서, HTTP 캐시, 메일 프록시</b>로도 널리 사용된다. Nginx는 <b>비동기(event-driven) 아키텍처</b> 덕분에 <b>대량의 동시 연결 처리</b>에 뛰어난 성능을 보인다.</p>
    <p>주요 기능으로는
        <ul>
            <li><strong>정적 콘텐츠 제공</strong> </li>
            <li><strong>동적 콘텐츠는 애플리케이션 서버로 프록시 처리</strong> </li>
            <li><strong>SSL/TLS 종료 제공(보안 기능)</strong> </li>
        </ul>
        또한 <b>모듈형 설계(modular design)</b>로 다양한 애플리케이션 및 서비스와의 통합·확장이 가능하여, <b>현대 웹 인프라에서 널리 사용되는 선택지</b>가 되고 있다.
    </p>
    <p><strong style="color: #555555;">📝 정리: Nginx는 이벤트 기반 아키텍처로 수많은 동시 연결을 효율적으로 처리하며, 웹 서버·리버스 프록시·로드 밸런서로 현대 웹 인프라에 널리 활용되는 고성능 오픈 소스 서버이다.</strong></p>
</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title">Apache </span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
    <p>Apache(정식 명칭: <b>Apache HTTP Server</b>)는 <b>Apache Software Foundation</b>에서 개발·관리하는 <b>무료 오픈 소스 웹 서버 소프트웨어</b>이다. 전 세계에서 가장 널리 쓰이는 웹 서버 중 하나로, <b>견고함, 유연성, 풍부한 기능</b>으로 잘 알려져 있다.</p>
    <p>Apache는 <b>다양한 운영체제</b>를 지원하고, <b>모듈형 아키텍처</b>를 통해 여러 콘텐츠 유형과 프로그래밍 언어를 처리할 수 있다. 주요 기능으로는 <b>가상 호스팅(Virtual Hosting), SSL/TLS 지원, URL 리라이팅</b> 등이 있다. 또한 <b>설정 파일(Configuration Files)</b>을 통해 서버 동작을 세밀하게 커스터마이징할 수 있다.</p>
    <p>최근에는 <b>동시성 처리 성능</b>에서 Nginx 같은 신생 대안과 경쟁을 겪고 있지만, Apache는 여전히 <b>안정성, 풍부한 문서, 대규모 커뮤니티 지원</b> 덕분에 널리 사용된다. 특히 <b>LAMP 스택(Linux, Apache, MySQL, PHP/Perl/Python)</b>과의 높은 호환성으로 선호된다.</p>
    <p><strong style="color: #555555;">📝 정리: Apache는 LAMP 스택을 대표하는 오픈 소스 웹 서버로, 모듈형 아키텍처와 풍부한 기능을 제공하며 안정성과 커뮤니티 지원 덕분에 여전히 널리 사용된다.</strong></p>
</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title">Caddy </span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
    <p>Caddy는 <b>Go 언어로 작성된 현대적인 오픈 소스 웹 서버</b>이다. 주요 특징은 <b>간단함, 자동 HTTPS 암호화, HTTP/2 기본 지원</b>으로 잘 알려져 있다.</p>
    <p>Caddy의 장점은 <b>쉬운 사용성</b>으로, 단순한 설정 구문을 제공하며, 정적 파일을 <b>설정 없이 바로 서비스</b>할 수 있다. 또한 <b>Let's Encrypt</b>를 통해 SSL/TLS 인증서를 자동으로 발급·갱신하여 보안 배포를 손쉽게 할 수 있다.</p>
    <p>Caddy는 <b>리버스 프록시, 로드 밸런싱, 동적 가상 호스팅</b> 등을 포함한 다양한 플러그인·모듈 확장을 지원한다. 기본적으로 <b>보안을 염두에 둔 설계</b>로, 최신 웹 표준을 기본 구현하고 있다.</p>
    <p>비록 극도로 높은 부하 상황에서는 Nginx 같은 서버의 <b>순수 성능(raw performance)</b>에 미치지 못할 수 있지만, <b>간결함, 내장된 보안 기능, 낮은 리소스 사용량</b> 덕분에, 특히 <b>소규모~중간 규모 프로젝트나 번거롭지 않은 서버 세팅을 원하는 개발자</b>에게 매력적인 선택지가 된다.</p>
    <p><strong style="color: #555555;">📝 정리: Caddy는 Go로 작성된 현대적 웹 서버로, 자동 HTTPS·간단한 설정·보안 중심 설계 덕분에 중소규모 프로젝트와 빠른 배포에 적합한 오픈 소스 서버이다.</strong></p>
    <!-- 가로선 추가 -->
    <hr>
    <ul>
        <li><strong>Let's Encrypt:</strong> 무료로 SSL/TLS 인증서를 발급해 주는 인증 기관(CA)으로, HTTPS를 자동으로 적용·갱신할 수 있게 해주는 서비스.</li>
        <li><strong>리버스 프록시 (Reverse Proxy):</strong> 클라이언트 대신 서버 요청을 받아 내부 서버로 전달하고, 그 결과를 다시 클라이언트에 반환하는 중간 서버.</li>
        <ul>
            <li>예: 로드 밸런싱, 보안, 캐싱에 사용</li>
        </ul>
        <li><strong>순수 성능 (Raw Performance):</strong> 추가적인 기능이나 최적화를 제외하고, 시스템이 기본적으로 처리할 수 있는 성능(처리 속도·처리량) 자체를 의미.</li>
    </ul>
</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title">MS IIS </span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
    <p><b>Microsoft Internet Information Services (IIS)</b>는 마이크로소프트가 개발한 <b>유연하고 안전하며 고성능의 웹 서버</b>로, Windows Server에서 웹 애플리케이션과 서비스를 호스팅·관리하기 위해 사용된다.</p>
    <p>IIS는 <b>ASP.NET, PHP, 정적 콘텐츠</b> 등 다양한 웹 기술을 지원하며, <b>요청 처리, 인증, SSL/TLS 암호화, URL 리라이팅</b> 같은 기능을 제공한다. 또한 <b>GUI(그래픽 인터페이스)</b>와 <b>명령줄 옵션</b>을 포함한 강력한 관리 도구를 제공하여 웹 사이트 및 애플리케이션을 손쉽게 설정·모니터링할 수 있다.</p>
    <p>IIS는 주로 <b>Windows 기반 환경</b>에서 <b>엔터프라이즈 웹 애플리케이션과 서비스 배포</b>에 사용되며, 다른 Microsoft 기술 및 서비스와의 뛰어난 통합성을 제공한다.</p>
    <p><strong style="color: #555555;">📝 정리: IIS는 Windows Server용 마이크로소프트 웹 서버로, ASP.NET 등 다양한 기술을 지원하며 보안·관리 도구·MS 생태계 통합에 강점을 가진다.</strong></p>
</div>
</details>
