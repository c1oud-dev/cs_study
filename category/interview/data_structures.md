---
layout: default
title: "자료구조 면접 대비 — 완전 정리"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>자료구조 면접 대비 — 기본·심화 Q&A + 개념 설명(상세)</h2>
  <p>구성: ① 기본 면접 Q&A → ② 심화 면접 Q&A → ③ 추가 예상 질문 Q&A → ④ 개념 설명(상세) → 📌 부록: 복잡도 요약 표</p>
</section>

<!-- ① 기본 면접 Q&A -->
<details open>
  <summary><span class="accordion-title">📋 기본 면접 Q&A</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <details>
    <summary style="font-size:1rem;"><b>Q1. 자료구조란 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p><b>A:</b> 자료구조는 컴퓨터에서 데이터를 효율적으로 저장하고 조작할 수 있도록 조직화하는 방법입니다. 데이터의 삽입, 삭제, 검색 등의 연산을 효율적으로 수행하기 위해 데이터들 간의 관계를 정의한 것이라고 할 수 있습니다. 좋은 자료구조를 선택하면 알고리즘의 효율성을 크게 향상시킬 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q2. 배열(Array)의 특징과 시간복잡도를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p><b>A:</b> 배열은 같은 타입의 데이터를 연속된 메모리 공간에 저장하는 선형 자료구조입니다. 인덱스를 통해 직접 접근이 가능하여 검색의 시간복잡도가 O(1)입니다. 하지만 중간에 원소를 삽입하거나 삭제할 때는 다른 원소들을 이동시켜야 하므로 O(n)의 시간이 걸립니다. 크기가 고정되어 있어 메모리를 효율적으로 사용할 수 있지만, 동적으로 크기를 변경하기 어렵다는 단점이 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q3. 연결리스트(Linked List)와 배열의 차이점은 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p><b>A:</b> 연결리스트는 노드들이 포인터로 연결된 동적 자료구조입니다. 배열과 달리 메모리상에서 연속적으로 저장되지 않으며, 각 노드가 데이터와 다음 노드의 주소를 가지고 있습니다. 삽입과 삭제는 O(1)로 배열보다 빠르지만, 특정 위치에 접근하려면 처음부터 순차적으로 탐색해야 하므로 검색은 O(n)입니다. 동적으로 크기를 조절할 수 있어 메모리를 유연하게 사용할 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q4. 스택(Stack)과 큐(Queue)의 차이점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p><b>A:</b> 스택은 LIFO(Last In First Out) 구조로 마지막에 들어간 데이터가 먼저 나오는 자료구조입니다. push와 pop 연산을 통해 데이터를 추가하고 제거하며, 함수 호출이나 재귀 알고리즘에 주로 사용됩니다. 큐는 FIFO(First In First Out) 구조로 먼저 들어간 데이터가 먼저 나오는 자료구조입니다. enqueue와 dequeue 연산을 사용하며, BFS나 작업 스케줄링에 활용됩니다.
