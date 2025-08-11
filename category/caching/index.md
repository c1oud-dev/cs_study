---
layout: default
title: "Caching"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>Caching</h2>
  <p>
    Caching은 컴퓨팅에서 자주 액세스하는 데이터를 빠르게 저장하고 검색하여 느린 원본 소스에서 반복적으로 가져올 필요성을 줄이는 데 사용되는 기술이다. 주 저장소보다 액세스 속도가 빠른 위치에 데이터 사본을 보관하는 것을 의미한다. 캐싱은 브라우저 캐싱, 애플리케이션 수준 캐싱, 데이터베이스 캐싱 등 다양한 수준에서 수행될 수 있다. 지연 시간을 줄이고, 네트워크 트래픽을 줄이며, 서버 또는 데이터베이스의 부하를 줄여 성능을 크게 향상시킨다. 일반적인 캐싱 전략에는 시간 기반 만료, 가장 최근에 사용된(LRU) 알고리즘, 연속 쓰기(write-through) 또는 다시 쓰기(write-back) 정책이 있다. 캐싱은 속도와 효율성을 향상시키지만, 데이터 일관성과 최신성을 유지하는 데 어려움을 야기한다. 효과적인 캐시 관리는 동적 시스템에서 성능 향상과 최신 정보 유지의 균형을 맞추는 데 매우 중요하다.
  </p>
  <p><strong>정리: Caching은 자주 쓰는 데이터를 미리 저장해 두어 빠르게 재사용하는 성능 최적화 기법이다.</strong></p>
</section>

<details open>
<summary><span class="accordion-title">Server Side</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  Server-side caching은 자주 액세스하는 데이터를 서버의 메모리에 저장하여 반복적인 데이터 검색이나 계산의 필요성을 줄임으로써 애플리케이션 성능을 향상시키는 기술이다. 이러한 접근 방식은 응답 시간을 단축하고 데이터베이스 및 기타 백엔드 서비스의 부하를 줄이는 데 도움이 된다. 일반적인 방법으로는 데이터베이스 쿼리 결과, *HTML 조각, API 응답을 캐싱하는 것이 있다. 널리 사용되는 서버 측 캐싱 도구 및 기술로는 Redis, Memcached, 그리고 웹 프레임워크에 내장된 *캐싱 메커니즘이 있다. 서버 측 캐싱은 캐시된 콘텐츠를 효율적으로 관리하고 제공함으로써 애플리케이션의 확장성과 응답성을 향상시킨다.
  </p>
  <p><strong>정리: Server-side caching은 서버에서 데이터를 미리 저장해 두어 클라이언트 요청 시 빠르게 전달하는 방식이다.</strong></p>

  <ul>
    <li><strong>HTML 조각:</strong> 웹 페이지의 일부(헤더, 네비게이션, 댓글 목록 등)를 캐싱해 전체 페이지를 다시 렌더링하지 않고 빠르게 제공</li>
    <li><strong>캐싱 메커니즘:</strong> 메모리(Redis, Memcached), 디스크, CDN 등을 사용해 캐시 저장·갱신·만료를 관리하는 방식</li>
  </ul>

  <!-- 박스 추가 -->
  <details>
    <summary><span class="accordion-title">Redis </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      Redis는 빠른 속도와 다재다능함으로 유명한 오픈소스 *인메모리 데이터 구조 저장소이다. 문자열, 리스트, 셋, 해시, 정렬된 셋 등 다양한 데이터 유형을 지원하고 캐싱, 세션 관리, 실시간 분석, *메시지 브로커링 등의 기능을 제공한다. Redis는 키-값 저장소로 작동하여 빠른 읽기 및 쓰기 작업을 지원하며, 애플리케이션의 성능과 확장성을 향상시키는 데 자주 사용된다. 디스크에 데이터를 저장하는 지속성 옵션, 고가용성을 위한 복제, 그리고 수평적 확장을 위한 *클러스터링을 지원한다. Redis는 데이터 액세스 지연 시간이 짧고 처리량이 높은 환경에서 널리 사용된다.
      </p>
      <p><strong>정리: Redis는 인메모리 기반의 고속 데이터 저장소로, 캐시·데이터베이스·메시지 브로커 역할을 수행한다.</strong></p>
      <ul>
        <li><strong>인메모리:</strong> 데이터를 디스크가 아닌 메모리에 저장해 읽기·쓰기 속도가 매우 빠른 방식</li>
        <li><strong>메시지 브로커링:</strong> Pub/Sub 구조로 서비스 간 메시지를 중계하고 비동기 통신을 가능하게 함</li>
        <li><strong>클러스터링:</strong> 데이터를 여러 노드에 분산 저장·처리하여 성능과 확장성을 높이고 장애 복구를 지원</li>
      </ul>
    </div>
  </details>

  <details>
    <summary><span class="accordion-title">Memcached </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      Memcached(다양한 발음은 mem-cash-dee 또는 mem-cashed)는 범용 분산 메모리 캐싱 시스템이다. *동적 데이터베이스 기반 웹사이트의 속도를 높이기 위해 데이터와 객체를 *RAM에 캐싱하여 외부 데이터 소스(예: DB 또는 API)를 읽어야 하는 횟수를 줄이는 데 자주 사용된다. Memcached는 개정된 *BSD 라이선스에 따라 라이선스가 부여된 무료 오픈 소스 SW이다. Memcached는 *Unix 계열 운영 체제(*Linux 및 macOS)와 Microsoft Windows에서 실행된다. *libevent 라이브러리에 따라 실행 여부가 결정됩니다 . Memcached의 API는 여러 머신에 분산된 매우 큰 해시 테이블을 제공한다. 테이블이 가득 차면 후속 삽입 작업으로 인해 오래된 데이터가 가장 오래 전에 사용된 것(*LRU) 순으로 삭제된다. Memcached를 사용하는 애플리케이션은 일반적으로 요청 및 추가 작업을 RAM에 저장한 후 DB와 같은 느린 백업 저장소로 대체한다.
      </p>
      <p><strong>정리: Memcached는 RAM 기반의 분산 캐시 시스템으로, 동적 웹 애플리케이션의 DB 부하를 줄여 성능을 높인다.</strong></p>
      <ul>
        <li><strong>동적 DB:</strong> 요청 시마다 실시간으로 데이터를 생성·조회하는 데이터베이스</li>
        <li><strong>RAM:</strong> 휘발성 메모리로, 디스크보다 훨씬 빠른 읽기·쓰기 속도를 제공</li>
        <li><strong>BSD 라이선스:</strong> 수정·배포가 자유로운 오픈소스 라이선스.</li>
        <li><strong>Unix:</strong> 안정성과 멀티태스킹에 강한 다중 사용자 운영체제</li>
        <li><strong>Linux:</strong> Unix 계열의 오픈소스 운영체제</li>
        <li><strong>libevent 라이브러리:</strong> 비동기 이벤트 기반 네트워크 프로그래밍을 위한 C 라이브러리</li>
        <li><strong>LRU(Least Recently Used):</strong> 가장 오래 사용되지 않은 데이터를 먼저 제거하는 캐시 교체 알고리즘</li>
      </ul>
    </div>
  </details>

