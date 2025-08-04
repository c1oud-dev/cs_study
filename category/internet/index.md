---
layout: default
title: "Internet"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>Internet</h2>
  <p>
    인터넷은 표준화된 프로토콜, 주로 TCP/IP를 사용하여 통신하는 상호 연결된 컴퓨터들의 글로벌 네트워크이다.
    사용자가 웹페이지를 요청하면, 사용자의 기기는 인터넷 서비스 제공업체(ISP)를 통해 DNS 서버로 데이터 패킷을 전송한다.DNS 서버는 웹사이트의 도메인 이름을 IP 주소로 변환한다. 이 패킷은 라우터와 스위치를 사용하는 다양한 네트워크를 거쳐 목적지 서버로 라우팅 되고, 목적지 서버는 요청을 처리하여 응답을 보낸다. 이러한 양방향 교환을 통해 웹페이지, 이메일, 파일 등의 데이터 전송이 가능해져 인터넷은 글로벌 커뮤니케이션을 위한 역동적이고 분산된 시스템이 된다.
  </p>
</section>

<details open>
  <summary><a href="category/internet/http.html">HTTP</a> <span class="indicator">접기</span></summary>
  <div class="accordion-content">
    <p>HTTP(Hypertext Transfer Protocol)는 *월드 와이드 웹(WWW)을 통해 *하이퍼텍스트를 전송하는 데
        사용되는 *프로토콜이다. HTTP는 메시지의 형식과 전송 방식, 그리고 *웹 서버와 *브라우저가 다양한 
        명령에 응답하는 방식을 정의한다. HTTP는 요청-응답 모델로 작동한다. 클라이언트(일반적으로 웹 브라우저)
        가 웹 페이지나 파일과 같은 리소스에 대한 HTTP 요청을 서버에 보내면 서버는 요청된 콘텐츠와 요청
        결과를 나타내는 *HTTP 상태 코드로 응답한다. HTTP는 *상태 비저장(stateless) 프로토콜로, 클라이언트에서
        서버로 보내는 각 요청은 독립적이며 이전 상호작용에 대한 정보를 유지하지 않는다. HTTP는 웹에서
        데이터 통신의 기반을 형성하며, 일반적으로 암호화된 통신을 위해 HTTP(HTTPS)와 함께 사용된다.
        </p>
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
<summary><a href="category/internet/domain_name.html">Domain Name</a> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
        <p>도메인 이름은 인터넷에서 특정 위치를 식별하는 데 사용되는 사람이 읽을 수 있는 주소로, 웹 사이트와
        온라인 서비스에 쉽게 접근할 수 있도록 한다. *IP 주소는 컴퓨터가 서버를 찾고 연결하는 데 사용하는
        숫자 식별자이다. 도메인 이름은 두 가지 주요 부분으로 구성된다. 2차 도메인(예: "example.com"의
        "example")과 최상위 도메인(예: "com")이다. 도메인 이름은 도메인 이름 등록 기관에서 관리하며,
        웹사이트를 구축하는 데 필수적이며, 숫자 IP 주소 대신 사용자 친화적인 방식으로 웹사이트를 탐색할
        수 있도록 한다.
    </p>

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
<summary><a href="category/internet/hosting.html">Hosting</a> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
    <p>호스팅은 인터넷을 통해 사용자에게 웹사이트 파일과 애플리케이션을 저장하고 전송하기 위한 서버 공간과 
    리소스를 제공하는 서비스를 말한다. 호스팅 제공업체는 웹사이트와 애플리케이션이 온라인에서 접근 가능
    하도록 하는 데 필요한 서버, *스토리지, 네트워크 연결 등의 *인프라를 제공한다. 호스팅에는 여러 웹사이트가 
    하나의 서버를 공유하는 공유 호스팅, *가상 사설 서버(VPS), 한 명의 사용자에게 하나의 서버가 전용으로 
    제공되는 전용 호스팅, 그리고 서버 네트워크를 사용하여 확장 가능한 리소스를 제공하는 클라우드 호스팅 
    등 다양한 유형이 있다. 호스팅 서비스에는 웹사이트의 안정적인 *가용성과 원활한 성능을 보장하기 위해 
    도메인 등록, 보안 기능, 기술 지원이 포함되는 경우가 많다.
