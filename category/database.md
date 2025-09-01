---
layout: default
title: "데이터베이스 완전 정리"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>데이터베이스 완전 정리 - 면접부터 개념까지</h2>
</section>


<!-- 면접 예상 질문 및 답변 -->
<details open>
  <summary><span class="accordion-title">면접 예상 질문 및 답변</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

<details>
  <summary style="font-size:1rem;"><b>Q: 데이터베이스와 DBMS의 차이점을 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 데이터베이스는 조직화된 데이터의 집합체로, 특정 목적을 위해 구조화되어 저장된 데이터들입니다. DBMS(Database Management System)는 데이터베이스를 생성, 관리, 조작할 수 있게 해주는 소프트웨어 시스템입니다. 즉, 데이터베이스는 데이터 자체이고, DBMS는 그 데이터를 관리하는 도구입니다. Oracle, MySQL, PostgreSQL 등이 DBMS의 예시이며, 데이터 독립성, 동시성 제어, 보안, 무결성 보장 등의 기능을 제공합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q: 관계형 데이터베이스의 특징을 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 관계형 데이터베이스는 데이터를 테이블(릴레이션) 형태로 저장하고 관리하는 데이터베이스입니다. 각 테이블은 행(튜플)과 열(속성)으로 구성되며, 기본키로 각 행을 고유하게 식별합니다. 테이블 간의 관계는 외래키를 통해 설정됩니다. ACID 속성을 만족하고, SQL이라는 표준 질의어를 사용하며, 스키마를 통해 데이터 구조를 미리 정의합니다. 데이터 무결성과 일관성을 보장하지만, 스키마 변경이 어렵고 수평 확장에 제약이 있습니다.  ### SQL 관련</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q: JOIN의 종류와 차이점을 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> JOIN은 두 개 이상의 테이블을 연결하여 데이터를 조회하는 방법입니다. INNER JOIN은 두 테이블에 모두 존재하는 데이터만 반환하고, LEFT/RIGHT OUTER JOIN은 한쪽 테이블의 모든 데이터와 다른 테이블의 매칭되는 데이터를 반환합니다. FULL OUTER JOIN은 양쪽 테이블의 모든 데이터를 반환하며, CROSS JOIN은 카티시안 곱으로 모든 조합을 생성합니다. SELF JOIN은 같은 테이블을 자기 자신과 조인하는 것입니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q: 인덱스의 동작 원리와 종류를 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 인덱스는 데이터의 물리적 위치를 가리키는 포인터를 정렬된 구조로 관리하여 검색 성능을 향상시키는 도구입니다. B-Tree 구조를 주로 사용하며, 검색 시간을 O(log n)으로 단축시킵니다. 클러스터드 인덱스는 데이터와 인덱스가 함께 정렬되어 저장되고, 논클러스터드 인덱스는 별도의 구조로 관리됩니다. 복합 인덱스는 여러 컬럼을 조합하여 만들며, 유니크 인덱스는 중복값을 허용하지 않습니다. 검색 성능은 향상되지만 삽입/수정/삭제 시 오버헤드가 발생합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q: 트랜잭션과 ACID 속성에 대해 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 트랜잭션은 데이터베이스의 상태를 변화시키는 논리적 작업 단위로, 모두 성공하거나 모두 실패하는 특성을 가집니다. ACID는 트랜잭션의 4가지 속성입니다. 원자성(Atomicity)은 트랜잭션이 전부 실행되거나 전혀 실행되지 않아야 함을 의미합니다. 일관성(Consistency)은 트랜잭션 실행 후에도 데이터베이스가 일관된 상태를 유지해야 함을 의미합니다. 격리성(Isolation)은 동시 실행되는 트랜잭션들이 서로 영향을 주지 않아야 함을 의미합니다. 지속성(Durability)은 성공한 트랜잭션의 결과가 영구적으로 저장되어야 함을 의미합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q: 정규화에 대해 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 정규화는 관계형 데이터베이스에서 중복을 최소화하고 데이터 무결성을 보장하기 위해 테이블을 분해하는 과정입니다. 1NF는 원자값만 저장하고 반복 그룹을 제거합니다. 2NF는 1NF + 부분 함수 종속성을 제거합니다. 3NF는 2NF + 이행적 함수 종속성을 제거합니다. BCNF는 3NF + 결정자가 후보키가 되도록 합니다. 정규화를 통해 데이터 중복과 갱신 이상을 방지할 수 있지만, 조인 연산이 증가하여 성능이 저하될 수 있습니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q: 격리 수준(Isolation Level)에 대해 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 격리 수준은 동시에 실행되는 트랜잭션들 간의 간섭 정도를 조절하는 설정입니다. READ UNCOMMITTED는 커밋되지 않은 데이터도 읽을 수 있어 Dirty Read가 발생할 수 있습니다. READ COMMITTED는 커밋된 데이터만 읽어 Dirty Read는 방지하지만 Non-repeatable Read가 발생할 수 있습니다. REPEATABLE READ는 같은 트랜잭션 내에서 동일한 읽기 결과를 보장하지만 Phantom Read가 발생할 수 있습니다. SERIALIZABLE은 모든 이상 현상을 방지하지만 동시성이 가장 낮습니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q: 데이터베이스 락(Lock)에 대해 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 락은 동시성 제어를 위해 트랜잭션이 데이터에 접근할 때 다른 트랜잭션의 접근을 제한하는 메커니즘입니다. 공유락(S-Lock)은 읽기만 가능하며 여러 트랜잭션이 동시에 가질 수 있고, 배타락(X-Lock)은 읽기/쓰기 모두 가능하며 하나의 트랜잭션만 가질 수 있습니다. 락 단위는 데이터베이스, 테이블, 페이지, 레코드 수준이 있으며, 단위가 작을수록 동시성이 높아지지만 오버헤드가 증가합니다. 데드락 방지를 위해 2단계 락킹 프로토콜을 사용합니다.  ### 성능 최적화</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q: 쿼리 최적화 방법에 대해 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 쿼리 최적화는 SQL 쿼리의 실행 계획을 분석하여 가장 효율적인 방법을 선택하는 과정입니다. 적절한 인덱스 사용, WHERE 절에서 선택성이 높은 조건을 먼저 사용, 불필요한 컬럼 조회 방지, EXISTS 대신 JOIN 사용, 서브쿼리보다 JOIN 선호 등의 방법이 있습니다. 실행 계획을 확인하여 테이블 스캔을 인덱스 스캔으로 변경하고, 조인 순서를 최적화하며, 통계 정보를 최신으로 유지하는 것이 중요합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q: 파티셔닝과 샤딩의 차이점을 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 파티셔닝은 하나의 데이터베이스 내에서 테이블을 여러 부분으로 나누는 것입니다. 수평 파티셔닝(특정 조건으로 행 분할)과 수직 파티셔닝(컬럼 기준 분할)이 있으며, 쿼리 성능 향상과 관리 편의성을 제공합니다. 샤딩은 데이터를 여러 데이터베이스 서버에 분산 저장하는 것으로, 각 샤드는 독립적인 데이터베이스입니다. 샤딩은 수평 확장을 가능하게 하지만 복잡성이 증가하고, 크로스 샤드 쿼리가 어려워집니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q: NoSQL 데이터베이스의 종류와 특징을 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> NoSQL은 관계형 모델을 사용하지 않는 데이터베이스의 총칭입니다. 문서형(MongoDB)은 JSON 형태로 데이터를 저장하여 스키마가 유연하고 중첩 구조를 지원합니다. 키-값형(Redis, DynamoDB)은 간단한 구조로 빠른 조회가 가능하고 캐시나 세션 저장에 적합합니다. 컬럼형(Cassandra, HBase)은 컬럼 단위로 저장하여 분석 쿼리에 유리하고 압축률이 높습니다. 그래프형(Neo4j)은 노드와 관계로 데이터를 표현하여 복잡한 관계 분석에 적합합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q: CAP 정리에 대해 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> CAP 정리는 분산 시스템에서 일관성(Consistency), 가용성(Availability), 분할 허용성(Partition Tolerance) 중 최대 2가지만 보장할 수 있다는 이론입니다. 일관성은 모든 노드가 같은 시간에 같은 데이터를 보는 것이고, 가용성은 시스템이 항상 동작하는 것이며, 분할 허용성은 네트워크 분할이 발생해도 시스템이 동작하는 것입니다. 관계형 DB는 주로 CA를, NoSQL DB는 AP 또는 CP를 선택합니다. 실제로는 BASE(Eventually Consistent) 모델로 일관성을 완화하여 가용성과 분할 허용성을 확보하는 경우가 많습니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q: 데이터베이스 복제(Replication)와 클러스터링의 차이점을 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 복제는 동일한 데이터를 여러 데이터베이스 서버에 복사하여 저장하는 것입니다. 마스터-슬레이브 구조에서 마스터는 쓰기를 담당하고 슬레이브는 읽기를 담당하여 읽기 성능을 향상시킵니다. 클러스터링은 여러 데이터베이스 서버가 하나의 시스템처럼 동작하도록 구성하는 것으로, Active-Active 또는 Active-Standby 방식이 있습니다. 복제는 주로 성능 향상과 읽기 확장에 중점을 두고, 클러스터링은 고가용성과 무중단 서비스에 중점을 둡니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q: MVCC(Multi-Version Concurrency Control)에 대해 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> MVCC는 데이터의 여러 버전을 유지하여 동시성을 제어하는 기법입니다. 읽기 연산은 락을 사용하지 않고 특정 시점의 스냅샷을 읽으며, 쓰기 연산만 락을 사용합니다. 각 트랜잭션은 시작 시점의 데이터베이스 상태를 보게 되어 일관된 읽기가 보장됩니다. PostgreSQL, Oracle 등에서 사용되며, 읽기 성능이 향상되고 데드락 가능성이 줄어들지만, 추가적인 저장 공간이 필요하고 가비지 컬렉션이 필요합니다.  ### 성능 및 최적화</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q: 실행 계획(Execution Plan)을 분석하는 방법을 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 실행 계획은 DBMS가 SQL 쿼리를 어떻게 실행할지 결정한 절차입니다. EXPLAIN 명령어로 확인할 수 있으며, 테이블 스캔 방식(Full Table Scan vs Index Scan), 조인 방식(Nested Loop, Hash Join, Merge Join), 예상 비용과 실제 처리 행 수를 분석해야 합니다. 높은 비용을 가진 연산, 많은 행을 처리하는 연산, 테이블 풀 스캔이 발생하는 부분을 찾아 인덱스 추가나 쿼리 수정을 통해 최적화합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q: 데이터베이스 커넥션 풀에 대해 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 커넥션 풀은 데이터베이스 연결을 미리 생성하여 풀에 저장해두고 재사용하는 기법입니다. 애플리케이션에서 DB 연결이 필요할 때마다 새로 생성하지 않고 풀에서 가져와 사용한 후 반환합니다. 연결 생성/해제 오버헤드를 줄여 성능을 향상시키고, 동시 연결 수를 제한하여 DB 서버 부하를 관리할 수 있습니다. 적절한 풀 크기 설정이 중요하며, 너무 작으면 대기시간이 증가하고 너무 크면 메모리 낭비가 발생합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q: 데이터베이스 정규화와 비정규화의 장단점을 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 정규화는 데이터 중복을 제거하고 무결성을 보장하는 장점이 있지만, 조인 연산이 증가하여 조회 성능이 저하될 수 있습니다. 저장 공간을 절약하고 데이터 일관성을 유지하기 쉽지만, 복잡한 쿼리가 필요하고 애플리케이션 로직이 복잡해집니다. 비정규화는 조회 성능을 향상시키고 쿼리를 단순화하는 장점이 있지만, 데이터 중복으로 인한 저장 공간 증가와 데이터 불일치 위험이 있습니다. 실무에서는 OLTP는 정규화를, OLAP는 비정규화를 선호하는 경향이 있습니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q: 데이터베이스 백업과 복구 전략을 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 데이터베이스 백업은 데이터 손실에 대비한 필수 작업입니다. 풀 백업은 전체 데이터를 백업하여 복구가 간단하지만 시간과 저장 공간이 많이 필요합니다. 증분 백업은 마지막 백업 이후 변경된 데이터만 백업하여 효율적이지만 복구가 복잡합니다. 차등 백업은 마지막 풀 백업 이후 변경된 모든 데이터를 백업합니다. 복구 전략으로는 Point-in-Time Recovery, 로그 기반 복구, 레플리케이션을 활용한 실시간 복구 등이 있습니다. RTO(복구 목표 시간)와 RPO(복구 목표 시점)를 고려한 전략 수립이 중요합니다.  ### 분산 데이터베이스</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q: 분산 데이터베이스의 장단점과 CAP 이론을 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 분산 데이터베이스는 여러 위치에 분산된 데이터베이스들이 네트워크로 연결되어 하나의 논리적 시스템으로 동작하는 것입니다. 장점으로는 확장성, 가용성, 성능 향상, 지리적 분산이 있습니다. 단점으로는 복잡성 증가, 네트워크 의존성, 일관성 유지의 어려움, 보안 위험 증가가 있습니다. CAP 이론에 의하면 분산 시스템은 일관성, 가용성, 분할 허용성 중 최대 2가지만 완전히 보장할 수 있어, 비즈니스 요구사항에 따라 적절한 트레이드오프를 선택해야 합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q: 데이터베이스 모니터링과 튜닝 방법을 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p><b>A:</b> 데이터베이스 모니터링은 성능 지표 추적, 슬로우 쿼리 로그 분석, 리소스 사용률 확인, 락 대기 상황 모니터링 등을 포함합니다. 튜닝 방법으로는 인덱스 최적화(불필요한 인덱스 제거, 복합 인덱스 활용), 쿼리 최적화(조인 순서 변경, 서브쿼리를 조인으로 변경), 파라미터 튜닝(버퍼 크기, 캐시 설정), 하드웨어 최적화(CPU, 메모리, 스토리지 업그레이드)가 있습니다. 성능 테스트를 통해 튜닝 효과를 검증하고 지속적으로 모니터링해야 합니다.  ---</p>
  </div>