</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q5. 해시 테이블(Hash Table)의 동작 원리를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p><b>A:</b> 해시 테이블은 해시 함수를 사용하여 키를 배열의 인덱스로 변환하고, 해당 위치에 값을 저장하는 자료구조입니다. 이상적인 경우 삽입, 삭제, 검색이 모두 O(1)의 시간복잡도를 가집니다. 하지만 서로 다른 키가 같은 해시값을 가지는 충돌이 발생할 수 있어, 체이닝이나 오픈 어드레싱 같은 충돌 해결 방법이 필요합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q6. 이진 트리(Binary Tree)란 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p><b>A:</b> 이진 트리는 각 노드가 최대 2개의 자식 노드를 가질 수 있는 트리 구조입니다. 왼쪽 자식과 오른쪽 자식으로 구분되며, 계층적 데이터를 표현하는 데 적합합니다. 루트 노드부터 시작해서 레벨별로 데이터를 저장하며, 트리 순회 방법으로는 전위, 중위, 후위 순회가 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q7. 이진 탐색 트리(BST)의 특징은 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p><b>A:</b> 이진 탐색 트리는 왼쪽 서브트리의 모든 노드 값이 루트보다 작고, 오른쪽 서브트리의 모든 노드 값이 루트보다 큰 성질을 만족하는 이진 트리입니다. 이 성질 덕분에 검색, 삽입, 삭제 연산을 평균적으로 O(log n)에 수행할 수 있습니다. 하지만 트리가 한쪽으로 치우친 경우 최악의 경우 O(n)이 될 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q8. 힙(Heap)의 종류와 용도를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p><b>A:</b> 힙은 완전 이진 트리의 형태를 가진 자료구조로, 최대 힙과 최소 힙으로 나뉩니다. 최대 힙은 부모 노드가 자식 노드보다 큰 값을 가지며, 최소 힙은 그 반대입니다. 우선순위 큐를 구현하는 데 주로 사용되며, 힙 정렬 알고리즘의 기반이 됩니다. 삽입과 삭제 연산이 O(log n)의 시간복잡도를 가집니다.</p>
    </div>
  </details>

  </div>
</details>

<!-- ② 심화 면접 Q&A -->
<details>
  <summary><span class="accordion-title">🚀 심화 면접 Q&A</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <details>
    <summary style="font-size:1rem;"><b>Q9. AVL 트리와 Red-Black 트리의 차이점은 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p><b>A:</b>AVL 트리는 모든 노드에서 왼쪽과 오른쪽 서브트리의 높이 차이가 최대 1인 자기 균형 이진 탐색 트리입니다. 더 엄격한 균형 조건을 유지하여 검색 성능이 우수하지만, 삽입과 삭제 시 회전 연산이 자주 발생합니다. Red-Black 트리는 각 노드에 색깔 정보를 추가하여 균형을 유지하는 트리로, AVL 트리보다 균형 조건이 완화되어 삽입과 삭제가 더 효율적입니다.
</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q10. B-트리가 데이터베이스에서 사용되는 이유는 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p><b>A:</b> B-트리는 하나의 노드에 여러 개의 키를 저장할 수 있는 다진 트리로, 디스크 I/O를 최소화하는 데 최적화되어 있습니다. 디스크에서 한 번의 읽기로 여러 키를 가져올 수 있어 외부 저장장치의 특성에 적합합니다. 또한 모든 리프 노드가 같은 레벨에 있어 일정한 검색 성능을 보장하며, 삽입과 삭제 시에도 트리의 균형을 자동으로 유지합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q11. 해시 테이블의 충돌 해결 방법들을 비교해주세요.</b></summary>
    <div class="accordion-content">
      <p><b>A:</b> 체이닝은 같은 해시값을 가진 데이터들을 연결리스트로 연결하는 방법입니다. 구현이 간단하고 테이블이 가득 차도 동작하지만, 추가 메모리가 필요하고 캐시 성능이 떨어질 수 있습니다. 오픈 어드레싱은 충돌 발생 시 다른 빈 슬롯을 찾는 방법으로, 선형 탐사, 제곱 탐사, 이중 해싱 등이 있습니다. 메모리 효율성이 좋지만 삭제가 복잡하고 클러스터링 문제가 발생할 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q12. 그래프의 표현 방법인 인접 행렬과 인접 리스트의 장단점은?</b></summary>
    <div class="accordion-content">
      <p><b>A:</b> 인접 행렬은 2차원 배열로 그래프를 표현하는 방법입니다. 두 정점 간의 연결 여부를 O(1)에 확인할 수 있고 구현이 간단하지만, 정점 수의 제곱만큼 메모리를 사용하여 희소 그래프에서는 비효율적입니다. 인접 리스트는 각 정점마다 연결된 정점들의 리스트를 유지하는 방법으로, 간선 수에 비례하는 메모리만 사용하여 효율적이지만, 두 정점의 연결 여부 확인이 O(V)까지 걸릴 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q13. 트라이(Trie) 자료구조의 특징과 용도를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p><b>A:</b> 트라이는 문자열을 저장하고 검색하는 데 특화된 트리 자료구조입니다. 각 노드가 하나의 문자를 나타내며, 루트에서 특정 노드까지의 경로가 하나의 문자열을 구성합니다. 문자열의 길이를 m이라 할 때 삽입, 삭제, 검색이 모두 O(m)에 가능합니다. 자동 완성, 사전 검색, IP 라우팅 등에 활용되며, 공통 접두사를 가진 문자열들을 효율적으로 저장할 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q14. 세그먼트 트리(Segment Tree)란 무엇이며 언제 사용하나요?</b></summary>
    <div class="accordion-content">
      <p><b>A:</b> 세그먼트 트리는 배열의 구간에 대한 쿼리를 효율적으로 처리하기 위한 트리 자료구조입니다. 각 노드가 특정 구간의 정보를 저장하며, 리프 노드는 배열의 개별 원소를 나타냅니다. 구간 합, 최댓값, 최솟값 등의 쿼리를 O(logn)에 처리할 수 있고, 원소 값 변경도 O(log n)에 가능합니다. 대량의 구간 쿼리가 있는 문제에서 효과적으로 사용됩니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q15. Union-Find(Disjoint Set) 자료구조의 동작 원리는?</b></summary>
    <div class="accordion-content">
      <p><b>A:</b> Union-Find는 서로소 집합들을 효율적으로 관리하는 자료구조입니다. 각 집합을 트리로 표현하고, 트리의 루트를 집합의 대표로 사용합니다. Find 연산은 원소가 속한 집합의 대표를 찾고, Union 연산은 두 집합을 하나로 합칩니다. 경로 압축과 랭크에 의한 합치기 최적화를 적용하면 거의 상수 시간에 연산이 가능하며, 크러스칼 알고리즘이나 연결 성분 찾기에 활용됩니다.</p>
    </div>
  </details>

  </div>
