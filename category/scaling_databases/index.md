---
layout: default
title: "Scaling Databases"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>Scaling Databases</h2>
  <p>
    Scaling Databases(데이터베이스 확장)는 더 많은 데이터와 사용자를 효율적으로 처리하도록 데이터베이스를 조정하는 과정이다. 기존 하드웨어를 업그레이드(수직 확장)하거나 서버를 추가(수평 확장)하여 확장할 수 있다. 샤딩 및 복제와 같은 기술이 핵심이다. 이를 통해 데이터베이스가 성장함에 따라 지속적으로 강력한 자산으로 기능할 수 있다.
  </p>
  <p><strong>정리: Scaling Databases는 DB의 처리량과 성능을 향상시키기 위해 수직 확장(성능 업그레이드) 또는 수평 확장(서버 분산)을 적용하는 과정이다.</strong></p>
</section>

<details open>
<summary><span class="accordion-title">Database Indexes</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  데이터베이스 인덱스는 DBMS에서 데이터 검색 작업 속도를 향상시키는 데이터 구조이다. *장부 인덱스와 유사하게 작동하여 특정 열 또는 열 집합을 기반으로 정보를 빠르게 찾을 수 있도록 한다. 인덱스는 실제 데이터에 대한 참조를 보유하는 별도의 구조를 생성하여 DB 엔진이 전체 테이블을 스캔하지 않고도 정보를 찾을 수 있도록 한다. 인덱스는 특히 대규모 데이터 세트의 쿼리 성능을 크게 향상시키지만, 단점도 있다. 데이터가 수정될 때마다 인덱스를 업데이트해야 하므로 저장 공간 요구 사항이 증가하고 쓰기 작업 속도가 느려질 수 있다. 일반적인 유형으로는 *범용 B-트리 인덱스, 카디널리티가 낮은 데이터를 위한 *비트맵 인덱스, 동등 비교를 위한 *해시 인덱스가 있다. 적절한 인덱스 설계는 DB 성능을 최적화하고, 빠른 읽기 속도와 느린 쓰기 속도, 그리고 증가하는 저장 공간 요구 사항 간의 균형을 맞추는 데 매우 중요하다.
  </p>
  <p><strong>정리: 데이터베이스 인덱스는 검색 속도를 높이기 위해 데이터의 위치 정보를 미리 저장한 자료 구조다.</strong></p>

  <ul>
    <li><strong>장부 인덱스(Ledger Index):</strong> 장부처럼 순차적으로 키와 위치를 기록하는 단순 인덱스 구조로, 작은 데이터셋이나 로그성 데이터에 적합.</li>
    <li><strong>범용 B-트리 인덱스(General B-Tree Index):</strong> 균형 트리 구조로 키 값을 정렬해 저장하며, 범위 검색·정렬·부분 검색에 효율적.</li>
    <li><strong>비트맵 인덱스(Bitmap Index):</strong> 각 키 값에 대해 비트 벡터를 사용해 저장하는 방식으로, 값 종류가 적고 데이터가 반복되는 경우(예: 성별, 상태)에 효율적.</li>
    <li><strong>해시 인덱스(Hash Index):</strong> 해시 함수를 이용해 키를 해시 값으로 변환하고 위치를 찾는 방식으로, 정확한 값 검색(=)에 매우 빠름.</li>
  </ul>

</div>
</details>