</div>
</details>

<details>
<summary><span class="accordion-title">CDN (Content Delivery Network) </span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  콘텐츠 전송 네트워크(CDN) 서비스는 웹사이트의 고가용성 및 성능 향상을 목표로 한다. 이는 일반적으로 클라이언트 요청과 지리적으로 더 가까운 엔드포인트를 통해 웹사이트 자산과 콘텐츠를 빠르게 전송함으로써 달성된다.
  기존 상용 CDN(Amazon CloudFront, Akamai, CloudFlare, Fastly)은 이러한 목적으로 사용할 수 있는 전 세계 서버를 제공한다. CDN을 통해 자산과 콘텐츠를 제공하면 웹사이트 호스팅 대역폭을 줄이고, 추가적인 캐싱 계층을 제공하여 잠재적인 서비스 중단을 줄이며, 웹사이트 보안도 강화할 수 있다.
  </p>
  <p><strong>정리: CDN은 전 세계에 분산된 서버 네트워크로, 사용자와 가까운 위치에서 콘텐츠를 제공해 속도와 안정성을 높인다.</strong></p>

  <ul>
    <li><strong>엔드포인트:</strong> 클라이언트가 요청을 보내고 응답을 받는 네트워크 접속 지점</li>
      <ul><li>예: API URL, CDN 서버 주소</li></ul>
  </ul>

</div>
</details>

<details>
<summary><span class="accordion-title">Client Side Caching </span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  Client Side Caching은 웹 브라우저나 애플리케이션이 성능을 향상시키고 서버 부하를 줄이기 위해 사용자 기기에 데이터를 로컬로 저장하는 기술이다. 웹 페이지, 이미지, 스크립트 및 기타 리소스의 사본을 클라이언트 시스템에 저장하여 후속 방문 시 더 빠르게 액세스할 수 있도록 한다. 최신 브라우저는 HTTP 캐싱(Cache-Control 및 ETag와 같은 헤더 사용), 오프라인 기능을 위한 서비스 워커, 로컬 스토리지 API 등 다양한 캐싱 메커니즘을 구현한다. 클라이언트 측 캐싱은 네트워크 트래픽과 로드 시간을 크게 줄여 특히 느린 연결 환경에서 사용자 경험을 향상시킨다. 하지만 성능 향상과 최신 콘텐츠 제공의 필요성 사이에서 균형을 맞추기 위해서는 신중한 관리가 필요하다. 개발자는 적절한 캐시 무효화 전략을 구현하고 중요한 업데이트에 대한 캐시 버스팅(cache-busting) 기법을 고려해야 한다. 효과적인 클라이언트 측 캐싱은 서버 리소스 사용량을 최소화하면서 반응성이 뛰어나고 효율적인 웹 애플리케이션을 구축하는 데 필수적이다.
  </p>
  <p><strong>정리: Client Side Caching은 브라우저나 앱이 데이터를 로컬에 저장해 서버 요청 없이 빠르게 재사용하는 방식이다.</strong></p>

  <ul>
    <li><strong>서비스 워커(Service Worker):</strong> 브라우저 백그라운드에서 동작하며, 네트워크 요청 가로채기·오프라인 캐시·푸시 알림 등을 처리하는 스크립트</li>
    <li><strong>로컬 스토리지 API(Local Storage API):</strong> 브라우저에 키-값 형태로 데이터를 영구 저장할 수 있는 웹 스토리지 API</li>
    <li><strong>캐시 버스팅(Cache Busting):</strong> 파일 이름에 버전이나 해시 값을 붙여 브라우저가 오래된 캐시를 사용하지 않고 최신 파일을 받아오게 하는 기법</li>
  </ul>

</div>
</details>