</details>

<!-- ③ 추가 예상 질문 Q&A (확장/꼬리질문) -->
<details>
  <summary><span class="accordion-title">💡 추가 예상 질문 Q&A (확장/꼬리질문)</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <details>
    <summary><b>Q16. 동적 배열(Dynamic Array)의 동작 원리를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p><b>A:</b> 동적 배열은 크기를 런타임에 조절할 수 있는 배열입니다. 내부적으로 고정 크기의 배열을 사용하되, 용량이 부족해지면 더 큰 배열을 할당하고 기존 데이터를 복사합니다. 일반적으로 용량이 가득 찰 때마다 2배씩 확장하는 전략을 사용하여, 삽입의 분할상환 시간복잡도를 O(1)로 만듭니다. 메모리 사용량과 복사 비용 사이의 균형을 맞춘 효율적인 자료구조입니다</p>
    </div>
  </details>

  <details>
    <summary><b>Q17. 스킵 리스트(Skip List)란 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p><b>A:</b> 스킵 리스트는 정렬된 연결리스트에 여러 레벨의 "지름길"을 추가한 확률적 자료구조입니다. 각 노드가 여러 레벨의 포인터를 가져서 빠른 검색을 가능하게 합니다. 검색, 삽입, 삭제가 평균적으로 O(log n)의 성능을 보이며, 구현이 이진 탐색 트리보다 간단합니다. Redis 같은 시스템에서 정렬된 집합을 구현하는 데 사용됩니다.</p>
    </div>
  </details>

  <details>
    <summary><b>Q18. 블룸 필터(Bloom Filter)의 원리와 용도는?</b></summary>
    <div class="accordion-content">
      <p><b>A:</b> 블룸 필터는 어떤 원소가 집합에 속하는지를 확률적으로 검사하는 자료구조입니다. 비트 배열과 여러 개의 해시 함수를 사용하여 원소를 저장합니다. 거짓 양성은 있을 수 있지만 거짓 음성은 없어서 "확실히 없다" 또는 "있을 수도 있다"라는 답을 줍니다. 메모리를 매우 효율적으로 사용하여 대용량 데이터에서 중복 검사나 캐시 시스템에 활용됩니다.</p>
    </div>
  </details>

  <details>
    <summary><b>Q19. 캐시 교체 알고리즘들을 비교해주세요.</b></summary>
    <div class="accordion-content">
      <p><b>A:</b> LRU(Least Recently Used)는 가장 오래 사용되지 않은 데이터를 교체하는 방식으로, 연결리스트와 해시맵을 조합해서 O(1)에 구현할 수 있습니다. LFU(Least Frequently Used)는 가장 적게 사용된 데이터를 교체하며, FIFO는 가장 먼저 들어온 데이터를 교체합니다. Random은 무작위로 선택하는 방식으로 구현이 간단합니다. 각각 지역성의 종류에 따라 다른 성능을 보입니다.</p>
    </div>
  </details>

  <details>
    <summary><b>Q20. 문자열 매칭 알고리즘에서 사용되는 자료구조는?</b></summary>
    <div class="accordion-content">
      <p><b>A:</b> KMP 알고리즘에서는 부분 매치 테이블(접두사 함수)을 사용하여 불일치 시 얼마나 이동할지 미리 계산합니다. Rabin-Karp 알고리즘은 롤링 해시를 사용하여 문자열의 해시값을 효율적으로 업데이트합니다. Aho-Corasick 알고리즘은 트라이와 실패 함수를 결합하여 여러 패턴을 동시에 검색합니다. 접미사 배열이나 접미사 트리는 문자열의 모든 접미사 정보를 저장하여 복잡한 문자열 질의를 처리합니다.</p>
    </div>
  </details>

  <details>
    <summary><b>Q21. 메모리 풀(Memory Pool)의 개념과 장점은?</b></summary>
    <div class="accordion-content">
      <p><b>A:</b> 메모리 풀은 미리 큰 메모리 블록을 할당해두고, 필요할 때마다 작은 단위로 나누어 사용하는 메모리 관리 기법입니다. 동적 할당과 해제의 오버헤드를 줄이고, 메모리 단편화를 방지하며, 할당 속도를 향상시킵니다. 특히 같은 크기의 객체를 자주 생성하고 삭제하는 상황에서 효과적이며, 게임 엔진이나 실시간 시스템에서 널리 사용됩니다.</p>
    </div>
  </details>

  <details>
    <summary><b>Q22. 스레드 안전한 자료구조는 어떻게 구현하나요?</b></summary>
    <div class="accordion-content">
      <p><b>A:</b> 스레드 안전성을 위해 뮤텍스나 스핀락 같은 동기화 기법을 사용할 수 있습니다. Lock-free 자료구조는 원자적 연산(atomic operations)을 사용하여 락 없이도 동시성을 보장합니다. Copy-on-Write 방식은 읽기가 많은 상황에서 효과적이며, 세분화된 락킹은 전체 자료구조가 아닌 부분적으로만 락을 거는 방법입니다. 각 방법은 성능과 복잡성 사이의 트레이드오프를 가집니다.</p>
    </div>
  </details>

  <details>
    <summary><b>Q23. 압축 자료구조(Succinct Data Structure)란?</b></summary>
    <div class="accordion-content">
      <p><b>A:</b> 압축 자료구조는 이론적 최소 공간에 가까운 메모리를 사용하면서도 효율적인 연산을 지원하는 자료구조입니다. 예를 들어, 비트 벡터에서 rank와 select 연산을 상수 시간에 지원하면서도 추가 공간을 거의 사용하지 않습니다. Wavelet 트리, FM-인덱스 등이 대표적이며, 대용량 데이터 처리나 생물정보학에서 활용됩니다.</p>
    </div>
  </details>

  <details>
    <summary><b>Q24. 영속적 자료구조(Persistent Data Structure)의 특징은?</b></summary>
    <div class="accordion-content">
      <p><b>A:</b> 영속적 자료구조는 수정 연산 후에도 이전 버전을 그대로 유지하는 자료구조입니다. Path copying, Fat node, Copy-on-Write 등의 기법을 사용하여 구현하며, 함수형 프로그래밍 언어에서 주로 사용됩니다. 버전 관리, 되돌리기 기능, 병렬 처리에서 유용하지만 일반적으로 더 많은 메모리를 사용합니다.</p>
    </div>
  </details>

  <details>
    <summary><b>Q25. 근사 자료구조(Approximate Data Structure)는 언제 사용하나요?</b></summary>
    <div class="accordion-content">
      <p><b>A:</b> 근사 자료구조는 정확한 결과 대신 근사치를 빠르게 제공하는 자료구조입니다. HyperLogLog는 집합의 크기를 근사적으로 계산하고, Count-Min Sketch는 원소의 빈도를 추정합니다. 스트리밍 데이터나 대용량 데이터에서 실시간 분석이 필요할 때 사용하며, 정확성을 일부 포기하는 대신 메모리와 처리 시간을 크게 절약할 수 있습니다.</p>
    </div>
  </details>

  </div>