</details>

  </div>
</details>

<details>
  <summary><span class="accordion-title">시스템 기초 개념 정리 (전체)</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

<!-- 개념 정리 -->
<h2>데이터베이스 개념 정리</h2>

<h2>1. 데이터베이스 기초</h2>

<h3>1.1 데이터베이스 개요</h3>

<h4>데이터베이스란?</h4>
특정 조직이나 개인이 필요에 의해 논리적으로 연관된 데이터를 모아 체계적으로 구성해놓은 데이터의 집합입니다.

<h4>데이터베이스의 특징</h4>
<ul>
  <li><strong>데이터 독립성</strong>: 물리적/논리적 구조 변경이 응용 프로그램에 영향을 주지 않음</li>
</ul>
<ul>
  <li><strong>데이터 무결성</strong>: 데이터의 정확성과 일관성 보장</li>
</ul>
<ul>
  <li><strong>데이터 보안</strong>: 인가되지 않은 접근으로부터 보호</li>
</ul>
<ul>
  <li><strong>데이터 중복 최소화</strong>: 동일한 데이터의 중복 저장 방지</li>
</ul>
<ul>
  <li><strong>데이터 공유</strong>: 여러 사용자가 동시에 데이터 사용 가능</li>
</ul>

<h4>DBMS의 장점</h4>
<ul>
  <li>데이터 중복 감소</li>
