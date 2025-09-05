---
layout: default
title: "데이터베이스 면접 대비 — 완전 정리"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>데이터베이스 면접 대비 — 기본·심화 Q&A + 개념 요약</h2>
  <p>구성: 기본 면접 Q&A → 심화 면접 Q&A → 추가 예상 질문 Q&A → 데이터베이스 개념 요약 노트</p>
</section>

<!-- ① 기본 면접 Q&A -->
<details open>
  <summary><span class="accordion-title">📋 기본 면접 Q&A</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <details>
    <summary style="font-size:1rem;"><b>Q1. 데이터베이스와 DBMS의 개념을 설명하고, 사용하는 이유를 말해주세요.</b></summary>
    <div class="accordion-content">
      <p>데이터베이스는 여러 사용자가 공유하여 사용할 목적으로 통합 관리되는 데이터의 집합입니다. DBMS(Database Management System)는 데이터베이스를 관리하고 운영하는 소프트웨어입니다. 데이터베이스를 사용하는 이유는 데이터 중복을 최소화하고 일관성을 유지하며, 데이터 독립성을 보장하여 응용 프로그램과 데이터를 분리할 수 있기 때문입니다. 또한 동시성 제어를 통해 여러 사용자가 동시에 접근할 수 있고, 보안과 무결성을 보장하며, 장애 발생 시 백업과 복구 기능을 제공합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q2. 관계형 데이터베이스(RDBMS)의 특징과 장단점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>관계형 데이터베이스는 데이터를 2차원 테이블 형태로 저장하고 관리하는 데이터베이스입니다. 테이블 간의 관계를 외래키로 연결하여 데이터의 무결성을 보장합니다. 주요 특징으로는 ACID 속성을 만족하여 트랜잭션의 안정성을 보장하고, SQL이라는 표준화된 질의 언어를 사용합니다. 장점으로는 데이터 일관성과 무결성이 우수하고, 복잡한 질의와 조인 연산이 가능하며, 성숙한 기술로 안정성이 높습니다. 단점으로는 수직적 확장만 가능하여 대용량 데이터 처리에 한계가 있고, 스키마 변경이 어려우며, 빅데이터나 비정형 데이터 처리에 적합하지 않습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q3. NoSQL 데이터베이스의 종류와 각각의 특징을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>NoSQL은 관계형 데이터베이스의 제약을 극복하기 위해 등장한 비관계형 데이터베이스입니다. 키-값 스토어는 Redis, DynamoDB가 대표적이며 단순한 구조로 빠른 읽기/쓰기가 가능합니다. 문서 지향 데이터베이스는 MongoDB, CouchDB가 있으며 JSON 형태의 문서를 저장하여 스키마 유연성이 좋습니다. 컬럼 패밀리는 Cassandra, HBase가 있으며 대용량 데이터의 분산 저장에 적합합니다. 그래프 데이터베이스는 Neo4j, Amazon Neptune이 있으며 관계 데이터 분석에 특화되어 있습니다. 각각은 수평적 확장성과 고성능을 제공하지만 ACID 보장이 약하고 복잡한 질의가 어렵습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q4. SQL의 DDL, DML, DCL, TCL을 구분하여 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>DDL(Data Definition Language)은 데이터베이스 구조를 정의하는 언어로 CREATE, ALTER, DROP, TRUNCATE가 있습니다. 테이블, 인덱스, 뷰 등의 객체를 생성하고 수정, 삭제할 때 사용하며 자동으로 커밋됩니다. DML(Data Manipulation Language)은 데이터를 조작하는 언어로 SELECT, INSERT, UPDATE, DELETE가 있습니다. 실제 데이터를 조회하고 추가, 수정, 삭제할 때 사용합니다. DCL(Data Control Language)은 데이터 접근 권한을 제어하는 언어로 GRANT, REVOKE가 있습니다. 사용자에게 권한을 부여하거나 회수할 때 사용합니다. TCL(Transaction Control Language)은 트랜잭션을 제어하는 언어로 COMMIT, ROLLBACK, SAVEPOINT가 있으며 트랜잭션의 시작과 종료를 관리합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q5. JOIN의 종류와 각각의 동작 방식을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>JOIN은 두 개 이상의 테이블을 연결하여 데이터를 조회하는 SQL 기법입니다. INNER JOIN은 양쪽 테이블에 모두 존재하는 데이터만 반환하며 가장 일반적으로 사용됩니다. LEFT OUTER JOIN은 왼쪽 테이블의 모든 데이터와 오른쪽 테이블의 매칭되는 데이터를 반환하고, 매칭되지 않으면 NULL로 채웁니다. RIGHT OUTER JOIN은 그 반대입니다. FULL OUTER JOIN은 양쪽 테이블의 모든 데이터를 반환하며, 매칭되지 않는 부분은 NULL로 처리됩니다. CROSS JOIN은 카테시안 곱으로 모든 조합을 반환하고, SELF JOIN은 같은 테이블을 자기 자신과 조인하는 방식입니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q6. 인덱스(Index)의 개념과 동작 원리, 장단점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>인덱스는 데이터베이스 테이블의 검색 속도를 향상시키기 위한 자료구조입니다. 테이블의 특정 컬럼값과 해당 레코드의 주소를 키-값 쌍으로 저장합니다. 대부분 B+Tree 구조를 사용하여 O(log n)의 시간복잡도로 빠른 검색이 가능합니다. 클러스터 인덱스는 테이블 데이터 자체가 인덱스 순서로 정렬되고, 논클러스터 인덱스는 별도의 구조로 관리됩니다. 장점으로는 SELECT 성능이 크게 향상되고 ORDER BY, GROUP BY의 성능도 개선됩니다. 단점으로는 추가 저장공간이 필요하고, INSERT, UPDATE, DELETE 시 인덱스도 함께 수정되어 성능 저하가 발생할 수 있습니다. 또한 잘못 설계된 인덱스는 오히려 성능을 떨어뜨릴 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q7. 정규화(Normalization)의 개념과 1NF, 2NF, 3NF를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>정규화는 데이터의 중복을 최소화하고 일관성을 유지하기 위해 테이블을 분해하는 과정입니다. 제1정규형(1NF)은 테이블의 모든 속성이 원자값을 가져야 하며, 반복 그룹이 없어야 합니다. 즉, 하나의 셀에는 하나의 값만 들어가야 합니다. 제2정규형(2NF)은 1NF를 만족하면서 부분적 함수 종속을 제거한 형태입니다. 기본키가 아닌 모든 속성이 기본키에 완전 함수 종속되어야 합니다. 제3정규형(3NF)은 2NF를 만족하면서 이행적 함수 종속을 제거한 형태입니다. 기본키가 아닌 속성들 간에 종속 관계가 없어야 합니다. 정규화를 통해 데이터 중복과 갱신 이상을 방지할 수 있지만, 과도한 정규화는 조인 연산을 증가시켜 성능 저하를 일으킬 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q8. 트랜잭션(Transaction)과 ACID 속성을 상세히 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>트랜잭션은 데이터베이스에서 하나의 논리적 작업 단위로 실행되는 일련의 연산들입니다. 모든 연산이 성공하거나 모든 연산이 실패하는 All-or-Nothing 방식으로 동작합니다. ACID는 트랜잭션이 만족해야 하는 네 가지 속성입니다. 원자성(Atomicity)은 트랜잭션의 연산들이 모두 성공하거나 모두 실패해야 함을 의미합니다. 일관성(Consistency)은 트랜잭션 실행 전후에 데이터베이스가 일관된 상태를 유지해야 함을 뜻합니다. 격리성(Isolation)은 동시에 실행되는 트랜잭션들이 서로 영향을 주지 않아야 함을 의미합니다. 지속성(Durability)은 성공적으로 완료된 트랜잭션의 결과가 시스템 장애가 발생해도 영구적으로 보존되어야 함을 의미합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q9. 트랜잭션 격리 수준(Isolation Level)의 종류와 발생 가능한 문제들을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>격리 수준은 동시에 실행되는 트랜잭션들 간의 격리 정도를 나타냅니다. READ UNCOMMITTED는 가장 낮은 격리 수준으로 커밋되지 않은 데이터도 읽을 수 있어 Dirty Read가 발생할 수 있습니다. READ COMMITTED는 커밋된 데이터만 읽을 수 있지만 Non-Repeatable Read가 발생할 수 있습니다. REPEATABLE READ는 트랜잭션 동안 같은 데이터를 반복 읽으면 같은 결과를 보장하지만 Phantom Read가 발생할 수 있습니다. SERIALIZABLE은 가장 높은 격리 수준으로 완전한 격리를 보장하지만 성능이 가장 떨어집니다. Dirty Read는 커밋되지 않은 데이터를 읽는 현상, Non-Repeatable Read는 같은 데이터를 다시 읽었을 때 다른 값이 읽히는 현상, Phantom Read는 같은 조건으로 조회했을 때 이전에 없던 레코드가 나타나는 현상입니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q10. 동시성 제어를 위한 Lock의 종류와 Deadlock을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>Lock은 동시에 실행되는 트랜잭션들이 같은 데이터에 접근할 때 일관성을 보장하기 위한 메커니즘입니다. Shared Lock(S-Lock)은 읽기 전용 잠금으로 다른 트랜잭션의 읽기는 허용하지만 쓰기는 차단합니다. Exclusive Lock(X-Lock)은 배타적 잠금으로 다른 트랜잭션의 읽기와 쓰기를 모두 차단합니다. 범위에 따라 행 수준 잠금, 페이지 수준 잠금, 테이블 수준 잠금으로 구분됩니다. Deadlock은 두 개 이상의 트랜잭션이 서로가 보유한 자원을 기다리며 무한정 대기하는 상황입니다. 예방 방법으로는 Lock 순서를 일정하게 유지하거나, Lock 타임아웃을 설정하는 방법이 있습니다. 탐지 및 해결 방법으로는 Wait-for Graph를 이용한 탐지나 희생자 선택을 통한 해결이 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q11. MVCC(Multi-Version Concurrency Control)의 동작 원리를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>MVCC는 동시성 제어를 위해 데이터의 여러 버전을 유지하는 기법입니다. 각 트랜잭션마다 고유한 타임스탬프나 버전 번호를 할당하고, 데이터를 수정할 때 새로운 버전을 생성합니다. 읽기 트랜잭션은 자신의 시작 시점에 존재했던 데이터 버전을 읽어 일관된 스냅샷을 제공합니다. 이를 통해 읽기 작업에서는 Lock을 사용하지 않아도 되므로 읽기와 쓰기 간의 충돌을 줄일 수 있습니다. PostgreSQL, Oracle, MySQL의 InnoDB 엔진에서 사용되며, 동시성은 향상되지만 과거 버전 데이터를 저장하기 위한 추가 공간이 필요하고, 가비지 컬렉션이 필요합니다. 또한 Write Skew와 같은 특수한 이상 현상이 발생할 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q12. 데이터베이스 설계 시 고려해야 할 요소들을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>데이터베이스 설계 시 가장 먼저 요구사항 분석을 통해 필요한 데이터와 기능을 파악해야 합니다. 개념적 설계에서는 ER 다이어그램을 작성하여 엔티티와 관계를 정의하고, 논리적 설계에서는 테이블 구조와 스키마를 설계합니다. 물리적 설계에서는 인덱스, 파티션, 클러스터링 등을 고려합니다. 성능 측면에서는 쿼리 패턴을 분석하여 적절한 인덱스를 설계하고, 정규화와 반정규화의 균형을 맞춰야 합니다. 확장성을 위해 파티셔닝이나 샤딩을 고려하고, 보안을 위해 접근 권한과 암호화를 설계해야 합니다. 또한 백업과 복구 전략, 모니터링 방안도 함께 계획해야 합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q13. Primary Key와 Foreign Key의 역할과 특징을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>Primary Key는 테이블에서 각 행을 유일하게 식별하는 컬럼 또는 컬럼들의 조합입니다. NULL 값을 가질 수 없고, 중복될 수 없으며, 한 테이블에 하나만 존재할 수 있습니다. 자동으로 인덱스가 생성되어 검색 성능이 향상되고, 클러스터 인덱스의 기준이 됩니다. Foreign Key는 다른 테이블의 Primary Key를 참조하는 컬럼으로, 테이블 간의 관계를 나타내고 참조 무결성을 보장합니다. 참조하는 값이 참조되는 테이블에 반드시 존재해야 하며, NULL 값을 가질 수 있습니다. CASCADE, SET NULL, RESTRICT 등의 옵션으로 참조되는 데이터 변경 시의 동작을 정의할 수 있습니다. 이를 통해 데이터의 일관성과 무결성을 자동으로 보장할 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q14. 뷰(View)의 개념과 장단점, 종류를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>뷰는 하나 이상의 테이블로부터 유도되는 가상 테이블입니다. 실제 데이터를 저장하지 않고 정의만 저장하며, 조회 시 기본 테이블로부터 동적으로 데이터를 가져옵니다. 장점으로는 복잡한 쿼리를 단순화하고, 보안을 위해 특정 컬럼만 노출할 수 있으며, 논리적 데이터 독립성을 제공합니다. 또한 여러 사용자가 다른 관점에서 동일한 데이터를 볼 수 있게 해줍니다. 단점으로는 뷰를 통한 삽입, 수정, 삭제가 제한적이고, 복잡한 뷰는 성능이 떨어질 수 있습니다. 종류로는 일반 뷰와 구체화된 뷰(Materialized View)가 있으며, 구체화된 뷰는 실제 데이터를 저장하여 성능을 향상시키지만 데이터 동기화 문제가 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q15. 데이터베이스 백업과 복구 전략을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>데이터베이스 백업은 시스템 장애나 데이터 손실에 대비하여 데이터를 안전한 곳에 복사하는 작업입니다. 전체 백업은 데이터베이스 전체를 백업하는 방식으로 복구가 간단하지만 시간과 저장공간이 많이 필요합니다. 증분 백업은 이전 백업 이후 변경된 부분만 백업하여 효율적이지만 복구가 복잡합니다. 차등 백업은 전체 백업 이후 변경된 모든 부분을 백업합니다. 핫 백업은 데이터베이스 운영 중에 수행하고, 콜드 백업은 데이터베이스를 정지한 상태에서 수행합니다. 복구 전략으로는 Point-in-Time Recovery를 통해 특정 시점으로 복구하거나, 트랜잭션 로그를 이용한 복구가 있습니다. RTO(Recovery Time Objective)와 RPO(Recovery Point Objective)를 고려하여 적절한 백업 주기와 방법을 선택해야 합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q16. 스토어드 프로시저(Stored Procedure)와 트리거(Trigger)를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>스토어드 프로시저는 데이터베이스에 저장되는 프로그램으로, 여러 SQL 문을 하나의 단위로 묶어 실행할 수 있습니다. 매개변수를 받아 처리하고 결과를 반환할 수 있으며, 조건문과 반복문 등의 제어 구조를 사용할 수 있습니다. 장점으로는 성능 향상(컴파일된 코드 재사용), 네트워크 트래픽 감소, 보안 강화, 비즈니스 로직 중앙 집중화가 있습니다. 단점으로는 데이터베이스 의존성이 높고 디버깅이 어려우며, 버전 관리가 복잡합니다. 트리거는 특정 이벤트(INSERT, UPDATE, DELETE)가 발생할 때 자동으로 실행되는 특수한 프로시저입니다. BEFORE 트리거는 이벤트 발생 전에, AFTER 트리거는 발생 후에 실행되며, 데이터 무결성 유지, 로깅, 알림 등에 사용됩니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q17. 파티셔닝(Partitioning)의 개념과 종류를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>파티셔닝은 대용량 테이블을 작은 단위로 분할하여 관리하는 기법입니다. 논리적으로는 하나의 테이블이지만 물리적으로는 여러 개의 세그먼트로 분할됩니다. 수평 파티셔닝은 행을 기준으로 분할하는 방식으로, 범위 파티셔닝은 특정 컬럼의 값 범위로, 해시 파티셔닝은 해시 함수로, 리스트 파티셔닝은 특정 값 목록으로 분할합니다. 수직 파티셔닝은 컬럼을 기준으로 분할합니다. 장점으로는 쿼리 성능 향상(파티션 제거), 관리 용이성(파티션별 백업/복구), 가용성 향상이 있습니다. 단점으로는 조인 성능 저하 가능성, 관리 복잡성 증가, 파티션 키 선택의 중요성이 있습니다. 적절한 파티션 키 선택이 성능에 결정적 영향을 미칩니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q18. SQL 쿼리 최적화 방법들을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>쿼리 최적화는 실행 시간을 단축하고 자원 사용량을 줄이는 것이 목표입니다. 인덱스를 적절히 활용하여 WHERE, ORDER BY, GROUP BY 절의 성능을 향상시킬 수 있습니다. SELECT절에서 필요한 컬럼만 조회하고, WHERE절에서 조건을 최대한 활용하여 데이터를 줄여야 합니다. JOIN 순서를 최적화하고, 가능하면 INNER JOIN을 사용하며, 서브쿼리보다는 JOIN을 사용하는 것이 좋습니다. LIKE 연산자는 앞부분 와일드카드(%)를 피하고, 함수 사용을 최소화해야 합니다. DISTINCT 대신 GROUP BY를 사용하고, UNION ALL이 UNION보다 빠릅니다. 실행 계획을 분석하여 비효율적인 부분을 찾고, 통계 정보를 최신으로 유지해야 합니다. 배치 처리 시에는 큰 트랜잭션을 작은 단위로 나누는 것이 좋습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q19. 데이터베이스 커넥션 풀(Connection Pool)의 개념과 중요성을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>커넥션 풀은 데이터베이스 연결을 미리 생성하여 풀에 저장해두고 재사용하는 기법입니다. 애플리케이션에서 데이터베이스에 접근할 때마다 새로운 연결을 생성하고 해제하는 오버헤드를 줄일 수 있습니다. 주요 매개변수로는 최소 연결 수, 최대 연결 수, 연결 대기 시간, 유휴 연결 타임아웃이 있습니다. 장점으로는 연결 생성/해제 비용 절약, 동시 연결 수 제한으로 데이터베이스 부하 방지, 응답 시간 단축이 있습니다. 적절한 풀 크기 설정이 중요한데, 너무 작으면 대기 시간이 길어지고, 너무 크면 메모리 낭비와 데이터베이스 부하가 증가합니다. 일반적으로 동시 사용자 수, 평균 쿼리 실행 시간, 서버 리소스를 고려하여 설정하며, 모니터링을 통해 지속적으로 조정해야 합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q20. OLTP와 OLAP의 차이점과 각각의 특징을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>OLTP(Online Transaction Processing)는 일상적인 거래 처리를 위한 시스템으로, 짧고 빈번한 트랜잭션을 처리합니다. 정규화된 데이터베이스 구조를 사용하고, 삽입, 수정, 삭제 작업이 많으며, 응답 시간이 매우 중요합니다. 동시성과 일관성이 핵심이고, 상세한 실시간 데이터를 다룹니다. 예시로는 온라인 뱅킹, 주문 처리, 재고 관리 시스템이 있습니다. OLAP(Online Analytical Processing)는 의사결정 지원을 위한 분석 시스템으로, 복잡한 집계 쿼리를 처리합니다. 반정규화된 스타 스키마나 스노플레이크 스키마를 사용하고, 주로 읽기 작업이며, 대용량 데이터를 처리합니다. 과거 데이터의 추세와 패턴 분석이 주목적이며, 응답 시간보다는 처리량이 중요합니다. 예시로는 데이터 웨어하우스, 비즈니스 인텔리전스, 리포팅 시스템이 있습니다.</p>
    </div>
  </details>

  </div>
