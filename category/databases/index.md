---
layout: default
title: "Databases"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>Databases</h2>
  <p>
    DB는 하나 이상의 관련 조직에서 수집된 유용한 데이터를 조직의 자산으로 활용할 수 있도록 구조화한 것이다. 데이터베이스 관리 시스템은 방대한 양의 데이터를 적시에 관리하고 추출할 수 있도록 설계된 소프트웨어이다.
  </p>
  <p><strong>정리: 데이터베이스는 데이터를 구조적으로 저장·관리하여 효율적인 검색·수정·보안을 가능하게 하는 시스템이다.</strong></p>
</section>

<details open>
<summary><span class="accordion-title">ORMs</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  객체 관계 매핑(ORM)은 개발자가 객체 지향 프로그래밍 개념을 사용하여 *관계형 데이터베이스와 상호 작용할 수 있도록 하는 프로그래밍 기법이다. ORM 프레임워크는 DB 테이블을 클래스에, 행을 객체에 매핑하여 개발자가 *원시 SQL 쿼리를 작성하는 대신 객체를 통해 DB 작업을 수행할 수 있도록 한다. 이러한 추상화는 DB 상호 작용을 애플리케이션의 객체 모델에 맞춰 조정함으로써 데이터 조작을 간소화하고 코드 유지 관리성을 향상시킨다. ORM 도구는 객체와 DB 스키마 간의 변환을 처리하고, 관계를 관리하며, 지연 로딩 및 캐싱과 같은 기능을 제공하는 경우가 많다. 널리 사용되는 ORM 프레임워크로는 Java용 *Hibernate, .NET용 *Entity Framework, Python용 *SQLAlchemy가 있다.
  </p>
  <p><strong>정리: ORM(Object-Relational Mapping)은 객체 지향 언어의 객체와 관계형 데이터베이스의 테이블을 매핑해 SQL 없이 데이터 조작을 가능하게 하는 기술이다.</strong></p>

  <ul>
    <li><strong>관계형 데이터베이스(RDB):</strong> 데이터를 행(ROW)과 열(COLUMN)로 구성된 테이블 형태로 저장하고, 테이블 간 관계를 키(KEY)로 연결하는 DB.</li>
    <li><strong>원시 SQL 쿼리:</strong> 프로그래밍 언어 코드와 별도로 직접 작성하는 SQL 문으로, SELECT·INSERT·UPDATE·DELETE 같은 명령을 사용해 데이터 조작.</li>
    <li><strong>Hibernate:</strong> Java 진영에서 가장 널리 쓰이는 ORM 프레임워크로, 객체와 테이블 매핑, 캐싱, 트랜잭션 관리 등을 지원.</li>
    <li><strong>Entity Framework(EF):</strong> .NET 환경에서 ORM 기능을 제공하는 프레임워크로, LINQ(Language Integrated Query)로 데이터 접근 가능.</li>
    <li><strong>SQLAlchemy:</strong> Python에서 사용하는 강력하고 유연한 ORM 및 SQL 툴킷으로, ORM 방식과 원시 SQL 방식을 모두 지원.</li>
  </ul>

</div>
</details>

<details>
<summary><span class="accordion-title">ACID </span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  ACID는 데이터베이스 트랜잭션의 안정적인 처리를 보장하는 네 가지 핵심 속성을 나타내는 약어이다. 원자성(Atomicity), 일관성(Consistency), 고립성(Isolation), 지속성(Durability)의 약자이다. 
  <ul>
    <li>원자성은 트랜잭션이 완전히 완료되거나 완전히 실패하는 단일의 분리할 수 없는 단위로 처리되도록 보장한다.</li> 
    <li>일관성은 트랜잭션 전후에 DB를 유효한 상태로 유지한다.</li>
    <li>고립성은 동시에 실행되는 트랜잭션들이 서로 간섭하지 않고 순차적으로 실행되는 것처럼 보이도록 보장한다.</li>
    <li>지속성은 트랜잭션이 커밋되면 시스템 장애 발생 시에도 커밋된 상태가 유지되도록 보장한다.</li>
  </ul> 
  이러한 속성은 DB 시스템의 데이터 무결성과 안정성을 유지하는 데 매우 중요하며, 특히 여러 트랜잭션이 동시에 진행되거나 금융 시스템이나 전자상거래 플랫폼처럼 데이터 정확성이 중요한 상황에서 더욱 중요하다.
  </p>
  <p><strong>정리: ACID는 데이터베이스 트랜잭션이 안정성과 일관성을 보장하기 위해 지켜야 하는 원자성·일관성·격리성·지속성을 의미한다.</strong></p>

</div>
</details>