</ul>
<ul>
  <li>데이터 일관성 유지</li>
</ul>
<ul>
  <li>데이터 보안 강화</li>
</ul>
<ul>
  <li>표준화 지원</li>
</ul>
<ul>
  <li>동시성 제어</li>
</ul>
<ul>
  <li>백업 및 복구 기능</li>
</ul>

<h3>1.2 데이터베이스 구조</h3>

<h4>3층 스키마 구조</h4>
<strong>외부 스키마 (External Schema)</strong>
<ul>
  <li>사용자나 응용 프로그램의 관점</li>
</ul>
<ul>
  <li>개별 사용자 레벨</li>
</ul>
<ul>
  <li>서브 스키마라고도 함</li>
</ul>

<strong>개념 스키마 (Conceptual Schema)</strong>
<ul>
  <li>전체 데이터베이스의 논리적 구조</li>
</ul>
<ul>
  <li>조직 전체의 관점</li>
</ul>
<ul>
  <li>일반적으로 스키마라고 하면 이를 의미</li>
</ul>

<strong>내부 스키마 (Internal Schema)</strong>
<ul>
  <li>물리적 저장 구조</li>
</ul>
<ul>
  <li>시스템 관리자 관점</li>
</ul>
<ul>
  <li>저장 레코드 형식, 인덱스, 데이터 압축 등</li>
</ul>

<h4>데이터 독립성</h4>
<strong>논리적 독립성</strong>
<ul>
  <li>개념 스키마가 변경되어도 외부 스키마는 영향받지 않음</li>
</ul>
<ul>
  <li>테이블 추가/삭제, 속성 추가/삭제</li>
</ul>

<strong>물리적 독립성</strong>
<ul>
  <li>내부 스키마가 변경되어도 개념 스키마는 영향받지 않음</li>
</ul>
<ul>
  <li>저장 장치 변경, 인덱스 추가/삭제</li>
</ul>

<h3>1.3 데이터 모델</h3>

<h4>계층형 데이터 모델</h4>
<ul>
  <li>트리 구조</li>
</ul>
<ul>
  <li>부모-자식 관계</li>
</ul>
<ul>
  <li>1:N 관계만 표현 가능</li>
</ul>

<h4>네트워크 데이터 모델</h4>
<ul>
  <li>그래프 구조</li>
</ul>
<ul>
  <li>복잡한 관계 표현 가능</li>
</ul>
<ul>
  <li>구현과 유지보수가 복잡</li>
</ul>

<h4>관계형 데이터 모델</h4>
<ul>
  <li>테이블(릴레이션) 구조</li>
</ul>
<ul>
  <li>수학적 집합 이론 기반</li>
</ul>
<ul>
  <li>현재 가장 널리 사용</li>
</ul>

<h4>객체지향 데이터 모델</h4>
<ul>
  <li>객체와 클래스 개념 적용</li>
</ul>
<ul>
  <li>복잡한 데이터 타입 지원</li>
</ul>
<ul>
  <li>상속과 캡슐화 지원</li>
</ul>

<h2>2. 관계형 데이터베이스</h2>

<h3>2.1 관계형 모델 기본 개념</h3>

<h4>릴레이션 (Relation)</h4>
행과 열로 구성된 테이블을 의미합니다.

<h4>튜플 (Tuple)</h4>
테이블의 행(row)으로, 하나의 레코드를 의미합니다.

<h4>속성 (Attribute)</h4>
테이블의 열(column)으로, 데이터의 특성을 나타냅니다.

<h4>도메인 (Domain)</h4>
속성이 가질 수 있는 값들의 집합입니다.

<h4>차수 (Degree)</h4>
릴레이션이 가진 속성의 개수입니다.

<h4>카디날리티 (Cardinality)</h4>
릴레이션이 가진 튜플의 개수입니다.

<h3>2.2 키 (Key)</h3>

<h4>슈퍼키 (Super Key)</h4>
튜플을 유일하게 식별할 수 있는 속성 또는 속성의 집합입니다.

<h4>후보키 (Candidate Key)</h4>
슈퍼키 중에서 최소성을 만족하는 키입니다.

<h4>기본키 (Primary Key)</h4>
후보키 중에서 선택된 주된 키로, 테이블에서 각 행을 유일하게 식별합니다.

<strong>기본키 조건</strong>
<ul>
  <li>유일성: 중복값 불허</li>
</ul>
<ul>
  <li>최소성: 꼭 필요한 속성으로만 구성</li>
</ul>
<ul>
  <li>불변성: 값이 자주 변경되지 않음</li>
</ul>
<ul>
  <li>존재성: NULL 값 불허</li>
</ul>

<h4>외래키 (Foreign Key)</h4>
다른 릴레이션의 기본키를 참조하는 속성입니다.

<strong>참조 무결성</strong>
<ul>
  <li>외래키 값은 참조 테이블의 기본키 값이거나 NULL이어야 함</li>
</ul>
<ul>
  <li>CASCADE, RESTRICT, SET NULL 등의 옵션 제공</li>
</ul>

<h4>대체키 (Alternate Key)</h4>
후보키 중에서 기본키로 선택되지 않은 키입니다.

<h3>2.3 무결성 제약조건</h3>

<h4>개체 무결성 (Entity Integrity)</h4>
기본키는 NULL 값을 가질 수 없고, 중복될 수 없습니다.

<h4>참조 무결성 (Referential Integrity)</h4>
외래키 값은 참조 테이블의 기본키 값이거나 NULL이어야 합니다.

<h4>도메인 무결성 (Domain Integrity)</h4>
속성의 값은 정의된 도메인에 속해야 합니다.

<h4>사용자 정의 무결성</h4>
사용자가 정의한 비즈니스 규칙을 만족해야 합니다.

<h2>3. 정규화 (Normalization)</h2>

<h3>3.1 정규화 개요</h3>
데이터의 중복을 최소화하고 무결성을 보장하기 위해 테이블을 분해하는 과정입니다.

<h4>이상 현상 (Anomaly)</h4>
<strong>삽입 이상</strong>: 불필요한 데이터를 함께 삽입해야 하는 문제
<strong>갱신 이상</strong>: 중복된 데이터 중 일부만 수정되어 불일치가 발생하는 문제
<strong>삭제 이상</strong>: 필요한 데이터까지 함께 삭제되는 문제