</details>

<!-- ② 심화 면접 Q&A -->
<details>
  <summary><span class="accordion-title">🚀 심화 면접 Q&A</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <details>
    <summary style="font-size:1rem;"><b>Q21. 분산 데이터베이스와 CAP 정리를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>분산 데이터베이스는 여러 노드에 걸쳐 데이터를 저장하고 관리하는 시스템입니다. CAP 정리는 분산 시스템에서 일관성(Consistency), 가용성(Availability), 분할 내성(Partition tolerance) 중 최대 두 가지만 동시에 보장할 수 있다는 이론입니다. 일관성은 모든 노드가 동시에 같은 데이터를 보는 것이고, 가용성은 시스템이 계속 동작하는 것이며, 분할 내성은 네트워크 장애에도 시스템이 동작하는 것입니다. CP 시스템은 일관성과 분할 내성을 보장하지만 가용성을 포기하고, AP 시스템은 가용성과 분할 내성을 보장하지만 일관성을 포기합니다. 실제로는 네트워크 분할이 발생할 수 있으므로 CA 시스템은 현실적으로 불가능하며, 대부분 CP 또는 AP 시스템 중 선택해야 합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q22. 샤딩(Sharding)의 개념과 구현 방법, 문제점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>샤딩은 대용량 데이터베이스를 수평으로 분할하여 여러 서버에 분산 저장하는 기법입니다. 각 샤드는 독립적인 데이터베이스 인스턴스로 동작하며, 전체 데이터의 일부분을 담당합니다. 구현 방법으로는 해시 기반 샤딩, 범위 기반 샤딩, 디렉토리 기반 샤딩이 있습니다. 해시 샤딩은 샤드 키를 해시하여 균등 분산하지만 범위 쿼리가 어렵고, 범위 샤딩은 범위 쿼리에 유리하지만 핫스팟이 발생할 수 있습니다. 장점으로는 선형적 확장성, 성능 향상, 장애 격리가 있습니다. 문제점으로는 크로스 샤드 조인의 복잡성, 리샤딩의 어려움, 트랜잭션 처리 복잡성, 데이터 일관성 문제가 있습니다. 샤드 키 선택이 매우 중요하며, 애플리케이션 레벨에서의 복잡성이 증가합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q23. 복제(Replication)의 종류와 마스터-슬레이브 구조를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>데이터베이스 복제는 데이터의 복사본을 여러 서버에 유지하는 기법입니다. 동기 복제는 모든 복제본에 동시에 쓰기가 완료되면 트랜잭션이 커밋되어 강한 일관성을 보장하지만 성능과 가용성이 떨어집니다. 비동기 복제는 마스터에서 커밋된 후 복제본에 비동기적으로 전파되어 성능은 좋지만 데이터 손실 가능성이 있습니다. 반동기 복제는 적어도 하나의 슬레이브에는 동기적으로 전파하는 절충안입니다. 마스터-슬레이브 구조에서는 마스터가 쓰기를 처리하고 슬레이브가 읽기를 처리하여 읽기 성능을 향상시킵니다. 마스터 장애 시 슬레이브를 마스터로 승격하는 페일오버 과정이 필요하며, 이때 일시적인 데이터 불일치가 발생할 수 있습니다. 스플릿 브레인 문제를 방지하기 위한 적절한 장애 감지와 조치가 필요합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q24. 데이터 웨어하우스와 ETL 프로세스를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>데이터 웨어하우스는 의사결정 지원을 위해 여러 소스로부터 수집된 통합 데이터를 저장하는 중앙 저장소입니다. 주제 중심적이고, 통합되어 있으며, 시간에 따라 변하지 않고, 비휘발성의 특징을 가집니다. 스타 스키마나 스노플레이크 스키마를 사용하여 차원 테이블과 팩트 테이블로 구성됩니다. ETL은 Extract, Transform, Load의 과정으로 데이터 웨어하우스 구축의 핵심입니다. Extract는 다양한 소스로부터 데이터를 추출하고, Transform은 데이터를 정제, 변환, 집계하며, Load는 데이터 웨어하우스에 적재합니다. 최근에는 ELT(Extract, Load, Transform) 방식도 사용되며, 클라우드 환경에서는 대용량 처리를 위해 분산 처리 엔진을 활용합니다. 데이터 품질 관리, 메타데이터 관리, 증분 로딩 전략이 중요한 고려사항입니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q25. 데이터베이스 성능 튜닝 방법론을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>데이터베이스 성능 튜닝은 체계적인 접근이 필요합니다. 먼저 성능 지표를 수집하여 병목지점을 식별해야 합니다. 응답시간, 처리량, 자원 사용률, 대기 이벤트를 모니터링하고, AWR(Automatic Workload Repository)이나 Performance Schema 등의 도구를 활용합니다. SQL 튜닝에서는 실행계획을 분석하여 비효율적인 접근 방법을 찾고, 인덱스 스캔 대신 풀 테이블 스캔이 발생하는 이유를 파악합니다. 인덱스 튜닝에서는 사용되지 않는 인덱스 제거, 복합 인덱스 컬럼 순서 최적화, 커버링 인덱스 활용을 고려합니다. 시스템 튜닝에서는 메모리 할당, I/O 서브시스템, CPU 사용률을 최적화하고, 병렬 처리와 파티셔닝을 활용합니다. 지속적인 모니터링과 성능 테스트를 통해 개선 효과를 검증해야 합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q26. NewSQL과 전통적 RDBMS의 차이점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>NewSQL은 NoSQL의 확장성과 RDBMS의 ACID 속성을 결합한 새로운 데이터베이스 유형입니다. 전통적 RDBMS의 SQL 지원과 트랜잭션 보장을 유지하면서 수평적 확장성을 제공합니다. 기존 RDBMS가 단일 노드 또는 제한적인 클러스터에서 동작하는 반면, NewSQL은 분산 아키텍처를 기본으로 설계되었습니다. 전통적 RDBMS는 잠금 기반 동시성 제어를 사용하지만, NewSQL은 MVCC나 최적화된 잠금 메커니즘을 사용합니다. 스토리지 엔진도 SSD에 최적화되거나 인메모리 처리를 지원합니다. 대표적인 NewSQL로는 Google Spanner, CockroachDB, VoltDB, MemSQL 등이 있습니다. 하지만 복잡성 증가, 운영 비용 상승, 상대적으로 짧은 검증 기간 등의 단점도 있어 신중한 선택이 필요합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q27. 데이터베이스 보안 위협과 대응 방안을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>데이터베이스는 조직의 핵심 정보를 담고 있어 다양한 보안 위협에 노출됩니다. SQL 인젝션은 가장 일반적인 공격으로 prepared statement와 입력값 검증으로 방지할 수 있습니다. 권한 상승 공격은 최소 권한 원칙과 역할 기반 접근 제어로 대응합니다. 내부자 위협은 감사 로그와 접근 모니터링으로 탐지하고, 중요 데이터는 암호화합니다. 데이터 유출 방지를 위해 DLP(Data Loss Prevention) 솔루션을 도입하고, 네트워크 세분화를 통해 데이터베이스 접근을 제한합니다. 백업 데이터의 보안도 중요하며, 암호화와 접근 제어를 적용해야 합니다. 정기적인 보안 감사, 취약점 스캐닝, 침투 테스트를 통해 보안 수준을 점검하고, 개인정보보호법 등 관련 규정을 준수해야 합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q28. 인메모리 데이터베이스의 특징과 활용 분야를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>인메모리 데이터베이스는 모든 데이터를 메모리에 저장하여 극도로 빠른 성능을 제공하는 데이터베이스입니다. 디스크 I/O를 제거하여 마이크로초 단위의 응답시간을 달성할 수 있지만, 메모리 비용이 높고 휘발성이라는 단점이 있습니다. 지속성을 위해 스냅샷이나 트랜잭션 로그를 디스크에 저장하며, 클러스터링을 통해 고가용성을 보장합니다. 컬럼 지향 저장, 압축, 병렬 처리 등의 기술을 활용하여 분석 성능을 극대화합니다. 실시간 분석, 고빈도 트레이딩, 실시간 추천 시스템, 세션 스토어, 캐싱 등에 활용됩니다. SAP HANA, Redis, Apache Ignite, VoltDB 등이 대표적이며, 최근에는 하이브리드 방식으로 자주 사용되는 데이터만 메모리에 두고 나머지는 디스크에 저장하는 방식도 사용됩니다.</p>
    </div>
  </details>

  </div>