</details>

<!-- ④ 개념 설명(상세) -->
<details>
  <summary><span class="accordion-title">📚 개념 설명(상세)</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <h3>1) 시간·공간 복잡도와 분할 상환</h3>
  <p>빅오 표기는 상한을 나타냅니다. 평균/최악/상환을 구분하는 습관이 중요합니다. 상환 분석은 희소한 비싼 연산(동적 확장/재해싱)을 평균화해 평균 <code>O(1)</code>을 정당화합니다.</p>

  <h3>2) 배열 &amp; 동적 배열</h3>
  <ul>
    <li><b>장점:</b> 연속 메모리로 캐시 친화적, 인덱스 접근 <code>O(1)</code></li>
    <li><b>단점:</b> 중간 삽입/삭제 <code>O(n)</code>, 크기 고정</li>
    <li><b>동적 배열:</b> 용량이 찰 때 배수 확장으로 평균 <code>O(1)</code> 삽입. 축소 정책도 고려</li>
  </ul>

  <h3>3) 연결 리스트(단일/이중/원형)</h3>
  <ul>
    <li><b>장점:</b> 중간 삽입/삭제 <code>O(1)</code>, 메모리 재배치 불필요</li>
    <li><b>단점:</b> 임의 접근 불가, 포인터 오버헤드, 캐시 비우호적</li>
    <li><b>응용:</b> LRU, 빈번한 중간 수정, 거대한 객체 이동 회피</li>
  </ul>

  <h3>4) 스택/큐/데크</h3>
  <p>스택(호출 스택, DFS, 수식 평가) / 큐(BFS, 버퍼, 생산자-소비자) / 데크(양끝 <code>O(1)</code> — 슬라이딩 윈도우, 모노톤 큐)</p>

  <h3>5) 해시 테이블</h3>
  <ul>
    <li><b>핵심 파라미터:</b> 해시 함수 품질, 부하율(<code>α</code>), 리사이즈 정책</li>
    <li><b>충돌 회피:</b> 체이닝, 개방 주소법(선형/이차/이중), Robin Hood/Cuckoo</li>
    <li><b>실무 팁:</b> 키 평활화, 난독화 해시로 공격적 충돌 방어, 버킷 트리화(JDK 8+)</li>
  </ul>

  <h3>6) 트리 &amp; 순회</h3>
  <p>트리 높이는 성능의 핵심. 전위(복원/직렬화), 중위(BST 정렬), 후위(삭제/평가), 레벨(BFS).</p>

  <h3>7) BST와 균형 트리(AVL/Red-Black)</h3>
  <p>BST는 편향 방지 필요. AVL: 탐색 유리 / Red-Black: 업데이트 유리(산업 표준).</p>

  <h3>8) 힙 &amp; 우선순위 큐</h3>
  <p>배열 구현으로 부모/자식 인덱스 계산이 간단. 응용: 일정 관리, QoS, 스트림 Top-K.</p>

  <h3>9) B-Tree/B+Tree</h3>
  <p>외부 메모리 친화: 큰 팬아웃으로 I/O 감소. B+Tree: 리프 체인으로 범위 스캔 최적.</p>

  <h3>10) Trie &amp; 변형</h3>
  <p>Radix/Patricia로 경로 압축, TST로 메모리 절약. Aho–Corasick: 다중 패턴 매칭 선형 시간.</p>

  <h3>11) 그래프 표현 &amp; 탐색</h3>
  <p>인접 리스트 vs 인접 행렬. BFS(최단거리, 레벨)/DFS(사이클, 위상, 연결성).</p>

  <h3>12) 세그먼트 트리 &amp; 펜윅 트리</h3>
  <p>세그먼트: 다양한 모노이드/지연 전파. 펜윅: 합/누적 빈도 특화(간단/저메모리).</p>

  <h3>13) Union-Find(DSU)</h3>
  <p>경로 압축 + 랭크/사이즈로 거의 상수. 응용: 동적 연결성, MST, 군집화.</p>

  <h3>14) Skip List</h3>
  <p>확률적 균형 — 단순 구현 + 정렬 리스트와 로그 탐색 결합. 병행성 구현에 우호적.</p>

  <h3>15) 문자열 자료구조</h3>
  <p>접미 배열/트리 + LCP: 부분 문자열/반복 패턴/사전 질의. Rope/Gap Buffer: 대용량 편집 최적.</p>

  <h3>16) 캐시 정책</h3>
  <p>LRU/LFU/ARC/TinyLFU — 액세스 패턴에 맞춘 하이브리드가 효과적. 구현: LRU(해시+이중리스트), LFU(해시+빈도버킷).</p>

  <h3>17) 불변/영속(Persistent) 구조</h3>
  <p>구조 공유로 스냅샷/버전 관리, 동시성 안전. 단점: 쓰기 시 메모리/GC 오버헤드.</p>

  <h3>18) 일관성·캐시 지역성·실무 선택</h3>
  <p>CPU 캐시/분기 예측을 고려하면 배열 기반이 대체로 우세. 데이터 패턴/업데이트 빈도/병행성 요구를 함께 평가해야 최적 선택.</p>

  </div>