</p>

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
<summary><a href="category/internet/dns.html">DNS</a> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
    <p>DNS(도메인 이름 시스템)는 인터넷이나 *사설망에 연결된 컴퓨터, 서비스 또는 기타 리소스에 대한 계층적이고 
    분산된 *네이밍 시스템이다. 사람이 읽을 수 있는 도메인 이름(예: www.example.com)을 컴퓨터가 서로를 
    식별하는 데 사용하는 IP 주소(예: 192.0.2.1)로 변환한다. 전 세계에 분산된 DNS 서버들이 이러한 *쿼리를 
    해결하기 위해 협력하여 *글로벌 디렉터리 서비스를 형성한다. 이 시스템은 최상위에 루트 서버가 있고, 그 
    아래에는 최상위 도메인 서버(.com, .org 등), 특정 도메인에 대한 권한 있는 네임 서버, 그리고 로컬 DNS 
    서버가 있는 트리 구조를 사용한다. DNS는 인터넷 작동에 필수적이며, 사용자가 숫자 IP 주소 대신 기억하기 
    쉬운 이름을 사용하여 웹사이트와 서비스에 액세스할 수 있도록 한다. 또한 이메일 라우팅, 서비스 검색 및 
    기타 네트워크 프로토콜을 지원한다.
</p>

<ul>
    <li><strong>사설망(Private Network):</strong> 외부 인터넷과 분리되거나 방화벽 등으로 격리된 네트워크로, 내부 자원 접근을 제한해 보안을 강화</li>
    <li><strong>네이밍 시스템(Naming System):</strong> 사람이 읽기 쉬운 이름(예: 도메인)을 기계가 이해하는 주소(IP 등)로 변환해 주는 서비스</li>
    <li><strong>쿼리(Query):</strong> DB나 네트워크 서비스에 정보를 요청하는 명령어 또는 질의로, 요청에 따라 결과 데이터를 반환받는다.</li>
    <li><strong>글로벌 디렉터리 서비스(Global Directory Service):</strong> 전사적·전지구적 자원(사용자 계정·장치·서비스) 정보를 통합 관리·검색할 수 있게 해 주는 분산 디렉터리로, LDAP 기반의 Active Directory 포리스트 등이 있다.</li>
</ul>

</div>
</details>

<details>
<summary><a href="category/internet/browser.html">Browser</a> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
    <p>웹 브라우저는 사용자가 월드 와이드 웹(WWW)의 정보에 접근하고, 검색하고, 탐색할 수 있도록 하는 소프트웨어 
    애플리케이션이다. HTML, CSS, JavaScript를 해석하고 표시하여 웹 페이지를 *렌더링한다. Google Chrome, 
    Mozilla Firefox, Apple Safari, Microsoft Edge와 같은 최신 브라우저는 탭 브라우징, 북마크, 확장 
    프로그램, 기기 간 동기화 등의 기능을 제공한다. 웹 콘텐츠를 처리하는 *렌더링 엔진(예: Blink, Gecko, WebKit)과 
    코드 실행을 위한 *JavaScript 엔진을 통합한다. 또한 *샌드박싱, HTTPS 적용, 팝업 차단 등의 기능을 통해 보안을 
    관리한다. *HTML5, *CSS3, 웹 API 등 다양한 웹 표준과 기술을 지원하여 풍부하고 인터랙티브한 *웹 경험을 제공한다. 
    웹 애플리케이션의 복잡성이 증가함에 따라 브라우저는 끊임없이 변화하는 인터넷 환경에서 성능, 보안, 사용자 경험의 
    균형을 맞추는 강력한 플랫폼으로 발전했다.
</p>

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