</details>

<!-- ③ 추가 예상 질문 Q&A -->
<details>
  <summary><span class="accordion-title">💡 추가 예상 질문 Q&A</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <details>
    <summary style="font-size:1rem;"><b>Q29. 클라우드 데이터베이스의 장점과 고려사항을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>클라우드 데이터베이스는 클라우드 환경에서 제공되는 관리형 데이터베이스 서비스입니다. 주요 장점으로는 초기 투자 비용 절감, 자동 확장성, 관리 부담 경감, 고가용성 및 재해 복구 기능 제공이 있습니다. 하드웨어 구매나 설치 없이 바로 사용할 수 있고, 사용량에 따른 탄력적 요금제가 적용됩니다. 자동 백업, 모니터링, 보안 패치 등이 제공되어 운영 복잡성이 줄어듭니다. 하지만 네트워크 지연 시간, 벤더 종속성, 데이터 보안 및 컴플라이언스 문제를 고려해야 합니다. 특히 금융이나 의료 분야에서는 데이터 거버넌스가 중요한 이슈입니다. 비용 최적화를 위해 적절한 인스턴스 타입 선택과 리소스 모니터링이 필요하며, 멀티 클라우드 전략을 통해 벤더 종속성을 완화할 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q30. 시계열 데이터베이스(TSDB)의 특징과 사용 사례를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>시계열 데이터베이스는 시간 순서로 정렬된 데이터를 효율적으로 저장하고 처리하는 특화된 데이터베이스입니다. IoT 센서 데이터, 서버 메트릭, 주식 가격, 로그 데이터 등을 처리하는 데 최적화되어 있습니다. 주요 특징으로는 높은 쓰기 처리량, 시간 기반 압축, 자동 데이터 보존 정책, 시간 창 기반 집계 기능이 있습니다. 과거 데이터는 압축하거나 다운샘플링하여 저장 공간을 절약하고, TTL(Time To Live)을 통해 오래된 데이터를 자동 삭제합니다. 특화된 쿼리 언어를 제공하여 시간 범위 조회, 집계, 보간 등을 효율적으로 수행할 수 있습니다. InfluxDB, TimescaleDB, OpenTSDB, Amazon Timestream 등이 대표적이며, 모니터링, IoT, 금융 데이터 분석 등의 분야에서 널리 사용됩니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q31. 그래프 데이터베이스의 개념과 활용 분야를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>그래프 데이터베이스는 노드(엔티티)와 엣지(관계)로 데이터를 표현하는 NoSQL 데이터베이스입니다. 관계형 데이터베이스에서 복잡한 JOIN으로 처리해야 하는 관계 데이터를 직관적이고 효율적으로 저장할 수 있습니다. 노드는 속성을 가질 수 있고, 엣지는 방향성과 타입, 속성을 가질 수 있습니다. 그래프 순회 알고리즘을 통해 최단 경로, 중심성 분석, 커뮤니티 탐지 등의 복잡한 분석이 가능합니다. Cypher(Neo4j), Gremlin(Apache TinkerPop) 등의 그래프 쿼리 언어를 사용합니다. 소셜 네트워크 분석, 추천 시스템, 사기 탐지, 지식 그래프, 네트워크 분석, 바이오인포매틱스 등에 활용됩니다. Neo4j, Amazon Neptune, ArangoDB, TigerGraph 등이 대표적이며, 관계의 깊이나 복잡성이 중요한 도메인에서 관계형 데이터베이스보다 우수한 성능을 보입니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q32. 데이터 레이크와 데이터 웨어하우스의 차이점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>데이터 레이크는 정형, 반정형, 비정형 데이터를 원본 형태 그대로 저장하는 중앙 저장소입니다. 스키마-온-리드 방식으로 데이터를 먼저 저장하고 사용할 때 스키마를 정의합니다. 확장성이 뛰어나고 비용이 저렴하며, 다양한 분석 도구와 연동이 가능합니다. 데이터 웨어하우스는 정형 데이터를 미리 정의된 스키마에 따라 저장하는 시스템으로, 스키마-온-라이트 방식을 사용합니다. 높은 성능과 일관성을 제공하지만 구조 변경이 어렵고 비용이 높습니다. 데이터 레이크는 탐색적 분석, 머신러닝, 실시간 스트리밍에 적합하고, 데이터 웨어하우스는 정형화된 비즈니스 보고서와 대시보드에 적합합니다. 최근에는 두 장점을 결합한 레이크하우스(Delta Lake, Apache Iceberg) 아키텍처가 주목받고 있으며, 데이터 거버넌스와 품질 관리가 핵심 과제입니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q33. 데이터베이스 마이그레이션 전략과 고려사항을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>데이터베이스 마이그레이션은 시스템 업그레이드, 클라우드 전환, 벤더 변경 등의 이유로 수행됩니다. 마이그레이션 유형으로는 버전 업그레이드, 플랫폼 변경, 클라우드 마이그레이션이 있습니다. Big Bang 방식은 한 번에 전환하여 빠르지만 위험이 크고, 단계적 마이그레이션은 안전하지만 시간이 오래 걸립니다. 병렬 운영 방식은 두 시스템을 동시에 운영하며 점진적으로 전환합니다. 주요 고려사항으로는 데이터 타입 호환성, 스키마 변환, 애플리케이션 코드 수정, 성능 영향, 다운타임 최소화가 있습니다. 철저한 사전 테스트와 롤백 계획이 필수이며, 데이터 무결성 검증과 성능 테스트를 반복해야 합니다. AWS DMS, Azure Database Migration Service 등의 도구를 활용할 수 있으며, 전문 컨설팅을 통해 위험을 최소화하는 것이 좋습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q34. 실시간 데이터 처리와 스트림 처리 데이터베이스를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>실시간 데이터 처리는 데이터가 생성되는 즉시 처리하여 결과를 제공하는 방식입니다. 배치 처리와 달리 지연 시간이 매우 중요하며, 스트리밍 데이터를 연속적으로 처리합니다. 스트림 처리 엔진은 Apache Kafka, Apache Storm, Apache Flink, Amazon Kinesis 등이 있으며, 이벤트 시간과 처리 시간의 차이를 고려한 윈도우 연산을 지원합니다. 스트림 데이터베이스는 실시간 쿼리를 지원하는 특수한 데이터베이스로, 시간 윈도우 기반 집계, 이벤트 패턴 매칭, 복합 이벤트 처리가 가능합니다. 실시간 추천, 사기 탐지, IoT 모니터링, 실시간 대시보드 등에 활용됩니다. 주요 고려사항으로는 처리량과 지연시간의 균형, 장애 처리와 정확성 보장, 백프레셀(backpressure) 처리가 있으며, 람다 아키텍처나 카파 아키텍처 등의 설계 패턴을 사용합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q35. 데이터베이스 DevOps와 CI/CD 파이프라인을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>데이터베이스 DevOps는 데이터베이스 변경을 애플리케이션 코드처럼 버전 관리하고 자동화하는 접근법입니다. 스키마 변경, 데이터 마이그레이션, 설정 변경을 코드로 관리하여 일관성과 추적성을 보장합니다. CI/CD 파이프라인에서는 데이터베이스 변경사항을 자동으로 테스트하고 배포합니다. 스키마 마이그레이션 스크립트를 버전 관리 시스템에 저장하고, Flyway나 Liquibase 같은 도구로 자동 적용합니다. 데이터베이스 단위 테스트, 통합 테스트, 성능 테스트를 자동화하고, 테스트 데이터를 일관되게 관리합니다. 환경별(개발, 테스트, 운영) 설정을 분리하고, 블루-그린 배포나 카나리 배포를 통해 무중단 배포를 구현합니다. 모니터링과 알람을 자동화하여 문제를 조기에 발견하고, 롤백 절차를 표준화합니다. 이를 통해 배포 속도 향상, 오류 감소, 협업 개선 효과를 얻을 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q36. 프라이버시 보호와 데이터 마스킹 기법을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>개인정보보호법 강화로 데이터베이스에서 개인정보를 안전하게 처리하는 기법이 중요해졌습니다. 데이터 마스킹은 민감한 데이터를 실제값과 유사하지만 의미 없는 값으로 대체하는 기법입니다. 정적 마스킹은 테스트 환경 구축 시 사용하고, 동적 마스킹은 실시간으로 권한에 따라 다른 데이터를 제공합니다. 암호화는 데이터 자체를 변환하여 키 없이는 해독할 수 없게 만들며, 투명한 데이터 암호화(TDE)는 파일 레벨에서, 컬럼 레벨 암호화는 필드별로 적용됩니다. 토큰화는 민감 데이터를 무의미한 토큰으로 대체하고 별도 시스템에서 매핑 정보를 관리합니다. 차분 프라이버시는 통계적 분석 결과에 노이즈를 추가하여 개별 데이터를 보호하며, 동형 암호는 암호화된 상태에서 연산이 가능합니다. GDPR, CCPA 등의 규정 준수를 위해 데이터 생명주기 관리와 삭제 권한 지원도 중요합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q37. 데이터베이스 모니터링과 성능 진단 방법을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>데이터베이스 모니터링은 시스템 안정성과 성능을 보장하기 위한 필수 활동입니다. 주요 모니터링 지표로는 응답시간, 처리량(TPS/QPS), 연결 수, CPU/메모리 사용률, I/O 대기시간, 락 대기시간이 있습니다. 슬로우 쿼리 로그를 통해 비효율적인 쿼리를 식별하고, 실행계획을 분석하여 최적화 포인트를 찾습니다. 대기 이벤트 분석으로 병목지점을 파악하고, 버퍼 캐시 히트율, 락 경합, 데드락 발생 빈도를 모니터링합니다. APM(Application Performance Monitoring) 도구나 데이터베이스 전용 모니터링 솔루션을 활용하여 실시간 모니터링과 알림을 설정합니다. 성능 기준선(baseline)을 설정하고 임계치 초과 시 자동 알림을 받습니다. 정기적인 성능 리포트를 통해 트렌드를 분석하고, 용량 계획과 성능 튜닝에 활용합니다. 장애 발생 시 신속한 원인 분석을 위해 성능 히스토리를 보관하고, 자동화된 진단 스크립트를 준비해야 합니다.</p>
    </div>
  </details>

  </div>