</details>

<!-- 📌 부록: 복잡도 요약 표 -->
<details>
  <summary><span class="accordion-title">📌 부록: 복잡도 요약 표</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">
    <table>
      <thead>
        <tr>
          <th>구조</th><th>조회</th><th>삽입</th><th>삭제</th><th>비고</th>
        </tr>
      </thead>
      <tbody>
        <tr><td>배열</td><td>O(1)</td><td>O(n)</td><td>O(n)</td><td>끝 삽입은 상환 O(1)</td></tr>
        <tr><td>연결 리스트</td><td>O(n)</td><td>O(1)*</td><td>O(1)*</td><td>*노드 참조 있으면</td></tr>
        <tr><td>해시 테이블</td><td>O(1) avg</td><td>O(1) avg</td><td>O(1) avg</td><td>충돌/리사이즈 고려</td></tr>
        <tr><td>BST(균형)</td><td>O(log n)</td><td>O(log n)</td><td>O(log n)</td><td>편향 시 O(n)</td></tr>
        <tr><td>힙</td><td>O(1) extremum</td><td>O(log n)</td><td>O(log n)</td><td>우선순위 큐</td></tr>
        <tr><td>Trie</td><td>O(m)</td><td>O(m)</td><td>O(m)</td><td>m=문자열 길이</td></tr>
        <tr><td>세그먼트 트리</td><td>O(log n)</td><td>O(log n)</td><td>O(log n)</td><td>Lazy로 대량 업데이트</td></tr>
        <tr><td>펜윅 트리</td><td>O(log n)</td><td>O(log n)</td><td>O(log n)</td><td>합/빈도 특화</td></tr>
        <tr><td>스킵 리스트</td><td>O(log n) avg</td><td>O(log n) avg</td><td>O(log n) avg</td><td>확률적</td></tr>
      </tbody>
    </table>
  </div>
</details>