<h3>3.2 함수적 종속성 (Functional Dependency)</h3>
속성 A의 값이 결정되면 속성 B의 값이 유일하게 결정되는 관계입니다.

<h4>종류</h4>
<ul>
  <li><strong>완전 함수적 종속</strong>: 기본키 전체에 종속</li>
</ul>
<ul>
  <li><strong>부분 함수적 종속</strong>: 기본키의 일부에만 종속</li>
</ul>
<ul>
  <li><strong>이행적 함수적 종속</strong>: A → B, B → C이면 A → C</li>
</ul>

<h3>3.3 정규화 단계</h3>

<h4>제1정규형 (1NF)</h4>
<ul>
  <li>모든 속성은 원자값(atomic value)을 가져야 함</li>
</ul>
<ul>
  <li>반복 그룹 제거</li>
</ul>
<ul>
  <li>각 행은 고유해야 함</li>
</ul>

<h4>제2정규형 (2NF)</h4>
<ul>
  <li>1NF를 만족</li>
</ul>
<ul>
  <li>부분 함수적 종속성 제거</li>
</ul>
<ul>
  <li>복합키의 일부에만 종속되는 속성 분리</li>
</ul>

<h4>제3정규형 (3NF)</h4>
<ul>
  <li>2NF를 만족</li>
</ul>
<ul>
  <li>이행적 함수적 종속성 제거</li>
</ul>
<ul>
  <li>기본키가 아닌 속성 간의 종속성 제거</li>
</ul>

<h4>BCNF (Boyce-Codd Normal Form)</h4>
<ul>
  <li>3NF를 만족</li>
</ul>
<ul>
  <li>모든 결정자가 후보키여야 함</li>
</ul>
<ul>
  <li>3NF보다 엄격한 조건</li>
</ul>

<h4>제4정규형 (4NF)</h4>
<ul>
  <li>BCNF를 만족</li>
</ul>
<ul>
  <li>다치 종속성(Multi-valued Dependency) 제거</li>
</ul>

<h4>제5정규형 (5NF)</h4>
<ul>
  <li>4NF를 만족</li>
</ul>
<ul>
  <li>조인 종속성(Join Dependency) 제거</li>
</ul>

<h3>3.4 비정규화 (Denormalization)</h3>
성능 향상을 위해 의도적으로 정규화 규칙을 위반하여 테이블을 통합하거나 중복 데이터를 허용하는 것입니다.

<strong>비정규화 기법</strong>
<ul>
  <li>테이블 통합</li>
</ul>
<ul>
  <li>테이블 분할</li>
</ul>
<ul>
  <li>중복 컬럼 추가</li>
</ul>
<ul>
  <li>파생 컬럼 추가</li>
</ul>
<ul>
  <li>이력 테이블 분리</li>
</ul>

<h2>4. SQL (Structured Query Language)</h2>

<h3>4.1 SQL 개요</h3>
관계형 데이터베이스에서 데이터를 관리하기 위한 표준 언어입니다.

<h4>SQL 분류</h4>
<strong>DDL (Data Definition Language)</strong>
<ul>
  <li>데이터베이스 구조 정의</li>
</ul>
<ul>
  <li>CREATE, ALTER, DROP, TRUNCATE</li>
</ul>

<strong>DML (Data Manipulation Language)</strong>
<ul>
  <li>데이터 조작</li>
</ul>
<ul>
  <li>SELECT, INSERT, UPDATE, DELETE</li>
</ul>

<strong>DCL (Data Control Language)</strong>
<ul>
  <li>접근 권한 제어</li>
</ul>
<ul>
  <li>GRANT, REVOKE</li>
</ul>

<strong>TCL (Transaction Control Language)</strong>
<ul>
  <li>트랜잭션 제어</li>
</ul>
<ul>
  <li>COMMIT, ROLLBACK, SAVEPOINT</li>
</ul>

<h3>4.2 기본 쿼리</h3>

<h4>SELECT 문</h4>
```sql
SELECT 컬럼명
FROM 테이블명
WHERE 조건
GROUP BY 그룹컬럼
HAVING 그룹조건
ORDER BY 정렬컬럼
```

<h4>조인 (JOIN)</h4>
<strong>INNER JOIN</strong>
<ul>
  <li>두 테이블에 모두 존재하는 데이터만 반환</li>
</ul>

<strong>LEFT OUTER JOIN</strong>
<ul>
  <li>왼쪽 테이블의 모든 데이터와 오른쪽 테이블의 매칭 데이터</li>
</ul>

<strong>RIGHT OUTER JOIN</strong>
<ul>
  <li>오른쪽 테이블의 모든 데이터와 왼쪽 테이블의 매칭 데이터</li>
</ul>

<strong>FULL OUTER JOIN</strong>
<ul>
  <li>양쪽 테이블의 모든 데이터</li>
</ul>

<strong>CROSS JOIN</strong>
<ul>
  <li>카티시안 곱, 모든 조합</li>
</ul>

<h4>서브쿼리</h4>
다른 쿼리 내부에 포함된 쿼리입니다.

<strong>종류</strong>
<ul>
  <li><strong>스칼라 서브쿼리</strong>: 단일 값 반환</li>
</ul>
<ul>
  <li><strong>인라인 뷰</strong>: FROM 절에 사용</li>
</ul>
<ul>
  <li><strong>중첩 서브쿼리</strong>: WHERE 절에 사용</li>
</ul>

<strong>연관성</strong>
<ul>
  <li><strong>연관 서브쿼리</strong>: 외부 쿼리와 연관된 서브쿼리</li>
</ul>
<ul>
  <li><strong>비연관 서브쿼리</strong>: 독립적으로 실행 가능한 서브쿼리</li>
</ul>

<h3>4.3 고급 SQL</h3>

<h4>윈도우 함수</h4>
```sql
함수명() OVER (PARTITION BY 컬럼 ORDER BY 컬럼)
```

<strong>종류</strong>
<ul>
  <li><strong>ROW_NUMBER()</strong>: 행 번호</li>
</ul>
<ul>
  <li><strong>RANK()</strong>: 순위 (동일값 존재 시 다음 순위 건너뜀)</li>
</ul>
<ul>
  <li><strong>DENSE_RANK()</strong>: 순위 (동일값 존재해도 다음 순위 연속)</li>
</ul>
<ul>
  <li><strong>LAG/LEAD</strong>: 이전/다음 행 값 참조</li>
</ul>

<h4>집계 함수</h4>
<ul>
  <li><strong>COUNT</strong>: 행 개수</li>
</ul>
<ul>
  <li><strong>SUM</strong>: 합계</li>
</ul>
<ul>
  <li><strong>AVG</strong>: 평균</li>
</ul>
<ul>
  <li><strong>MAX/MIN</strong>: 최댓값/최솟값</li>
</ul>
<ul>
  <li><strong>GROUP_CONCAT</strong>: 문자열 연결</li>
</ul>

<h4>CTE (Common Table Expression)</h4>
WITH 절을 사용하여 임시 결과 집합을 정의하는 기능입니다.

```sql
WITH temp_table AS (
    SELECT ...
)
SELECT * FROM temp_table;
```

<h2>5. 인덱스 (Index)</h2>