</details>

<!-- ④ 데이터베이스 개념 요약 노트 -->
<details>
  <summary><span class="accordion-title">📚 데이터베이스 개념 요약 노트</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <h3>🏗️ 데이터베이스 기초</h3>
  <p><b>DBMS 유형</b></p>
  <pre><code>관계형 DBMS (RDBMS)
├── Oracle, MySQL, PostgreSQL, SQL Server
├── ACID 속성 보장
├── SQL 표준 지원
└── 정규화된 스키마

NoSQL DBMS
├── 키-값: Redis, DynamoDB
├── 문서: MongoDB, CouchDB
├── 컬럼: Cassandra, HBase
├── 그래프: Neo4j, Neptune
└── 유연한 스키마, 수평 확장</code></pre>

  <p><b>데이터 모델링</b></p>
  <ul>
    <li>개념적 모델링: ER 다이어그램</li>
    <li>논리적 모델링: 테이블 설계</li>
    <li>물리적 모델링: 인덱스, 파티션</li>
    <li>정규화 vs 반정규화 균형</li>
  </ul>

  <h3>📊 SQL 기본</h3>
  <p><b>DML 성능 최적화</b></p>
  <ul>
    <li>SELECT: 필요한 컬럼만 조회</li>
    <li>WHERE: 인덱스 활용 조건</li>
    <li>JOIN: 적절한 조인 순서</li>
    <li>GROUP BY: 인덱스 컬럼 활용</li>
  </ul>

  <p><b>JOIN 성능 비교</b></p>
  <table>
    <thead>
      <tr><th>JOIN 타입</th><th>특징</th><th>사용 시기</th></tr>
    </thead>
    <tbody>
      <tr><td>INNER</td><td>교집합</td><td>매칭 데이터만</td></tr>
      <tr><td>LEFT OUTER</td><td>왼쪽 전체</td><td>기준 테이블 보존</td></tr>
      <tr><td>FULL OUTER</td><td>합집합</td><td>모든 데이터 필요</td></tr>
      <tr><td>CROSS</td><td>곱집합</td><td>조합 생성</td></tr>
    </tbody>
  </table>

  <h3>🔍 인덱스 전략</h3>
  <p><b>인덱스 유형</b></p>
  <ul>
    <li>B-Tree: 일반적인 인덱스 (범위, 정렬)</li>
    <li>Hash: 등치 검색에 최적화</li>
    <li>Bitmap: 카디널리티가 낮은 컬럼</li>
    <li>복합 인덱스: 여러 컬럼 조합</li>
  </ul>

  <p><b>인덱스 설계 원칙</b></p>
  <ol>
    <li>선택도가 높은 컬럼</li>
    <li>WHERE 절에 자주 사용되는 컬럼</li>
    <li>ORDER BY, GROUP BY 컬럼</li>
    <li>복합 인덱스의 컬럼 순서 중요</li>
    <li>DML 성능 고려</li>
  </ol>

  <h3>🔒 트랜잭션 관리</h3>
  <p><b>ACID 속성</b></p>
  <ul>
    <li><b>원자성(Atomicity)</b>: All or Nothing</li>
    <li><b>일관성(Consistency)</b>: 제약조건 유지</li>
    <li><b>격리성(Isolation)</b>: 동시성 제어</li>
    <li><b>지속성(Durability)</b>: 영구 저장</li>
  </ul>

  <p><b>격리 수준별 문제</b></p>
  <table>
    <thead>
      <tr><th>격리 수준</th><th>Dirty Read</th><th>Non-Repeatable</th><th>Phantom</th></tr>
    </thead>
    <tbody>
      <tr><td>READ UNCOMMITTED</td><td>O</td><td>O</td><td>O</td></tr>
      <tr><td>READ COMMITTED</td><td>X</td><td>O</td><td>O</td></tr>
      <tr><td>REPEATABLE READ</td><td>X</td><td>X</td><td>O</td></tr>
      <tr><td>SERIALIZABLE</td><td>X</td><td>X</td><td>X</td></tr>
    </tbody>
  </table>

  <h3>⚡ 성능 최적화</h3>
  <p><b>쿼리 최적화 체크리스트</b></p>
  <ul>
    <li>[ ] 적절한 인덱스 사용</li>
    <li>[ ] WHERE 절 최적화</li>
    <li>[ ] JOIN 순서 최적화</li>
    <li>[ ] 서브쿼리 → JOIN 변환</li>
    <li>[ ] DISTINCT → GROUP BY</li>
    <li>[ ] UNION → UNION ALL</li>
    <li>[ ] 함수 사용 최소화</li>
  </ul>

  <p><b>시스템 레벨 최적화</b></p>
  <ul>
    <li>메모리 할당 (버퍼 풀, 캐시)</li>
    <li>I/O 최적화 (SSD, RAID)</li>
    <li>네트워크 최적화</li>
    <li>파티셔닝 전략</li>
    <li>병렬 처리 활용</li>
  </ul>

  <h3>🛡️ 데이터 보안</h3>
  <p><b>보안 위협과 대응</b></p>
  <pre><code>SQL 인젝션 → Prepared Statement