<details>
<summary>Data Replication <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  Data Replication(데이터 복제)는 분산 시스템의 여러 위치 또는 노드에 동일한 데이터의 여러 복사본을 생성하고 유지하는 프로세스이다. 하나 이상의 노드에 장애가 발생하더라도 데이터에 계속 액세스할 수 있도록 보장하여 데이터 가용성, 안정성 및 성능을 향상시킨다. 복제는 동기식(변경 사항이 모든 복사본에 동시에 적용됨) 또는 비동기식(변경 사항이 주 복사본에 적용된 후 전파됨)으로 수행될 수 있다. 데이터베이스 시스템, 콘텐츠 전송 네트워크(CDN), 분산 파일 시스템에서 널리 사용된다. 복제 전략에는 마스터-슬레이브, 멀티 마스터, 피어 투 피어 모델이 있다. 복제는 내결함성과 읽기 성능을 향상시키지만, 복사본 간 데이터 일관성을 유지하고 잠재적 충돌을 관리하는 데 어려움을 초래한다. 효과적인 복제 전략은 일관성, 가용성, 그리고 파티션 허용 간의 균형을 맞춰야 하며, 이는 종종 CAP 정리의 원칙에 부합해야 한다.
  </p>
  <p><strong>정리: 데이터 복제(Data Replication)는 동일한 데이터를 여러 노드에 복사·동기화해 가용성과 내결함성을 높이는 기술이다.</strong></p>

  <ul>
    <li><strong>노드(Node):</strong> 네트워크나 분산 시스템에서 데이터를 저장·처리하는 개별 서버 또는 인스턴스.</li>
    <li><strong>동기식(Synchronous):</strong> 데이터 변경 시 모든 복제본에 즉시 반영 후 응답하는 방식으로, 일관성이 높지만 지연이 커질 수 있음.</li>
    <li><strong>비동기식(Asynchronous):</strong> 변경 사항을 우선 한 곳에 기록하고 나중에 다른 복제본에 전파하는 방식으로, 속도는 빠르지만 최신성 보장이 떨어질 수 있음.</li>
    <li><strong>CDN(Content Delivery Network):</strong> 전 세계 여러 위치에 콘텐츠 복제본을 저장해, 사용자에게 가장 가까운 서버에서 빠르게 제공하는 네트워크.</li>
    <li><strong>분산 파일 시스템(Distributed File System):</strong> 데이터를 여러 서버에 나누어 저장하고, 하나의 파일 시스템처럼 접근할 수 있도록 하는 기술(HDFS 등).</li>
    <li><strong>마스터-슬레이브(Master-Slave):</strong> 한 노드가 쓰기 작업을 담당하고 다른 노드들이 읽기 전용 복제본으로 동작하는 구조.</li>
    <li><strong>멀티 마스터(Multi-Master):</strong> 여러 노드가 동시에 읽기와 쓰기 작업을 수행하며, 서로 데이터 변경 사항을 동기화하는 구조.</li>
    <li><strong>피어 투 피어 모델(Peer-to-Peer):</strong> 모든 노드가 동등한 권한을 가지고 서로 데이터를 직접 교환·복제하는 구조.</li>
    <li><strong>내결함성(Fault Tolerance):</strong> 일부 노드나 네트워크에 장애가 발생해도 시스템이 정상적으로 동작을 유지하는 능력.</li>
  </ul>

</div>
</details>


<details>
<summary>Sharding strategies <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  Sharding strategies(샤딩 전략)은 대규모 데이터 세트를 작은 *청크(logical shard)로 분할하는 기술로, 트래픽 부하를 분산하기 위해 이러한 청크를 여러 머신/DB 노드에 분산한다. 애플리케이션의 확장성을 향상시키는 효과적인 방법이다. 많은 DB가 *샤딩을 지원하지만, 모든 DB가 지원하는 것은 아니다.
  </p>
  <p><strong>정리: Sharding 전략은 데이터를 여러 샤드로 분할해 분산 저장·처리하여 성능과 확장성을 높이는 방법이다.</strong></p>

  <ul>
    <li><strong>청크(Logical Shard):</strong> 샤딩된 데이터의 논리적 단위로, 실제 물리적 서버나 파티션에 매핑되기 전 단계의 데이터 블록을 의미하며 이동·재분배가 가능하다.</li>
    <li><strong>샤딩(Sharding):</strong> 대용량 DB를 여러 개의 작은 단위(샤드)로 나누어 서로 다른 서버나 노드에 분산 저장하는 기술</li>
  </ul>

</div>
</details>


<details>
<summary>CAP Theorem <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  CAP 정리(Brewer's Theorem)는 분산 데이터베이스 시스템의 기본 원리이다. 이 정리는 분산 시스템에서 다음 세 가지 속성을 동시에 보장하는 것은 불가능하다고 말한다. 일관성(모든 노드가 동시에 동일한 데이터를 볼 수 있음), 가용성(모든 요청이 응답을 받지만 최신 버전의 데이터가 포함되어 있다는 보장은 없음), 분할 허용성(노드 간 네트워크 장애 발생 시에도 시스템이 계속 작동함). 이 정리에 따르면 분산 시스템은 주어진 시간에 이 세 가지 보장 중 두 가지만 강력하게 제공할 수 있다. 이 원리는 분산 시스템의 설계 및 아키텍처를 안내하며 데이터 일관성 모델, 복제 전략 및 장애 처리에 대한 의사 결정에 영향을 미친다. CAP 정리를 이해하는 것은 견고하고 확장 가능한 분산 시스템을 설계하고 분산 컴퓨팅 환경의 특정 사용 사례에 적합한 데이터베이스 솔루션을 선택하는 데 매우 중요하다.
  </p>
  <p><strong>정리: CAP 정리는 분산 시스템에서 일관성·가용성·네트워크 분할 허용성 중 동시에 두 가지만 만족할 수 있다는 이론이다.</strong></p>
  
</div>
</details>
