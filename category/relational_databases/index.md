---
layout: default
title: "Relational Databases"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>Relational Databases</h2>
  <p>
    관계형 데이터베이스는 스키마를 사용하여 데이터 관계와 제약 조건을 정의하고, 행과 열로 구성된 구조화된 테이블로 데이터를 구성하는 데이터베이스 관리 시스템(DBMS)의 한 유형이다. 관계형 데이터베이스는 구조화된 질의 언어(SQL)를 사용하여 데이터를 쿼리하고 관리하며, 데이터 검색, 삽입, 업데이트, 삭제와 같은 작업을 지원한다. 관계형 데이터베이스는 키(기본 키와 외래 키)와 제약 조건(예: 고유 키, NOT-NULL)을 통해 데이터 무결성을 강화하며, 복잡한 쿼리, 트랜잭션 및 데이터 관계를 효율적으로 처리하도록 설계되었다. 관계형 데이터베이스의 예로는 MySQL, PostgreSQL, Oracle Database가 있다. 관계형 데이터베이스는 구조화된 데이터 저장, 강력한 일관성, 그리고 복잡한 쿼리 기능이 필요한 애플리케이션에 일반적으로 사용된다.
  </p>
</section>

<details open>
<summary>PostgreSQL <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>PostgreSQL은 견고성, 확장성, 그리고 표준 준수로 유명한 고급 오픈 소스 관계형 DB 관리 시스템(*RDBMS)이다. 복잡한 쿼리, *외래 키, 전체 텍스트 검색 등 다양한 데이터 유형과 고급 기능을 지원한다. PostgreSQL은 확장성이 뛰어나 사용자가 원하는 데이터 유형, 연산자, 함수를 직접 정의할 수 있다. 안정적인 *트랜잭션 처리를 위한 ACID(원자성, 일관성, 고립성, 지속성) 속성을 지원하고 *동시성 및 *데이터 무결성을 강력하게 지원한다. 이러한 기능 덕분에 간단한 웹 앱부터 대규모 *데이터 웨어하우징 및 분석 솔루션까지 다양한 애플리케이션에 적합하다.
  </p>
  <ul>
    <li><strong>RDBMS:</strong> 테이블 간 관계를 키로 관리하며 SQL로 데이터를 저장·조회·관리하는 관계형 DB 관리 시스템</li>
    <li><strong>외래 키:</strong> 한 테이블의 컬럼이 다른 테이블의 기본 키를 참조해 테이블 간 참조 무결성을 유지하는 제약</li>
    <li><strong>트랜잭션:</strong> 여러 DB 연산을 하나의 단위로 묶어 모두 성공하거나 모두 실패하도록 보장하는 작업 단위</li>
    <li><strong>동시성:</strong> 여러 트랜잭션이 동시에 실행될 때 데이터 일관성과 무결성을 지키며 처리하는 기법</li>
    <li><strong>데이터 무결성:</strong> 제약조건·비즈니스 규칙을 통해 데이터가 정확하고 일관되게 유지되는 상태</li>
    <li><strong>데이터 웨어하우징:</strong> 다양한 소스의 대규모 데이터를 통합·저장해 OLAP 분석과 의사결정 지원에 최적화한 저장소</li>
    <ul>
      <li>OLAP(Online Analytical Processing): 데이터 웨어하우스 위에서 다차원 큐브 구조로 대량의 데이터를 빠르게 분석·집계하는 기술</li>
    </ul>
  </ul>
</div>
</details>

<details>
<summary>MySQL <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>MySQL은 빠른 속도, 안정성, 그리고 사용 편의성으로 유명한 오픈 소스 관계형 DB 관리 시스템(RDBMS)이다. DB 상호작용에 *SQL(구조적 질의 언어)을 사용하고 트랜잭션, *인덱싱, *저장 프로시저 등 다양한 데이터 관리 기능을 지원한다. MySQL은 확장성과 유연성 덕분에 웹 애플리케이션, 데이터 웨어하우징 등 다양한 애플리케이션에 널리 사용된다. 다양한 프로그래밍 언어 및 플랫폼과 원활하게 통합되며, LAMP(Linux, Apache, MySQL, PHP/Python/Perl)와 같은 인기 소프트웨어 스택의 웹 서버 및 프레임워크와 함께 사용되는 경우가 많다. MySQL은 Oracle Corporation에서 관리하며, 개발 및 사용을 지원하는 광범위한 커뮤니티와 생태계를 보유하고 있다.
  </p>
  <ul>
    <li><strong>SQL(Structured Query Language):</strong> 관계형 DB에서 데이터 조회·삽입·수정·삭제 및 스키마 정의를 표준화된 문법으로 수행하는 질의 언어</li>
    <li><strong>인덱싱:</strong> 테이블의 특정 컬럼에 색인을 생성해 검색 키를 빠르게 조회함으로써 쿼리 성능을 크게 향상시키는 기법</li>
    <li><strong>저장 프로시저:</strong> 미리 컴파일된 SQL 문들의 집합으로, 복잡한 로직을 서버 측에서 재사용·일괄 실행해 성능과 보안을 강화하는 DB 객체</li>
  </ul>
</div>
</details>

<details>
<summary>MariaDB <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>MariaDB 서버는 MySQL 서버의 커뮤니티 개발 *포크이다. 초기 MySQL 팀의 핵심 멤버들이 시작한 MariaDB는 외부 개발자들과 적극적으로 협력하여 업계에서 가장 풍부한 기능, 안정성, 그리고 합리적인 라이선스를 갖춘 오픈 SQL 서버를 제공한다. MariaDB는 MySQL의 더욱 다재다능하고 즉시 사용 가능한 대체 버전을 목표로 개발되었다.
  </p>
  <ul>
    <li><strong>포크(Fork):</strong> 오픈소스 프로젝트의 코드베이스를 복제해 새로운 독립 개발 라인을 만드는 행위</li>
  </ul>