권한 상승 → 최소 권한 원칙
내부자 위협 → 감사 로그
데이터 유출 → 암호화
무단 접근 → 접근 제어</code></pre>

  <p><b>암호화 방식</b></p>
  <ul>
    <li>TDE: 파일 레벨 투명 암호화</li>
    <li>컬럼 암호화: 필드별 선택적 암호화</li>
    <li>애플리케이션 암호화: 앱에서 처리</li>
    <li>키 관리: HSM, KMS 활용</li>
  </ul>

  <h3>🌐 분산 데이터베이스</h3>
  <p><b>CAP 정리</b></p>
  <ul>
    <li><b>C</b>onsistency: 일관성</li>
    <li><b>A</b>vailability: 가용성</li>
    <li><b>P</b>artition tolerance: 분할 내성</li>
    <li>세 가지 중 최대 두 가지만 보장 가능</li>
  </ul>

  <p><b>분산 전략</b></p>
  <ul>
    <li>복제(Replication): 가용성, 읽기 성능</li>
    <li>샤딩(Sharding): 쓰기 성능, 확장성</li>
    <li>파티셔닝: 관리성, 성능</li>
    <li>페더레이션: 기능별 분산</li>
  </ul>

  <h3>📈 빅데이터 처리</h3>
  <p><b>OLTP vs OLAP</b></p>
  <table>
    <thead>
      <tr><th>구분</th><th>OLTP</th><th>OLAP</th></tr>
    </thead>
    <tbody>
      <tr><td>목적</td><td>트랜잭션 처리</td><td>분석 처리</td></tr>
      <tr><td>쿼리</td><td>단순, 빠름</td><td>복잡, 집계</td></tr>
      <tr><td>데이터</td><td>현재, 상세</td><td>과거, 요약</td></tr>
      <tr><td>구조</td><td>정규화</td><td>비정규화</td></tr>
      <tr><td>사용자</td><td>운영진</td><td>분석가</td></tr>
    </tbody>
  </table>

  <p><b>빅데이터 아키텍처</b></p>
  <ul>
    <li>배치 처리: Hadoop, Spark</li>
    <li>스트림 처리: Kafka, Flink</li>
    <li>하이브리드: Lambda, Kappa</li>
    <li>레이크하우스: Delta Lake, Iceberg</li>
  </ul>

  <h3>🔧 운영 관리</h3>
  <p><b>백업 전략</b></p>
  <ul>
    <li>전체 백업: 주간/월간</li>
    <li>증분 백업: 일간</li>
    <li>차등 백업: 절충안</li>
    <li>로그 백업: 실시간 복구</li>
  </ul>

  <p><b>모니터링 지표</b></p>
  <ul>
    <li>성능: 응답시간, 처리량</li>
    <li>자원: CPU, 메모리, I/O</li>
    <li>가용성: 업타임, 연결 수</li>
    <li>품질: 오류율, 슬로우 쿼리</li>
  </ul>

  <p><b>고가용성 구성</b></p>
  <ul>
    <li>클러스터링: Active-Active</li>
    <li>복제: Master-Slave</li>
    <li>페일오버: 자동 전환</li>
    <li>로드밸런싱: 부하 분산</li>
  </ul>

  <h3>🚀 최신 기술 동향</h3>
  <p><b>클라우드 네이티브</b></p>
  <ul>
    <li>관리형 서비스: RDS, Aurora</li>
    <li>서버리스: DynamoDB, FaunaDB</li>
    <li>컨테이너: Kubernetes Operator</li>
    <li>멀티클라우드: 벤더 독립성</li>
  </ul>

  <p><b>AI/ML 통합</b></p>
  <ul>
    <li>자동 쿼리 최적화</li>
    <li>이상 탐지 모니터링</li>
    <li>자동 인덱스 추천</li>
    <li>예측적 용량 계획</li>
  </ul>

  <h3>💡 면접 팁</h3>
  <ol>
    <li><b>기본 개념을 정확히</b> 이해하고 실무 예시 연결</li>
    <li><b>성능과 확장성</b> 관점에서 트레이드오프 설명</li>
    <li><b>실제 경험담</b> 포함하여 구체적 답변</li>
    <li><b>최신 기술 동향</b> 관심 표현</li>
    <li><b>문제 해결 과정</b> 체계적으로 설명</li>
    <li><b>비즈니스 관점</b>에서 기술 선택 이유 제시</li>
  </ol>

  <h3>🎯 면접 시나리오별 대응</h3>
  <p><b>성능 문제 해결 과정</b></p>
  <ol>
    <li>모니터링으로 병목 지점 식별</li>
    <li>실행 계획 분석</li>
    <li>인덱스 최적화</li>
    <li>쿼리 튜닝</li>
    <li>하드웨어 리소스 확인</li>
    <li>아키텍처 레벨 개선</li>
  </ol>

  <p><b>데이터베이스 선택 기준</b></p>
  <ul>
    <li>데이터 구조와 관계 복잡도</li>
    <li>트랜잭션 요구사항 (ACID)</li>
    <li>확장성 요구사항</li>
    <li>성능 요구사항</li>
    <li>일관성 vs 가용성 우선순위</li>
    <li>팀의 기술 스택과 경험</li>
  </ul>

  </div>
</details>