<h3>5.1 인덱스 개요</h3>
데이터의 물리적 위치를 빠르게 찾기 위한 데이터 구조입니다.

<h4>인덱스의 목적</h4>
<ul>
  <li>검색 성능 향상</li>
</ul>
<ul>
  <li>정렬 성능 향상</li>
</ul>
<ul>
  <li>조인 성능 향상</li>
</ul>
<ul>
  <li>유니크 제약 조건 지원</li>
</ul>

<h3>5.2 인덱스 구조</h3>

<h4>B-Tree 인덱스</h4>
가장 일반적인 인덱스 구조로, 균형 잡힌 트리 형태입니다.

<strong>특징</strong>
<ul>
  <li>모든 리프 노드가 같은 레벨</li>
</ul>
<ul>
  <li>범위 검색에 효율적</li>
</ul>
<ul>
  <li>정렬된 순서로 데이터 접근 가능</li>
</ul>

<h4>B+Tree 인덱스</h4>
B-Tree의 변형으로, 리프 노드에만 데이터를 저장합니다.

<strong>특징</strong>
<ul>
  <li>리프 노드 간 연결로 순차 접근 효율적</li>
</ul>
<ul>
  <li>내부 노드는 인덱스 역할만 수행</li>
</ul>
<ul>
  <li>더 많은 키를 내부 노드에 저장 가능</li>
</ul>

<h4>해시 인덱스</h4>
해시 테이블을 이용한 인덱스 구조입니다.

<strong>특징</strong>
<ul>
  <li>등치 검색에 매우 빠름 (O(1))</li>
</ul>
<ul>
  <li>범위 검색 불가능</li>
</ul>
<ul>
  <li>정렬 불가능</li>
</ul>

<h3>5.3 인덱스 종류</h3>

<h4>클러스터드 인덱스 (Clustered Index)</h4>
<ul>
  <li>데이터와 인덱스가 물리적으로 같은 순서로 저장</li>
</ul>
<ul>
  <li>테이블당 하나만 생성 가능</li>
</ul>
<ul>
  <li>기본키에 자동 생성</li>
</ul>
<ul>
  <li>범위 검색에 유리</li>
</ul>

<h4>논클러스터드 인덱스 (Non-Clustered Index)</h4>
<ul>
  <li>인덱스와 데이터가 별도로 저장</li>
</ul>
<ul>
  <li>여러 개 생성 가능</li>
</ul>
<ul>
  <li>추가적인 조회 과정 필요</li>
</ul>

<h4>복합 인덱스 (Composite Index)</h4>
<ul>
  <li>두 개 이상의 컬럼으로 구성</li>
</ul>
<ul>
  <li>컬럼 순서가 중요</li>
</ul>
<ul>
  <li>첫 번째 컬럼부터 순차적으로 사용해야 효과적</li>
</ul>

<h4>유니크 인덱스 (Unique Index)</h4>
<ul>
  <li>중복값을 허용하지 않는 인덱스</li>
</ul>
<ul>
  <li>자동으로 유니크 제약 조건 생성</li>
</ul>

<h3>5.4 인덱스 최적화</h3>

<h4>인덱스 생성 기준</h4>
<ul>
  <li>WHERE 절에 자주 사용되는 컬럼</li>
</ul>
<ul>
  <li>조인 조건에 사용되는 컬럼</li>
</ul>
<ul>
  <li>ORDER BY에 사용되는 컬럼</li>
</ul>
<ul>
  <li>선택도(Selectivity)가 높은 컬럼</li>
</ul>

<h4>인덱스 사용 시 주의사항</h4>
<ul>
  <li>함수나 연산 사용 시 인덱스 사용 불가</li>
</ul>
<ul>
  <li>LIKE의 앞부분 와일드카드 사용 시 인덱스 사용 불가</li>
</ul>
<ul>
  <li>OR 조건 사용 시 인덱스 효율성 저하</li>
</ul>
<ul>
  <li>타입이 다른 컬럼 비교 시 인덱스 사용 불가</li>
</ul>

<h2>6. 트랜잭션 (Transaction)</h2>

<h3>6.1 트랜잭션 개요</h3>
데이터베이스의 상태를 변화시키는 하나의 논리적 기능을 수행하기 위한 작업의 단위입니다.

<h4>트랜잭션의 특성 (ACID)</h4>

<strong>원자성 (Atomicity)</strong>
<ul>
  <li>트랜잭션은 분해가 불가능한 최소 단위</li>
</ul>
<ul>
  <li>전부 실행되거나 전혀 실행되지 않아야 함</li>
</ul>
<ul>
  <li>Commit 또는 Rollback</li>
</ul>

<strong>일관성 (Consistency)</strong>
<ul>
  <li>트랜잭션 실행 전후에 데이터베이스가 일관된 상태 유지</li>
</ul>
<ul>
  <li>무결성 제약조건 만족</li>
</ul>

<strong>격리성 (Isolation)</strong>
<ul>
  <li>동시에 실행되는 트랜잭션들이 서로 간섭하지 않아야 함</li>
</ul>
<ul>
  <li>각 트랜잭션은 독립적으로 실행되는 것처럼 보여야 함</li>
</ul>

<strong>지속성 (Durability)</strong>
<ul>
  <li>성공적으로 완료된 트랜잭션의 결과는 영구적으로 반영</li>
</ul>
<ul>
  <li>시스템 장애가 발생해도 결과 유지</li>
</ul>

<h3>6.2 트랜잭션 상태</h3>

<h4>활동 (Active)</h4>
트랜잭션이 실행 중인 상태입니다.

<h4>부분 완료 (Partially Committed)</h4>
트랜잭션의 마지막 연산까지 실행했지만 Commit 되지 않은 상태입니다.

<h4>완료 (Committed)</h4>
트랜잭션이 성공적으로 종료된 상태입니다.

<h4>실패 (Failed)</h4>
트랜잭션 실행에 오류가 발생하여 중단된 상태입니다.

<h4>철회 (Aborted)</h4>
트랜잭션이 비정상적으로 종료되어 Rollback 연산을 수행한 상태입니다.

<h3>6.3 동시성 제어</h3>

<h4>동시성 제어의 필요성</h4>
여러 트랜잭션이 동시에 실행될 때 데이터 일관성과 무결성을 보장하기 위해서입니다.

<h4>동시성 제어 문제</h4>
<strong>갱신 손실 (Lost Update)</strong>
<ul>
  <li>두 트랜잭션이 같은 데이터를 동시에 갱신할 때 하나의 갱신이 손실</li>
</ul>

<strong>비일관성 분석 (Inconsistent Analysis)</strong>
<ul>
  <li>트랜잭션이 데이터를 갱신하는 동안 다른 트랜잭션이 갱신 전후의 데이터를 읽음</li>
</ul>

<strong>모순성 (Inconsistency)</strong>
<ul>
  <li>동시에 실행된 트랜잭션들의 상호 간섭으로 모순된 결과 발생</li>
</ul>

<strong>연쇄 복귀 (Cascading Rollback)</strong>
<ul>
  <li>복귀하는 트랜잭션과 관련된 다른 트랜잭션들도 함께 복귀</li>
</ul>

<h3>6.4 격리 수준 (Isolation Level)</h3>