</div>
</details>

<details>
<summary>MS SQL <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>Microsoft SQL Server(MS SQL)는 Microsoft에서 구조화된 데이터를 관리하고 저장하기 위해 개발한 관계형 DB 관리 시스템입니다. 쿼리, 트랜잭션 관리, 데이터 웨어하우징 등 광범위한 데이터 작업을 지원한다. SQL Server는 *T-SQL(Transact-SQL)을 통한 복잡한 쿼리 지원, SQL Server Integration Services(*SSIS)와의 데이터 통합, SQL Server Analysis Services(*SSAS) 및 SQL Server Reporting Services(*SSRS)와의 *비즈니스 인텔리전스 등 데이터베이스 설계, 성능 최적화, 보안을 위한 도구와 기능을 제공한다. 안정적인 데이터 저장, 트랜잭션 처리 및 보고가 필요한 *엔터프라이즈 환경에서 일반적으로 사용된다.
  </p>
  <ul>
    <li><strong>T-SQL:</strong> Microsoft SQL Server의 확장 SQL 언어로, 변수·제어문·저장 프로시저 등 프로그래밍 기능을 지원</li>
    <li><strong>SSIS:</strong> 데이터 추출·변환·적재(ETL)를 자동화해 다양한 소스 간 데이터 흐름을 관리하는 도구</li>
    <li><strong>SSAS:</strong> OLAP 큐브와 데이터 마이닝 모델로 다차원 분석을 제공해 대규모 데이터에서 인사이트를 도출</li>
    <li><strong>SSRS:</strong> 표·차트·대시보드 형태의 보고서를 생성·배포·관리하는 서버 기반 보고 솔루션</li>
    <li><strong>비즈니스 인텔리전스(BI):</strong> 기업 데이터 수집·분석·시각화를 통해 의사결정과 전략 수립을 지원하는 프로세스 및 기술</li>
    <li><strong>엔터프라이즈 환경:</strong> 대규모 조직의 복잡한 네트워크·데이터베이스·보안 요구를 충족하는 통합 IT 인프라 및 운영 구조</li>
  </ul>
</div>
</details>

<details>
<summary>Oracle <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>Oracle Database는 Oracle Corporation에서 개발한 매우 강력한 엔터프라이즈급 관계형 DB 관리 시스템(RDBMS)입니다. 확장성, 안정성, 그리고 포괄적인 기능으로 유명한 Oracle Database는 복잡한 데이터 관리 작업과 미션 크리티컬 애플리케이션을 지원한다. SQL 쿼리, 트랜잭션 관리, *클러스터링을 통한 *고가용성, 데이터 웨어하우징과 같은 고급 기능을 제공한다. Oracle 데이터베이스 솔루션은 관계형, 공간형, 그래프형 등 다양한 데이터 모델을 지원하고 보안, 성능 최적화, 데이터 통합을 위한 도구를 제공한다. 대규모의 안전하고 고성능 데이터 처리가 필요한 산업에서 널리 사용되고 있다.
  </p>
  <ul>
    <li><strong>클러스터링:</strong> 여러 대의 서버(노드)를 하나의 논리적 시스템으로 묶어 부하를 분산하고, 특정 노드 장애 시 자동 대체로 내결함성을 확보하는 기술</li>
    <li><strong>고가용성:</strong> 서비스 중단 없이 지속적으로 운영되도록 중복 구성·장애 감지·페일오버 메커니즘을 설계해 시스템 가동 시간을 극대화하는 설계 기법</li>
  </ul>
</div>
</details>

<details>
<summary>SQLite <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>SQLite는 가볍고 *서버리스이며 자체적으로 동작하는 SQL DB 엔진으로, 간편성과 효율성을 고려하여 설계되었다. 모바일 앱, 데스크톱 애플리케이션, 중소 규모 웹사이트 등 모든 기능을 갖춘 DB 서버가 필요하지 않은 *임베디드 시스템 및 애플리케이션에 널리 사용된다. SQLite는 데이터를 *단일 파일에 저장하므로 배포 및 관리가 용이하다. 표준 SQL 쿼리를 지원하고 ACID(원자성, 일관성, 격리성, 내구성)를 준수하여 데이터 무결성을 보장한다. SQLite는 작은 설치 공간, 최소한의 구성, 그리고 사용 편의성 덕분에 컴팩트하면서도 고성능 DB 솔루션이 필요한 애플리케이션에 널리 사용된다.
  </p>
  <ul>
    <li><strong>서버리스(Serverless):</strong> 클라우드 제공자가 인프라 관리를 대신해 주고, 개발자는 함수(Function) 단위로 코드만 배포하면 자동 확장·종량 과금되는 실행 모델</li>
    <li><strong>임베디드 시스템(Embedded System):</strong> 가전·자동차·산업 장비 등에 내장되어 특정 기능을 수행하는 소형·저전력 컴퓨팅 시스템으로, 펌웨어나 실시간 OS로 제어된다.</li>
    <li><strong>단일 파일(Single-file):</strong> 애플리케이션의 코드와 리소스를 하나의 실행 파일 또는 스크립트에 모두 포함해 배포·실행하는 방식으로, 설치 없이 간편하게 실행 가능</li>
  </ul>
</div>
</details>
