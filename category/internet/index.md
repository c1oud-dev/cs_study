---
layout: default
title: "Internet"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>Internet</h2>
  <p>인터넷은 주로 <b>TCP/IP</b>라는 표준화된 프로토콜을 사용하여 서로 통신하는, 전 세계적으로 상호 연결된 컴퓨터들의 글로벌 네트워크이다. 웹페이지를 요청하면, 사용자의 기기는 데이터 패킷을 인터넷 서비스 제공업체(ISP)를 거쳐 DNS 서버로 보낸다. <b>DNS 서버</b>는 웹사이트의 도메인 이름을 <b>IP 주소</b>로 변환한다. 그 후 이 패킷은 <b>라우터와 스위치</b>를 통해 여러 네트워크를 거쳐 목적지 서버로 전달되고, 서버는 요청을 처리한 뒤 응답을 다시 보낸다.</p>
  <p>이러한 요청과 응답의 왕복 과정은 웹페이지, 이메일, 파일과 같은 데이터를 전송할 수 있게 하며, 인터넷을 <b>글로벌 통신을 위한 역동적이고 분산된 시스템</b>으로 만든다.</p>
</section>

<details open>
  <summary><span class="accordion-title"><a href="category/internet/http.html">HTTP</a></span> <span class="indicator">접기</span></summary>
  <div class="accordion-content">
    <p>HTTP(Hypertext Transfer Protocol)는 월드 와이드 웹을 통해 하이퍼텍스트를 전송하는 데 사용되는 프로토콜이다. 이 프로토콜은 메시지가 어떻게 포맷되고 전송되는지, 그리고 웹 서버와 브라우저가 다양한 명령에 어떻게 응답해야 하는지를 정의한다.</p>
    <p>HTTP는 요청-응답 모델(request-response model)로 동작한다. 즉, 클라이언트(일반적으로 웹 브라우저)가 서버에 웹페이지나 파일과 같은 리소스를 요청하면, 서버는 요청된 콘텐츠와 함께 요청 결과를 나타내는 HTTP 상태 코드(HTTP status code)로 응답한다.</p>
    <p>HTTP는 <b>무상태(stateless)</b> 방식으로, 클라이언트가 서버에 보내는 각 요청은 이전 상호작용에 대한 정보를 유지하지 않고 독립적으로 처리된다. HTTP는 웹 데이터 통신의 기반을 이루며, 일반적으로 암호화된 통신을 위해 보안 HTTP(HTTPS)와 함께 사용된다.</p>
    <hr>
        <ul>
            <li><strong>월드 와이드 웹(WWW):</strong> 전 세계의 HTML 문서를 하이퍼링크로 연결해 정보를 탐색할 수 있는 시스템</li>
            <li><strong>하이퍼텍스트:</strong> 클릭 가능한 링크를 통해 문서 간 이동을 지원하는 텍스트 형식</li>
            <li><strong>프로토콜:</strong> 네트워크 상에서 데이터 교환 시 지켜야 할 통신 규약(형식·순서 등)</li>
            <li><strong>웹 서버:</strong> 클라이언트의 HTTP 요청을 받아 HTML, 이미지, API 응답 등을 제공하는 SW</li>
            <li><strong>브라우저:</strong> 웹 서버와 HTTP로 통신해 HTML/CSS/JS를 해석·렌더링하는 클라이언트 애플리케이션</li>
            <li><strong>HTTP 상태 코드:</strong> 요청 결과를 숫자(200 성공, 404 못 찾음 등)로 나타내는 표준화된 응답 코드</li>
            <li><strong>상태 비저장 프로토콜:</strong> 각 요청을 독립 처리해 서버가 이전 요청 정보를 저장하지 않는 통신 방식</li>
        </ul>
  </div>
</details>

<details>
<summary><span class="accordion-title"><a href="category/internet/domain_name.html">Domain Name</a></span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
    <p>도메인 이름(Domain Name)은 인터넷에서 특정 위치를 식별하기 위해 사용되는 <b>사람이 읽을 수 있는 주소</b>로, 웹사이트와 온라인 서비스에 더 쉽게 접근할 수 있게 해준다. 도메인 이름은 <b>IP 주소</b>로 변환되는데, IP 주소는 컴퓨터가 서버를 찾고 연결하는 데 사용하는 숫자 식별자이다.</p>
    <p>도메인 이름은 두 가지 주요 부분으로 구성된다.
        <ul>
            <li><b>2차 도메인(Second-Level Domain)</b> 예: "example.com"에서 "example"</li>
            <li><b>최상위 도메인(Top-Level Domain, TLD)</b> 예: ".com"</li>
        </ul>
    </p>
    <p>도메인 이름은 **도메인 등록기관(domain name registrar)**에 의해 관리되며, 숫자 IP 주소 대신 사용자 친화적인 방식으로 웹사이트에 접속할 수 있게 해주어 <b>웹 존재감을 확립하는 데 필수적</b>이다.</p>
    <hr>
    <ul>
        <li><strong>IP:</strong> 네트워크 상 장치에 고유한 주소(IP 주소)를 부여해 데이터 패킷을 목적지까지 전달하는 통신 규약
        <ul>
            <li>버전: IPv4(32비트 주소 체계)와 IPv6(128비트 주소 체계)로 구분되며, 라우터가 최적 경로로 패킷을 전송한다.</li>
            <li>비연결 지향: 상태를 유지하지 읺고 각 패킷을 독립 처리하므로, 신뢰성 보장은 상위 계층(TCP 등)에 맡긴다.</li>
        </ul>
        </li>
    </ul>

    </div>