<h4>READ UNCOMMITTED (Level 0)</h4>
<ul>
  <li>커밋되지 않은 데이터도 읽기 가능</li>
</ul>
<ul>
  <li>Dirty Read 발생 가능</li>
</ul>
<ul>
  <li>가장 낮은 격리 수준</li>
</ul>

<h4>READ COMMITTED (Level 1)</h4>
<ul>
  <li>커밋된 데이터만 읽기 가능</li>
</ul>
<ul>
  <li>Dirty Read 방지</li>
</ul>
<ul>
  <li>Non-repeatable Read 발생 가능</li>
</ul>

<h4>REPEATABLE READ (Level 2)</h4>
<ul>
  <li>트랜잭션 내에서 동일한 읽기 결과 보장</li>
</ul>
<ul>
  <li>Non-repeatable Read 방지</li>
</ul>
<ul>
  <li>Phantom Read 발생 가능</li>
</ul>

<h4>SERIALIZABLE (Level 3)</h4>
<ul>
  <li>가장 높은 격리 수준</li>
</ul>
<ul>
  <li>모든 이상 현상 방지</li>
</ul>
<ul>
  <li>동시성 가장 낮음</li>
</ul>

<h3>6.5 락킹 (Locking)</h3>

<h4>락의 종류</h4>
<strong>공유락 (Shared Lock, S-Lock)</strong>
<ul>
  <li>읽기만 가능</li>
</ul>
<ul>
  <li>여러 트랜잭션이 동시에 가질 수 있음</li>
</ul>

<strong>배타락 (Exclusive Lock, X-Lock)</strong>
<ul>
  <li>읽기/쓰기 모두 가능</li>
</ul>
<ul>
  <li>하나의 트랜잭션만 가질 수 있음</li>
</ul>

<h4>락 단위 (Lock Granularity)</h4>
<ul>
  <li><strong>데이터베이스 수준</strong>: 전체 데이터베이스</li>
</ul>
<ul>
  <li><strong>테이블 수준</strong>: 테이블 전체</li>
</ul>
<ul>
  <li><strong>페이지 수준</strong>: 페이지 단위</li>
</ul>
<ul>
  <li><strong>행 수준</strong>: 개별 행</li>
</ul>

<h4>2단계 락킹 프로토콜 (2PL)</h4>
<strong>확장 단계 (Growing Phase)</strong>
<ul>
  <li>락을 획득만 하고 해제하지 않음</li>
</ul>

<strong>축소 단계 (Shrinking Phase)</strong>
<ul>
  <li>락을 해제만 하고 새로 획득하지 않음</li>
</ul>

<h2>7. 데이터베이스 설계</h2>

<h3>7.1 개념적 설계</h3>
<strong>E-R 모델 (Entity-Relationship Model)</strong>
<ul>
  <li>개체(Entity), 속성(Attribute), 관계(Relationship)로 구성</li>
</ul>
<ul>
  <li>개념적 데이터 모델링에 사용</li>
</ul>

<strong>개체 (Entity)</strong>
<ul>
  <li>독립적으로 존재하는 객체</li>
</ul>
<ul>
  <li>강한 개체와 약한 개체</li>
</ul>

<strong>속성 (Attribute)</strong>
<ul>
  <li>개체의 특성</li>
</ul>
<ul>
  <li>단순/복합, 단일값/다중값, 저장/유도</li>
</ul>

<strong>관계 (Relationship)</strong>
<ul>
  <li>개체 간의 연관성</li>
</ul>
<ul>
  <li>1:1, 1:N, N:M 관계</li>
</ul>

<h3>7.2 논리적 설계</h3>
E-R 모델을 관계형 모델로 변환하는 과정입니다.

<h4>변환 규칙</h4>
<ul>
  <li>개체 → 테이블</li>
</ul>
<ul>
  <li>속성 → 컬럼</li>
</ul>
<ul>
  <li>1:1 관계 → 외래키 또는 테이블 통합</li>
</ul>
<ul>
  <li>1:N 관계 → N 쪽에 외래키</li>
</ul>
<ul>
  <li>N:M 관계 → 연결 테이블 생성</li>
</ul>

<h3>7.3 물리적 설계</h3>
논리적 설계 결과를 실제 DBMS에 구현하는 과정입니다.

<h4>고려사항</h4>
<ul>
  <li>인덱스 설계</li>
</ul>
<ul>
  <li>뷰 설계</li>
</ul>
<ul>
  <li>파티셔닝</li>
</ul>
<ul>
  <li>클러스터링</li>
</ul>
<ul>
  <li>스토리지 할당</li>
</ul>

<h2>8. 데이터베이스 성능 최적화</h2>

<h3>8.1 쿼리 최적화</h3>

<h4>옵티마이저 (Optimizer)</h4>
SQL 쿼리를 가장 효율적으로 수행할 실행 계획을 생성하는 DBMS 구성 요소입니다.

<strong>종류</strong>
<ul>
  <li><strong>규칙 기반 옵티마이저 (RBO)</strong>: 미리 정의된 규칙 사용</li>
</ul>
<ul>
  <li><strong>비용 기반 옵티마이저 (CBO)</strong>: 통계 정보를 바탕으로 비용 계산</li>
</ul>

<h4>실행 계획 (Execution Plan)</h4>
옵티마이저가 생성한 쿼리 실행 방법입니다.

<strong>확인 방법</strong>
<ul>
  <li>EXPLAIN (MySQL)</li>
</ul>
<ul>
  <li>EXPLAIN PLAN (Oracle)</li>
</ul>
<ul>
  <li>SET SHOWPLAN_ALL ON (SQL Server)</li>
</ul>

<h4>쿼리 튜닝 기법</h4>
<ul>
  <li>인덱스 활용 극대화</li>
</ul>
<ul>
  <li>조인 순서 최적화</li>
</ul>
<ul>
  <li>서브쿼리를 조인으로 변경</li>
</ul>
<ul>
  <li>WHERE 절 조건 순서 조정</li>
</ul>
<ul>
  <li>DISTINCT, GROUP BY 최소화</li>
</ul>

<h3>8.2 인덱스 튜닝</h3>

<h4>인덱스 스캔 방식</h4>
<strong>Index Range Scan</strong>
<ul>
  <li>B-Tree 인덱스의 일반적인 스캔</li>
</ul>
<ul>
  <li>범위 조건에 사용</li>
</ul>

<strong>Index Full Scan</strong>
<ul>
  <li>인덱스 전체를 스캔</li>
</ul>
<ul>
  <li>정렬된 결과가 필요할 때</li>
</ul>

<strong>Index Unique Scan</strong>
<ul>
  <li>유니크 인덱스에서 하나의 값만 검색</li>
</ul>

<strong>Index Skip Scan</strong>
<ul>
  <li>복합 인덱스에서 선두 컬럼을 건너뛰고 검색</li>
</ul>

<h3>8.3 파티셔닝 (Partitioning)</h3>

<h4>수평 파티셔닝</h4>
테이블의 행을 여러 파티션으로 나누는 방법입니다.

<strong>종류</strong>
<ul>
  <li><strong>Range Partitioning</strong>: 값의 범위로 분할</li>
</ul>
<ul>
  <li><strong>Hash Partitioning</strong>: 해시 함수로 분할</li>
</ul>
<ul>
  <li><strong>List Partitioning</strong>: 특정 값들로 분할</li>