<details>
<summary><span class="accordion-title">Transactions </span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  DB 시스템에서 트랜잭션은 데이터 무결성과 일관성을 보장하기 위해 단일 원자 단위로 실행되는 일련의 작업이다. 트랜잭션은 ACID 속성을 따른다. 
  <ul>
  <li>원자성은 모든 작업이 성공적으로 완료되거나 아무것도 적용되지 않도록 보장한다.</li>
  <li>일관성은 DB의 유효한 상태를 유지합니다. 격리성은 트랜잭션 간 간섭을 방지한다.</li>
  <li>내구성은 트랜잭션이 커밋되면 변경 사항이 영구적으로 유지됨을 보장한다.</li>
  </ul>  
  이러한 속성은 DB가 동시 작업을 안정적으로 처리하고 장애 발생 시에도 정확하고 일관된 데이터를 유지하도록 보장한다.
  </p>
  <p><strong>정리: 트랜잭션은 데이터베이스에서 여러 작업을 하나의 단위로 묶어 모두 성공하거나 모두 실패하도록 보장하는 기능이다.</strong></p>
</div>
</details>


<details>
<summary><span class="accordion-title">N+1 Problem </span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  N+1 Problem은 DB 쿼리에서 애플리케이션이 항목 목록을 검색하는 쿼리를 수행한 후, 각 항목에 대한 관련 데이터를 개별적으로 가져오기 위해 추가 쿼리를 실행할 때 발생한다. 이는 검색된 항목 수에 비례하여 실행되는 쿼리 수가 증가하기 때문에 비효율성과 성능 문제를 야기하는 경우가 많다. 예를 들어, 애플리케이션이 항목 10개를 검색한 후 각 항목에 대해 관련 세부 정보를 가져오기 위해 추가 쿼리를 실행하면, 목록 쿼리 1개와 세부 정보 쿼리 10개, 총 11개의 쿼리가 실행되어 2개가 아닌 11개의 쿼리가 실행된다. 이는 특히 대용량 데이터 세트의 경우 성능에 심각한 영향을 미칠 수 있다. N+1 문제에 대한 해결책은 일반적으로 조인이나 일괄 처리 기법을 사용하여 관련 데이터를 더 적은 수의 효율적인 쿼리로 검색하도록 쿼리를 최적화하는 것이다.
  </p>
  <p><strong>정리: N+1 문제는 하나의 쿼리 실행 후 관련 데이터를 가져오기 위해 N번의 추가 쿼리가 발생해 성능이 저하되는 문제다.</strong></p>

</div>
</details>


<details>
<summary><span class="accordion-title">Database Normalization </span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  데이터베이스 정규화(Normalization)는 데이터 중복을 줄이고 데이터 무결성을 향상시키기 위해 일련의 소위 정규형에 따라 관계형 DB를 구조화하는 프로세스이다. 에드거 F. 코드가 *관계 모델의 일부로 처음 제안했다. 정규화는 데이터베이스의 열(속성)과 테이블(관계)을 구성하여 *DB 무결성 제약 조건에 따라 종속성이 적절히 적용되도록 하는 것을 수반한다. 정규화는 합성(새로운 DB 설계 생성) 또는 분해(기존 DB 설계 개선) 과정을 통해 몇 가지 형식적 규칙을 적용하여 수행된다.
  </p>
  <p><strong>정리: 데이터베이스 정규화는 데이터 중복을 최소화하고 일관성을 유지하기 위해 테이블을 구조적으로 분해하는 과정이다.</strong></p>

  <ul>
    <li><strong>관계 모델(Relational Model):</strong> 데이터를 행(튜플)과 열(속성)로 구성된 테이블 형태로 표현하고, 테이블 간 관계를 키(KEY)로 정의하는 데이터 모델.</li>
    <li><strong>DB 무결성 제약 조건(Integrity Constraints):</strong> 데이터의 정확성과 일관성을 보장하기 위해 설정하는 규칙으로, 대표적으로 개체 무결성(기본 키는 NULL·중복 불가), 참조 무결성(외래 키는 참조하는 값만 허용), 도메인 무결성(속성 값의 형식·범위 제한) 등이 있다.</li>
  </ul>

</div>
</details>


