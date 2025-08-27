---
layout: default
title: "Search Engines"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>Search Engines</h2>
  <p>Elasticsearch 같은 검색 엔진은 <b>대량의 데이터를 빠르고, 확장 가능하며, 유연하게 검색·분석</b>하기 위해 설계된 특화된 도구이다.</p>
  <p>Elasticsearch는 <b>오픈 소스 분산 검색 및 분석 엔진</b>으로, <b>Apache Lucene</b> 위에 구축되었으며, <b>전문(full-text) 검색 기능, 실시간 인덱싱, 고급 쿼리 기능</b>을 제공한다.</p>
  <p>검색 엔진(예: Elasticsearch)의 주요 특징은 다음과 같다.</p>
  <ol>
    <li><strong>전문 검색(Full-Text Search):</strong> 관련성 점수(relevance scoring)와 텍스트 분석을 포함한 복잡한 검색 쿼리를 지원한다.</li>
    <li><strong>분산 아키텍처(Distributed Architecture):</strong> 여러 노드나 서버에 걸친 수평적 분산을 통해 확장성을 제공한다.</li>
    <li><strong>실시간 인덱싱(Real-Time Indexing):</strong> 데이터를 거의 즉시 인덱싱하고 검색할 수 있다.</li>
    <li><strong>강력한 Query DSL:</strong> 복잡한 쿼리를 작성하고 실행할 수 있는 도메인 특화 언어를 제공한다.</li>
    <li><strong>분석 기능(Analytics):</strong> 집계 및 데이터 분석 기능을 제공하며, 로그 및 이벤트 데이터 분석에 자주 사용된다.</li>
  </ol>
</section>

<!-- 설명 -->
<details open>
<summary><span class="accordion-title">Elasticsearch </span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
    <p>Elasticsearch의 핵심은 <b>문서 지향(document-oriented) 검색 엔진</b>이다. 이는 <b>문서 기반 데이터베이스</b>로서, 저장된 레코드에 대해 <b>삽입(INSERT), 삭제(DELETE), 조회(RETRIEVE)</b>는 물론 <b>분석(Analytics)</b>까지 수행할 수 있다. 하지만 Elasticsearch는 과거에 사용해본 일반적인 범용 데이터베이스와는 다르다. 본질적으로는 <b>검색 엔진</b>이며, 저장된 데이터를 <b>검색 조건에 맞게 초고속으로 조회</b>할 수 있는 다양한 기능을 제공한다.</p>
    <p><strong>📝정리: Elasticsearch는 문서 기반 검색 엔진이자 데이터베이스로, 단순 저장소가 아닌 초고속 검색과 분석 기능을 제공한다.</strong></p>
</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title">Solr </span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
    <p>Solr는 <b>오픈 소스이자 고도로 확장 가능한 검색 플랫폼</b>으로, <b>Apache Lucene</b> 위에 구축되었으며, <b>전문 검색(full-text search), 패싯 검색(faceted search), 실시간 인덱싱</b>을 위해 설계되었다. Solr는 대량의 데이터를 <b>고성능·고관련성(relevance)</b>으로 인덱싱하고 쿼리할 수 있는 강력한 기능을 제공한다. 또한 <b>복잡한 쿼리, 분산 검색, 고급 텍스트 분석(토크나이징, 스테밍 등)</b>을 지원한다.</p>
    <p>추가 기능으로는 <b>패싯 검색, 하이라이팅, 위치 기반 검색(geographic search)</b>이 있으며, <b>전자상거래, 콘텐츠 관리 등 다양한 애플리케이션</b>에서 검색 엔진 및 데이터 검색 시스템 구축에 널리 사용된다.</p>
    <p><strong>📝정리: Solr는 Lucene 기반 오픈 소스 검색 플랫폼으로, 전문·패싯 검색과 실시간 인덱싱, 고급 텍스트 분석을 지원하여 대규모 검색 시스템에 활용된다.</strong></p>
    <!-- 가로선 추가 -->
    <hr>
    <ul>
        <li><strong>패싯 검색(Faceted Search):</strong> 패싯 검색은 검색 결과를 <b>카테고리(속성)</b>별로 그룹화하여 사용자가 원하는 조건을 점점 좁혀가며 탐색할 수 있게 해주는 검색 방식이다.</li>
    </ul>
</div>
</details>