</details>

<details>
<summary><span class="accordion-title"><a href="category/internet/hosting.html">Hosting</a> </span><span class="indicator">펼치기</span></summary>
<div class="accordion-content">
    <p>호스팅(Hosting)은 인터넷을 통해 사용자에게 웹사이트 파일과 애플리케이션을 저장하고 제공하기 위해 <b>서버 공간과 리소스를 제공하는 서비스</b>를 의미한다. 호스팅 제공자는 웹사이트와 애플리케이션이 온라인에서 접근 가능하도록 하기 위해 필요한 <b>서버, 스토리지, 네트워크 연결</b> 등의 인프라를 제공한다.</p>
    <p>호스팅에는 여러 유형이 있으며, 예를 들어
        <ul>
            <li><b>공유 호스팅(Shared Hosting):</b> 여러 웹사이트가 하나의 서버를 공유</li>
            <li><b>가상 사설 서버(VPS)</b> </li>
            <li><b>전용 호스팅(Dedicated Hosting):</b> 하나의 서버를 단일 사용자에게 전용 제공</li>
            <li><b>클라우드 호스팅(Cloud Hosting):</b> 서버 네트워크를 사용하여 확장 가능한 리소스를 제공</li>
        </ul>
        호스팅 서비스는 종종 <b>도메인 등록, 보안 기능, 기술 지원</b>을 포함하여 웹사이트가 안정적으로 이용 가능하고 성능이 잘 유지되도록 한다.
    </p>
    <hr>
    <ul>
    <li><strong>스토리지:</strong> 데이터나 파일을 저장하는 물리적·논리적 공간으로, HDD/SSD, SAN/NAS, 오브젝트, 스토리지 등이 있다.
    <ul>
        <li>HDD/SSD: 블록 단위 스토리지 매체로, HDD는 회전하는 디스크 기반으로 대용량·저비용, SSD는 플래시 메모리 기반으로 빠른 입출력 성능을 제공</li>
        <li>SAN/NAS: SAN은 고속 네트워크로 연결된 블록 스토리지, NAS는 파일 공유 방식의 네트워크 스토리지로, 둘 다 중앙화된 스토리지 자원을 여러 서버에서 효율적으로 사용할 수 있게 해준다.</li>
        <li>오브젝트 스토리지: HTTP API로 접근하는 개체(Object) 단위 스토리지로, 각 객체에 메타데이터를 붙여 무제한 확장성과 높은 내구성·가용성을 제공하며 로그·이미지·백업 등 비정형 데이터에 최적화되어 있다.</li>
    </ul>
    </li>
    <li><strong>인프라:</strong> 서버·네트워크·스토리지·가상화·보안 같은 IT 시스템의 기반 자원과 환경 전체를 의미</li>
    <li><strong>가상 사설 서버(VPS):</strong> 하이퍼바이저로 물리 서버를 분할해 각 사용자에게 독립된 가상 머신 환경을 제공하는 서비스
    <ul>
        <li>하이퍼바이저: 물리 서버 위에 여러 가상 머신(VM)을 생성·관리하는 소프트웨어 계층</li>
    </ul>
    </li>
    <li><strong>가용성:</strong> 시스템이나 서비스가 일정 기간 동안 정상적으로 운영될 수 있는 비율(예: 99.9% 가용성은 연 8.76시간 이하 다운 허용)을 의미</li>
    <li><strong>호스팅 종류:</strong> 공유 호스팅, VPS, 전용 서버, 클라우드 호스팅, 매니지드 호스팅, 콜로케이션 등 자원 격리·관리 범위·비용별로 구분</li>
    </ul>

</div>
</details>