</ul>
<ul>
  <li><strong>Composite Partitioning</strong>: 여러 방법 조합</li>
</ul>

<h4>수직 파티셔닝</h4>
테이블의 컬럼을 여러 테이블로 나누는 방법입니다.

<strong>장점</strong>
<ul>
  <li>I/O 성능 향상</li>
</ul>
<ul>
  <li>관리 효율성</li>
</ul>
<ul>
  <li>병렬 처리 가능</li>
</ul>

<strong>단점</strong>
<ul>
  <li>조인 비용 증가</li>
</ul>
<ul>
  <li>복잡성 증가</li>
</ul>

<h2>9. 백업과 복구</h2>

<h3>9.1 백업 유형</h3>

<h4>물리적 백업</h4>
<ul>
  <li>데이터 파일을 직접 복사</li>
</ul>
<ul>
  <li>빠른 백업과 복구</li>
</ul>
<ul>
  <li>플랫폼 종속적</li>
</ul>

<h4>논리적 백업</h4>
<ul>
  <li>SQL 문으로 데이터 추출</li>
</ul>
<ul>
  <li>플랫폼 독립적</li>
</ul>
<ul>
  <li>선택적 백업 가능</li>
</ul>

<h4>백업 방식</h4>
<strong>풀 백업 (Full Backup)</strong>
<ul>
  <li>전체 데이터베이스 백업</li>
</ul>
<ul>
  <li>완전한 복구 가능</li>
</ul>
<ul>
  <li>시간과 공간 많이 소요</li>
</ul>

<strong>증분 백업 (Incremental Backup)</strong>
<ul>
  <li>마지막 백업 이후 변경된 데이터만 백업</li>
</ul>
<ul>
  <li>효율적이지만 복구 복잡</li>
</ul>

<strong>차등 백업 (Differential Backup)</strong>
<ul>
  <li>마지막 풀 백업 이후 변경된 모든 데이터 백업</li>
</ul>
<ul>
  <li>증분과 풀 백업의 중간 형태</li>
</ul>

<h3>9.2 복구 기법</h3>

<h4>즉시 갱신 기법</h4>
<ul>
  <li>트랜잭션 실행 중에 데이터베이스에 즉시 반영</li>
</ul>
<ul>
  <li>UNDO/REDO 로그 필요</li>
</ul>

<h4>지연 갱신 기법</h4>
<ul>
  <li>트랜잭션 완료 후 데이터베이스에 반영</li>
</ul>
<ul>
  <li>REDO 로그만 필요</li>
</ul>

<h4>체크포인트 (Checkpoint)</h4>
<ul>
  <li>특정 시점의 데이터베이스 상태를 저장</li>
</ul>
<ul>
  <li>복구 시 시작점 역할</li>
</ul>
<ul>
  <li>시스템 부하 분산</li>
</ul>

<h2>10. 동시성 제어</h2>

<h3>10.1 락킹 프로토콜</h3>

<h4>기본 락킹</h4>
<ul>
  <li>데이터 접근 전 락 획득</li>
</ul>
<ul>
  <li>작업 완료 후 락 해제</li>
</ul>

<h4>2단계 락킹 (2PL)</h4>
<ul>
  <li>확장 단계: 락 획득만 가능</li>
</ul>
<ul>
  <li>축소 단계: 락 해제만 가능</li>
</ul>
<ul>
  <li>직렬성 보장</li>
</ul>

<h4>엄격한 2단계 락킹</h4>
<ul>
  <li>트랜잭션 종료 시까지 배타락 유지</li>
</ul>
<ul>
  <li>연쇄 복귀 방지</li>
</ul>

<h3>10.2 타임스탬프 기법</h3>
각 트랜잭션에 고유한 타임스탬프를 부여하여 순서를 결정하는 방법입니다.

<strong>규칙</strong>
<ul>
  <li>늦게 시작한 트랜잭션이 먼저 시작한 트랜잭션의 결과를 읽으려면 대기</li>
</ul>
<ul>
  <li>먼저 시작한 트랜잭션이 늦게 시작한 트랜잭션의 결과를 수정하려면 롤백</li>
</ul>

<h3>10.3 낙관적 vs 비관적 동시성 제어</h3>

<h4>낙관적 (Optimistic)</h4>
<ul>
  <li>충돌이 드물다고 가정</li>
</ul>
<ul>
  <li>커밋 시점에 검증</li>
</ul>
<ul>
  <li>높은 동시성</li>
</ul>

<h4>비관적 (Pessimistic)</h4>
<ul>
  <li>충돌이 자주 발생한다고 가정</li>
</ul>
<ul>
  <li>미리 락 획득</li>
</ul>
<ul>
  <li>안전하지만 동시성 저하</li>
</ul>

<h2>11. 분산 데이터베이스</h2>

<h3>11.1 분산 데이터베이스 개요</h3>
지리적으로 분산된 여러 사이트에 데이터베이스를 분산 저장하고 관리하는 시스템입니다.

<h4>투명성 (Transparency)</h4>
<ul>
  <li><strong>분산 투명성</strong>: 사용자가 분산을 의식하지 않음</li>
</ul>
<ul>
  <li><strong>복제 투명성</strong>: 복제본 존재를 의식하지 않음</li>
</ul>
<ul>
  <li><strong>장애 투명성</strong>: 부분적 장애를 의식하지 않음</li>
</ul>

<h3>11.2 분산 트랜잭션</h3>

<h4>2단계 커밋 (2PC)</h4>
분산 환경에서 트랜잭션의 원자성을 보장하는 프로토콜입니다.

<strong>1단계: Prepare</strong>
<ul>
  <li>코디네이터가 모든 참여자에게 준비 요청</li>
</ul>
<ul>
  <li>참여자는 준비 완료 또는 중단 응답</li>
</ul>

<strong>2단계: Commit/Abort</strong>
<ul>
  <li>모든 참여자가 준비 완료 시 커밋 명령</li>
</ul>
<ul>
  <li>하나라도 중단 시 롤백 명령</li>
</ul>

<h2>12. NoSQL 데이터베이스</h2>

<h3>12.1 NoSQL 개요</h3>
관계형 데이터베이스의 제약을 벗어나 확장성과 성능을 중시하는 데이터베이스입니다.

<h4>NoSQL의 특징</h4>
<ul>
  <li>스키마가 없거나 유연함</li>
</ul>
<ul>
  <li>수평 확장성</li>
</ul>
<ul>
  <li>결국 일관성 (Eventually Consistent)</li>
</ul>
<ul>
  <li>분산 처리에 최적화</li>
</ul>

<h3>12.2 NoSQL 종류</h3>

<h4>키-값 저장소 (Key-Value Store)</h4>
<ul>
  <li>단순한 키-값 구조</li>
</ul>
<ul>
  <li>빠른 조회 성능</li>
</ul>
<ul>
  <li>예: Redis, DynamoDB, Riak</li>
</ul>

<h4>문서형 데이터베이스 (Document Database)</h4>
<ul>
  <li>JSON, XML 형태의 문서 저장</li>
</ul>
<ul>
  <li>중첩 구조 지원</li>
</ul>
<ul>
  <li>예: MongoDB, CouchDB</li>
</ul>