<details>
<summary><span class="accordion-title">Failure Modes </span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  데이터베이스 장애 모드(Failure Mode)는 DB 시스템이 오작동하거나 제대로 작동하지 않는 다양한 방식을 나타낸다. 여기에는 하드웨어 장애(디스크 충돌이나 네트워크 중단 등), 소프트웨어 버그, 데이터 손상, 과부하로 인한 성능 저하, 분산 시스템의 불일치 등이 포함된다. 일반적인 장애 모드에는 데이터 손실, 시스템 가용성 저하, 분산 DB의 복제 지연, *교착 상태가 포함된다. 이러한 문제를 완화하기 위해 DB는 중복성, 정기적인 백업, 트랜잭션 로깅, 장애 조치(failover) 메커니즘과 같은 전략을 사용한다. 잠재적인 장애 모드를 이해하는 것은 고가용성과 데이터 무결성을 갖춘 견고한 데이터베이스 시스템을 설계하는 데 매우 중요하다. 이는 내결함성 조치, 복구 절차, 모니터링 시스템 구현을 통해 데이터베이스 안정성을 보장하고 중요 애플리케이션의 *다운타임을 최소화하는 데 도움이 된다.
  </p>
  <p><strong>정리: Failure Modes는 시스템이 고장이나 오류로 인해 작동이 중단되거나 비정상적으로 동작하는 다양한 유형을 의미한다.</strong></p>

  <ul>
    <li><strong>교착 상태(Deadlock):</strong> 여러 프로세스나 트랜잭션이 서로의 자원을 기다리며 무한 대기 상태에 빠지는 현상.</li>
    <li><strong>다운타임(Downtime):</strong> 시스템이나 서비스가 장애·점검 등으로 인해 정상적으로 작동하지 않는 기간.</li>
  </ul>

</div>
</details>


<details>
<summary><span class="accordion-title">Profiling Performance </span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  성능 프로파일링(Profiling Performance)은 시스템 또는 애플리케이션의 동작을 분석하여 *병목 현상, 비효율성, 최적화 영역을 파악하는 과정이다. 이 프로세스는 일반적으로 CPU 및 메모리 사용량, *I/O 작업, 함수 또는 메서드 실행 시간 등 리소스 사용에 대한 자세한 정보를 수집하는 과정을 포함한다. 프로파일링 도구는 코드의 각 부분이 전체 성능에 어떻게 기여하는지에 대한 통찰력을 제공하여 느리거나 리소스를 많이 사용하는 작업을 파악할 수 있다. 개발자는 이러한 성능 특성을 이해함으로써 목표에 맞는 개선을 수행하고, 코드 경로를 최적화하며, 시스템 응답성과 확장성을 향상시킬 수 있다. 프로파일링은 성능 문제를 진단하고 애플리케이션이 원하는 성능 기준을 충족하는지 확인하는 데 필수적이다.
  </p>
  <p><strong>정리: Profiling Performance는 프로그램 실행 중 성능 데이터를 수집·분석해 병목 구간과 최적화 지점을 찾는 과정이다.</strong></p>

  <ul>
    <li><strong>병목 현상(Bottleneck):</strong> 시스템 전체 성능이 특정 자원(예: CPU, 메모리, 네트워크) 한계로 인해 제한되는 현상.</li>
    <li><strong>I/O 작업(Input/Output):</strong> 저장장치, 네트워크, 주변 장치 등 외부 자원과 데이터를 주고받는 작업으로, CPU 연산보다 속도가 느려 성능에 영향을 줄 수 있음.</li>
  </ul>

</div>
</details>


<details>
<summary><span class="accordion-title">Migrations </span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  데이터베이스 마이그레이션은 버전 관리 방식으로 DB *스키마의 점진적인 변경 사항을 관리하고 적용하는 방식으로, 개발자는 기존 데이터에 영향을 주지 않고 DB 구조(예: 테이블 추가, 열 변경)를 수정할 수 있다. 데이터베이스 마이그레이션은 이전 버전의 스키마와의 호환성을 유지하면서 DB가 개발, 테스트, 운영 등 다양한 환경에서 일관되고 반복 가능한 방식으로 애플리케이션 코드와 함께 발전하도록 보장한다. 마이그레이션은 일반적으로 SQL 또는 DB 독립적인 언어로 작성되며, *Liquibase, *Flyway와 같은 마이그레이션 도구 또는 *Django 또는 *Rails 마이그레이션과 같은 내장 ORM 기능을 사용하여 실행된다.
  </p>
  <p><strong>정리: 마이그레이션(Migrations)은 데이터베이스 스키마 변경 사항을 버전 관리하며 자동으로 적용·롤백할 수 있게 하는 기능이다.</strong></p>

  <ul>
    <li><strong>스키마(Schema):</strong> 데이터베이스의 구조와 제약 조건을 정의한 설계도(테이블, 컬럼, 관계, 인덱스 등 포함).</li>
    <li><strong>Liquibase:</strong> XML·YAML·JSON·SQL 형식으로 스키마 변경을 기록·관리하는 오픈소스 DB 마이그레이션 도구.</li>
    <li><strong>Flyway:</strong> SQL 스크립트 기반의 경량 DB 마이그레이션 도구로, Java 프로젝트(Spring 등)에서 자주 사용됨.</li>
    <li><strong>Django 마이그레이션:</strong> Django ORM 모델 변경 사항을 makemigrations/migrate 명령어로 DB에 반영하는 기능.</li>
    <li><strong>Rails 마이그레이션:</strong> Ruby on Rails에서 ActiveRecord 모델 변경을 코드로 정의하고 rails db:migrate로 적용하는 기능.</li>
  </ul>

</div>
</details>