<details>
<summary><span class="accordion-title"><a href="category/internet/dns.html">DNS</a> </span><span class="indicator">펼치기</span></summary>
<div class="accordion-content">
    <p>DNS(Domain Name System)는 인터넷이나 사설 네트워크에 연결된 컴퓨터, 서비스 또는 다른 자원들을 위한 <b>계층적이고 분산된 이름 체계</b>이다. DNS는 사람이 읽을 수 있는 도메인 이름(예: www.example.com)을 컴퓨터가 서로를 식별하는 데 사용하는 IP 주소(예: 192.0.2.1)로 변환한다. 전 세계에 분산된 DNS 서버들은 이러한 질의를 해결하기 위해 함께 작동하며, 전역 디렉터리 서비스(global directory service)를 형성한다.</p>
    <p>이 시스템은 트리 구조를 사용하며, 최상단에는 루트 서버(root servers)가 있고, 그 아래에는 최상위 도메인 서버(.com, .org 등), 특정 도메인에 대한 권한 있는 네임 서버(authoritative name servers), 그리고 로컬 DNS 서버가 이어진다.</p>
    <p>DNS는 인터넷이 동작하는 데 핵심적이며, 사용자가 숫자 IP 주소 대신 기억하기 쉬운 이름으로 웹사이트와 서비스에 접근할 수 있게 한다. 또한 이메일 라우팅, 서비스 디스커버리, 기타 네트워크 프로토콜도 지원한다.</p>
    <hr>
    <ul>
        <li><strong>사설망(Private Network):</strong> 외부 인터넷과 분리되거나 방화벽 등으로 격리된 네트워크로, 내부 자원 접근을 제한해 보안을 강화</li>
        <li><strong>네이밍 시스템(Naming System):</strong> 사람이 읽기 쉬운 이름(예: 도메인)을 기계가 이해하는 주소(IP 등)로 변환해 주는 서비스</li>
        <li><strong>쿼리(Query):</strong> DB나 네트워크 서비스에 정보를 요청하는 명령어 또는 질의로, 요청에 따라 결과 데이터를 반환받는다.</li>
        <li><strong>글로벌 디렉터리 서비스(Global Directory Service):</strong> 전사적·전지구적 자원(사용자 계정·장치·서비스) 정보를 통합 관리·검색할 수 있게 해 주는 분산 디렉터리로, LDAP 기반의 Active Directory 포리스트 등이 있다.</li>
    </ul>

</div>
</details>

<details>
<summary><span class="accordion-title"><a href="category/internet/browser.html">Browser</a> </span><span class="indicator">펼치기</span></summary>
<div class="accordion-content">
    <p>웹 브라우저(Web Browser)는 사용자가 월드 와이드 웹에서 정보를 접근, 검색, 탐색할 수 있도록 해주는 소프트웨어 애플리케이션이다.</p>
    <p>브라우저는 HTML, CSS, JavaScript를 해석하고 표시하여 웹 페이지를 렌더링한다. 현대의 브라우저인 Google Chrome, Mozilla Firefox, Apple Safari, Microsoft Edge는 <b>탭 브라우징, 북마크, 확장 기능, 기기 간 동기화</b>와 같은 기능을 제공한다. 또한 브라우저는 웹 콘텐츠를 처리하기 위해 <b>렌더링 엔진(예: Blink, Gecko, WebKit)</b>을 사용하고, JavaScript 코드를 실행하기 위해 <b>JavaScript 엔진</b>을 포함한다. 보안을 위해 <b>샌드박싱, HTTPS 강제, 팝업 차단</b> 같은 기능도 제공한다. 브라우저는 HTML5, CSS3, Web API 등 다양한 웹 표준과 기술을 지원하여 풍부하고 상호작용적인 웹 경험을 가능하게 한다.</p>
    <p>웹 애플리케이션이 점점 복잡해짐에 따라 브라우저는 성능, 보안, 사용자 경험을 균형 있게 제공하는 <b>강력한 플랫폼</b>으로 진화해 왔다.</p>
    <hr>
    <ul>
        <li><strong>렌더링: </strong> 브라우저가 HTML/CSS/JS를 해석해 시각적 요소로 변환해 화면에 출력하는 과정</li>
        <li><strong>렌더링 엔진:</strong> DOM·스타일 정보를 레이아웃·페인트 단계로 처리해 실제 픽셀을 그리는 브라우저 핵심 모듈</li>
        <li><strong>JavaScript 엔진:</strong> JS 코드를 파싱·컴파일·실행해 동적 기능과 로직을 처리하는 브라우저 구성 요소(예: V8, SpiderMonkey)</li>
        <li><strong>샌드박싱:</strong> 웹 콘텐츠 실행을 OS나 브라우저 수준에서 격리해 외부 시스템 침범을 방지하는 보안 메커니즘</li>
        <li><strong>HTML5:</strong> 시맨틱 태그, 멀티미디어, 로컬 저장소, 캔버스 등을 지원하는 HTML 표준의 최신 버전</li>
        <li><strong>CSS3:</strong> 애니메이션, 트랜지션, 그리드·Flex 레이아웃 등 모듈 기반 스타일링 기능이 확장된 CSS 표준 최신 버전</li>
        <li><strong>웹 경험:</strong> 페이지 로드·인터랙션·접근성·반응성·디자인 등 사용자가 웹사이트에서 체감하는 전체 품질과 만족도</li>
    </ul>

</div>
</details>