<h4>컬럼형 데이터베이스 (Column Family)</h4>
<ul>
  <li>컬럼 단위로 데이터 저장</li>
</ul>
<ul>
  <li>분석 쿼리에 적합</li>
</ul>
<ul>
  <li>예: Cassandra, HBase</li>
</ul>

<h4>그래프 데이터베이스 (Graph Database)</h4>
<ul>
  <li>노드와 엣지로 관계 표현</li>
</ul>
<ul>
  <li>복잡한 관계 분석에 적합</li>
</ul>
<ul>
  <li>예: Neo4j, Amazon Neptune</li>
</ul>

<h3>12.3 BASE 특성</h3>
NoSQL 데이터베이스의 특성을 나타냅니다.

<ul>
  <li><strong>BA (Basically Available)</strong>: 기본적으로 가용함</li>
</ul>
<ul>
  <li><strong>S (Soft State)</strong>: 일관성을 위해 지속적으로 상태 변경</li>
</ul>
<ul>
  <li><strong>E (Eventually Consistent)</strong>: 결국 일관성 달성</li>
</ul>

<h2>13. 데이터 웨어하우스와 빅데이터</h2>

<h3>13.1 데이터 웨어하우스</h3>
의사결정 지원을 위해 다양한 소스의 데이터를 통합, 저장하는 시스템입니다.

<h4>특징</h4>
<ul>
  <li>주제 지향적 (Subject-Oriented)</li>
</ul>
<ul>
  <li>통합적 (Integrated)</li>
</ul>
<ul>
  <li>시계열적 (Time-Variant)</li>
</ul>
<ul>
  <li>비휘발성 (Non-Volatile)</li>
</ul>

<h4>OLTP vs OLAP</h4>
<strong>OLTP (Online Transaction Processing)</strong>
<ul>
  <li>일상적인 업무 처리</li>
</ul>
<ul>
  <li>짧은 트랜잭션</li>
</ul>
<ul>
  <li>정규화된 구조</li>
</ul>
<ul>
  <li>높은 동시성</li>
</ul>

<strong>OLAP (Online Analytical Processing)</strong>
<ul>
  <li>분석 및 의사결정 지원</li>
</ul>
<ul>
  <li>복잡한 쿼리</li>
</ul>
<ul>
  <li>비정규화된 구조</li>
</ul>
<ul>
  <li>읽기 중심</li>
</ul>

<h3>13.2 데이터 마이닝</h3>
대량의 데이터에서 숨겨진 패턴이나 관계를 발견하는 과정입니다.

<h4>주요 기법</h4>
<ul>
  <li>분류 (Classification)</li>
</ul>
<ul>
  <li>군집화 (Clustering)</li>
</ul>
<ul>
  <li>연관 규칙 (Association Rules)</li>
</ul>
<ul>
  <li>순차 패턴 (Sequential Patterns)</li>
</ul>

<h3>13.3 빅데이터 처리</h3>

<h4>빅데이터의 3V</h4>
<ul>
  <li><strong>Volume</strong>: 대용량</li>
</ul>
<ul>
  <li><strong>Velocity</strong>: 빠른 속도</li>
</ul>
<ul>
  <li><strong>Variety</strong>: 다양성</li>
</ul>

<h4>분산 처리 프레임워크</h4>
<ul>
  <li><strong>Hadoop</strong>: 대용량 데이터 분산 저장 및 처리</li>
</ul>
<ul>
  <li><strong>Spark</strong>: 인메모리 기반 빠른 처리</li>
</ul>
<ul>
  <li><strong>MapReduce</strong>: 분산 병렬 처리 모델</li>
</ul>

<h2>14. 데이터베이스 보안</h2>

<h3>14.1 접근 제어</h3>

<h4>사용자 관리</h4>
<ul>
  <li>계정 생성 및 삭제</li>
</ul>
<ul>
  <li>비밀번호 정책</li>
</ul>
<ul>
  <li>역할 기반 접근 제어 (RBAC)</li>
</ul>

<h4>권한 관리</h4>
<ul>
  <li>객체 수준 권한</li>
</ul>
<ul>
  <li>시스템 수준 권한</li>
</ul>
<ul>
  <li>컬럼 수준 권한</li>
</ul>

<h3>14.2 데이터 암호화</h3>

<h4>저장 시 암호화 (Encryption at Rest)</h4>
<ul>
  <li>데이터 파일 암호화</li>
</ul>
<ul>
  <li>백업 파일 암호화</li>
</ul>

<h4>전송 시 암호화 (Encryption in Transit)</h4>
<ul>
  <li>SSL/TLS 프로토콜 사용</li>
</ul>
<ul>
  <li>네트워크 통신 보안</li>
</ul>

<h3>14.3 감사 (Auditing)</h3>
데이터베이스 접근과 변경 사항을 기록하고 모니터링하는 기능입니다.

<h4>감사 대상</h4>
<ul>
  <li>로그인/로그아웃</li>
</ul>
<ul>
  <li>데이터 변경</li>
</ul>
<ul>
  <li>스키마 변경</li>
</ul>
<ul>
  <li>권한 변경</li>
</ul>

<h2>15. 최신 데이터베이스 기술</h2>

<h3>15.1 인메모리 데이터베이스</h3>
데이터를 주로 메모리에 저장하여 빠른 처리 속도를 제공하는 데이터베이스입니다.

<strong>특징</strong>
<ul>
  <li>매우 빠른 응답 속도</li>
</ul>
<ul>
  <li>휘발성 데이터 위험</li>
</ul>
<ul>
  <li>높은 비용</li>
</ul>

<strong>예시</strong>
<ul>
  <li>Redis</li>
</ul>
<ul>
  <li>SAP HANA</li>
</ul>
<ul>
  <li>Oracle TimesTen</li>
</ul>

<h3>15.2 컬럼형 데이터베이스</h3>
데이터를 행 단위가 아닌 컬럼 단위로 저장하는 데이터베이스입니다.

<strong>장점</strong>
<ul>
  <li>분석 쿼리 성능 향상</li>
</ul>
<ul>
  <li>압축률 높음</li>
</ul>
<ul>
  <li>I/O 효율성</li>
</ul>

<strong>단점</strong>
<ul>
  <li>트랜잭션 처리에 불리</li>
</ul>
<ul>
  <li>행 단위 조회 시 성능 저하</li>
</ul>

<h3>15.3 뉴SQL</h3>
NoSQL의 확장성과 관계형 DB의 ACID 속성을 모두 제공하려는 데이터베이스입니다.

<strong>예시</strong>
<ul>
  <li>Google Spanner</li>
</ul>
<ul>
  <li>CockroachDB</li>
</ul>
<ul>
  <li>VoltDB</li>
</ul>

<h3>15.4 클라우드 데이터베이스</h3>
클라우드 환경에서 제공되는 데이터베이스 서비스입니다.

<strong>종류</strong>
<ul>
  <li><strong>DBaaS</strong>: 완전 관리형 서비스 (AWS RDS, Google Cloud SQL)</li>
</ul>
<ul>
  <li><strong>Serverless DB</strong>: 사용량에 따른 자동 확장 (Aurora Serverless)</li>
</ul>
<ul>
  <li><strong>Multi-model DB</strong>: 여러 데이터 모델 지원 (Amazon DocumentDB)</li>
</ul>

</div>
</details>
