---
layout: default
title: "자료구조 면접 대비"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>자료구조 면접 대비</h2>
  <p>📋 기본 면접 Q&A(16문항) → 💡 추가 예상 질문 Q&A(19문항) → 📌 부록: 복잡도 요약 표</p>
</section>

<!-- ① 기본 면접 Q&A -->
<details open>
  <summary><span class="accordion-title">📋 기본 면접 Q&A</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <details>
    <summary style="font-size:1rem;"><b>Q1. 자료구조란 무엇이며 왜 중요한가요?</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
    <div class="accordion-content">
      <p><b>자료구조란 데이터를 효율적으로 저장하고 관리하기 위한 체계적인 방법</b>입니다.</p>
      <p>자료구조가 중요한 이유는 크게 두 가지입니다. 첫째, <b>프로그램의 성능에 직접적인 영향</b>을 미칩니다. 같은 문제라도 어떤 자료구조를 선택하느냐에 따라 시간 복잡도와 공간 복잡도가 크게 달라집니다. 예를 들어, 데이터 검색이 빈번한 경우 배열보다 해시 테이블을 사용하면 검색 속도를 획기적으로 줄일 수 있습니다.</p>
      <p>둘째, <b>문제 해결 방식 자체를 결정</b>합니다. 계층적인 데이터를 다룰 때는 트리 구조가 적합하고, 작업의 순서를 관리할 때는 큐나 스택이 효과적입니다. 이처럼 상황에 맞는 자료구조를 선택하는 것이 효율적인 알고리즘 설계의 출발점이 됩니다.</p>
      <p>결국 자료구조에 대한 이해는 <b>단순히 동작하는 코드가 아니라, 효율적으로 동작하는 코드</b>를 작성하기 위한 기반이라고 할 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q2. 배열(Array)과 연결 리스트(Linked List)의 차이점을 설명해주세요.</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
    <div class="accordion-content">
      <p><b>배열과 연결 리스트의 가장 큰 차이점은 메모리 저장 방식</b>입니다. 배열은 연속된 메모리 공간에 데이터를 저장하고, 연결 리스트는 각 노드가 다음 노드의 주소를 가리키며 흩어져 저장됩니다.</p>
      <p>이 구조적 차이로 인해 <b>성능 특성이 완전히 달라집니다</b>. 배열은 인덱스를 통해 원하는 위치에 바로 접근할 수 있어서 조회가 O(1)로 매우 빠릅니다. 반면 연결 리스트는 처음부터 순차적으로 탐색해야 하므로 조회에 O(n)이 걸립니다.</p>
      <p>하지만 <b>삽입과 삭제에서는 반대</b>입니다. 배열은 중간에 요소를 삽입하거나 삭제할 때 나머지 요소들을 전부 밀거나 당겨야 해서 O(n)이 소요됩니다. 연결 리스트는 해당 위치만 찾으면 포인터만 변경하면 되기 때문에 삽입과 삭제 자체는 O(1)입니다.</p>
      <p>따라서 <b>조회가 빈번한 경우에는 배열</b>이, <b>삽입과 삭제가 빈번한 경우에는 연결 리스트</b>가 더 적합합니다. 실제 개발에서는 이러한 특성을 고려해서 상황에 맞는 자료구조를 선택하는 것이 중요합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q3. ArrayList와 LinkedList의 차이점과 각각 언제 사용하는 것이 좋은가요?</b><span style="float:right;">🟩🟩🟩🟩🟩</span></summary>
    <div class="accordion-content">
      <p><b>ArrayList와 LinkedList는 둘 다 List 인터페이스의 구현체이지만, 내부 구조가 다릅니다</b>. ArrayList는 내부적으로 배열을 사용하고, LinkedList는 이중 연결 리스트로 구현되어 있습니다.</p>
      <p>이 구조 차이로 인해 <b>성능 특성이 다릅니다</b>. ArrayList는 인덱스를 통한 조회가 O(1)로 빠르지만, 중간에 삽입이나 삭제가 발생하면 요소들을 이동시켜야 해서 O(n)이 걸립니다. 또한 배열이 가득 차면 더 큰 배열을 새로 만들어 복사하는 과정이 필요합니다.</p>
      <p>반면 LinkedList는 조회 시 처음부터 순차 탐색해야 해서 O(n)이 걸리지만, <b>삽입과 삭제는 노드의 참조만 변경</b>하면 되기 때문에 해당 위치에서의 작업 자체는 O(1)입니다.</p>
      <p>따라서 <b>데이터 조회가 빈번하고 크기 변화가 적은 경우에는 ArrayList</b>가 적합하고, <b>삽입과 삭제가 빈번한 경우에는 LinkedList</b>가 유리합니다. 다만 실무에서는 대부분의 경우 ArrayList가 캐시 효율성 측면에서 더 좋은 성능을 보여서, 특별한 이유가 없다면 ArrayList를 기본으로 사용하는 경우가 많습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q4. 스택(Stack)과 큐(Queue)의 특징과 차이점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p><b>스택과 큐의 가장 큰 차이는 데이터를 꺼내는 순서</b>입니다. 스택은 후입선출, 즉 나중에 들어온 데이터가 먼저 나가고, 큐는 선입선출, 즉 먼저 들어온 데이터가 먼저 나갑니다.</p>
      <p><b>스택은 LIFO 구조</b>로, 접시를 쌓는 것처럼 가장 위에 있는 데이터만 접근할 수 있습니다. 대표적인 활용 사례로는 함수 호출 시 사용되는 콜 스택, 브라우저의 뒤로가기 기능, 그리고 실행 취소 기능이 있습니다.</p>
      <p><b>큐는 FIFO 구조</b>로, 줄을 서는 것처럼 먼저 들어온 순서대로 처리됩니다. 대표적인 활용 사례로는 프린터의 인쇄 대기열, 작업 스케줄링, 그래프의 너비 우선 탐색인 BFS가 있습니다.</p>
      <p>두 자료구조 모두 <b>삽입과 삭제가 O(1)로 빠르다</b>는 공통점이 있습니다. 차이점은 결국 문제의 특성에 따라 선택하면 되는데, 가장 최근 데이터를 우선 처리해야 하면 스택을, 순서대로 처리해야 하면 큐를 사용하면 됩니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q5. 스택과 큐는 각각 어떤 상황에서 사용되나요?</b></summary>
    <div class="accordion-content">
      <p><b>스택은 가장 최근 작업을 우선 처리해야 할 때</b>, <b>큐는 들어온 순서대로 처리해야 할 때</b> 사용됩니다.</p>
      <p>스택의 대표적인 활용 상황으로는 먼저 <b>함수 호출 관리</b>가 있습니다. 프로그램이 함수를 호출하면 콜 스택에 쌓이고, 가장 마지막에 호출된 함수부터 실행이 완료되어 빠져나갑니다. 또한 <b>브라우저의 뒤로가기</b>도 스택으로 구현되는데, 방문한 페이지를 스택에 쌓아두고 뒤로가기를 누르면 가장 최근 페이지부터 꺼내는 방식입니다. 그 외에도 실행 취소 기능, 괄호 짝 검사, 깊이 우선 탐색인 DFS에 활용됩니다.</p>
      <p>큐의 대표적인 활용 상황으로는 <b>작업 스케줄링</b>이 있습니다. 프린터 대기열처럼 먼저 요청한 작업을 먼저 처리해야 할 때 사용됩니다. 또한 <b>메시지 큐</b>도 대표적인 예인데, 서버 간 비동기 통신에서 메시지를 순서대로 처리할 때 활용됩니다. 그 외에도 너비 우선 탐색인 BFS, 캐시 구현, 버퍼 관리 등에 사용됩니다.</p>
      <p>결국 <b>역순 처리가 필요하면 스택</b>, <b>순차 처리가 필요하면 큐</b>를 선택하면 됩니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q6. 해시 테이블(Hash Table)이란 무엇이며 동작 원리를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p><b>해시 테이블은 키와 값의 쌍으로 데이터를 저장하며, 평균 O(1)의 시간 복잡도로 빠른 검색이 가능한 자료구조</b>입니다.</p>
      <p>동작 원리는 다음과 같습니다. 먼저 <b>해시 함수</b>를 통해 키를 특정 숫자로 변환합니다. 이 숫자를 배열의 인덱스로 사용해서 해당 위치에 값을 저장합니다. 조회할 때도 같은 해시 함수를 적용하면 바로 해당 인덱스로 접근할 수 있어서 검색 속도가 매우 빠릅니다.</p>
      <p>하지만 서로 다른 키가 같은 인덱스로 변환되는 <b>해시 충돌</b>이 발생할 수 있습니다. 이를 해결하는 대표적인 방법으로는 두 가지가 있습니다. 첫째는 <b>체이닝</b>으로, 같은 인덱스에 연결 리스트로 여러 데이터를 저장하는 방식입니다. 둘째는 <b>개방 주소법</b>으로, 충돌 시 다른 빈 공간을 찾아 저장하는 방식입니다.</p>
      <p>자바에서는 HashMap이 해시 테이블을 구현한 대표적인 예이며, 캐시 구현, 데이터베이스 인덱싱, 중복 검사 등 <b>빠른 검색이 필요한 다양한 상황</b>에서 활용됩니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q7. 해시 충돌(Hash Collision)이란 무엇이며 해결 방법은 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p><b>해시 충돌이란 서로 다른 키가 해시 함수를 통해 동일한 인덱스로 변환되는 현상</b>입니다. 해시 테이블의 크기는 한정되어 있기 때문에 충돌은 필연적으로 발생하며, 이를 효과적으로 처리하는 것이 중요합니다.</p>
      <p>대표적인 해결 방법으로는 <b>체이닝</b>과 <b>개방 주소법</b>이 있습니다.</p>
      <p>체이닝은 같은 인덱스에 충돌이 발생하면 <b>해당 위치에 연결 리스트로 데이터를 연결</b>해서 저장하는 방식입니다. 구현이 간단하고 삭제가 용이하다는 장점이 있지만, 충돌이 많아지면 연결 리스트가 길어져서 검색 성능이 저하될 수 있습니다. 자바의 HashMap이 이 방식을 사용하며, 자바 8부터는 연결 리스트가 일정 개수를 초과하면 트리 구조로 변환해서 성능을 개선합니다.</p>
      <p>개방 주소법은 충돌이 발생하면 <b>다른 빈 공간을 찾아 저장</b>하는 방식입니다. 대표적으로 다음 인덱스를 순차적으로 탐색하는 선형 탐사, 제곱 간격으로 탐색하는 이차 탐사, 그리고 별도의 해시 함수를 사용하는 이중 해싱이 있습니다.</p>
      <p>실무에서는 <b>좋은 해시 함수를 설계</b>해서 충돌 자체를 최소화하는 것이 가장 중요합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q8. 트리(Tree) 자료구조의 기본 개념과 용어들을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p><b>트리는 계층적인 관계를 표현하는 비선형 자료구조</b>입니다. 하나의 루트 노드에서 시작해서 여러 자식 노드로 뻗어나가는 구조이며, 사이클이 없다는 특징이 있습니다.</p>
      <p>트리의 주요 용어들을 설명드리면, 먼저 <b>노드</b>는 데이터를 저장하는 기본 단위입니다. <b>루트 노드</b>는 트리의 최상위에 있는 노드이고, <b>리프 노드</b>는 자식이 없는 가장 말단의 노드입니다. 노드 간의 관계에서 상위 노드를 <b>부모 노드</b>, 하위 노드를 <b>자식 노드</b>, 같은 부모를 가진 노드들을 <b>형제 노드</b>라고 합니다.</p>
      <p>또한 <b>간선</b>은 노드와 노드를 연결하는 선이고, <b>깊이</b>는 루트에서 특정 노드까지의 거리를 의미합니다. <b>높이</b>는 루트에서 가장 깊은 리프 노드까지의 거리이며, <b>차수</b>는 한 노드가 가진 자식 노드의 개수입니다.</p>
      <p>트리 구조는 <b>파일 시스템의 디렉토리 구조, HTML의 DOM 구조, 데이터베이스 인덱스</b> 등 계층적인 데이터를 표현하고 관리해야 하는 다양한 상황에서 활용됩니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q9. 이진 트리(Binary Tree)와 이진 탐색 트리(Binary Search Tree)의 차이점은?</b></summary>
    <div class="accordion-content">
      <p><b>이진 트리와 이진 탐색 트리의 가장 큰 차이점은 데이터 정렬 규칙의 유무</b>입니다. 이진 탐색 트리는 이진 트리에 특별한 정렬 규칙이 추가된 형태입니다.</p>
      <p><b>이진 트리</b>는 각 노드가 최대 두 개의 자식 노드를 가질 수 있는 트리 구조입니다. 이것은 순수하게 구조적인 정의이며, 데이터가 어떤 순서로 저장되는지에 대한 규칙은 없습니다.</p>
      <p>반면 <b>이진 탐색 트리</b>는 여기에 정렬 규칙이 추가됩니다. 모든 노드에서 <b>왼쪽 서브트리에는 부모보다 작은 값</b>이, <b>오른쪽 서브트리에는 부모보다 큰 값</b>이 위치해야 합니다. 이 규칙 덕분에 탐색 시 한 번 비교할 때마다 탐색 범위가 절반으로 줄어들어 평균 O(log n)의 시간 복잡도로 검색이 가능합니다.</p>
      <p>다만 이진 탐색 트리는 데이터가 한쪽으로 치우쳐 삽입되면 최악의 경우 O(n)까지 성능이 저하될 수 있습니다. 이를 보완하기 위해 <b>AVL 트리나 레드-블랙 트리</b> 같은 균형 이진 탐색 트리가 사용됩니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q10. 이진 탐색 트리(BST)의 시간 복잡도와 최악의 경우는?</b></summary>
    <div class="accordion-content">
      <p><b>이진 탐색 트리의 평균 시간 복잡도는 O(log n)이지만, 최악의 경우 O(n)까지 저하될 수 있습니다</b>.</p>
      <p>평균적인 경우, 트리가 균형 잡혀 있다면 한 번 비교할 때마다 탐색 범위가 절반으로 줄어듭니다. 따라서 <b>검색, 삽입, 삭제 모두 O(log n)</b>의 시간 복잡도를 가집니다. 이것이 이진 탐색 트리의 핵심 장점입니다.</p>
      <p>하지만 <b>최악의 경우는 트리가 한쪽으로 치우쳐진 편향 트리</b>가 될 때 발생합니다. 예를 들어, 이미 정렬된 데이터를 순차적으로 삽입하면 모든 노드가 한쪽 방향으로만 연결되어 사실상 연결 리스트와 같은 형태가 됩니다. 이 경우 검색, 삽입, 삭제 모두 O(n)이 됩니다.</p>
      <p>이 문제를 해결하기 위해 <b>자가 균형 이진 탐색 트리</b>가 사용됩니다. 대표적으로 AVL 트리는 삽입과 삭제 시 회전 연산을 통해 균형을 유지하고, 레드-블랙 트리는 색상 규칙을 통해 균형을 보장합니다. 자바의 TreeMap이나 HashMap 내부에서 레드-블랙 트리가 활용됩니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q11. 힙(Heap) 자료구조란 무엇이며 종류는 어떤 것이 있나요?</b></summary>
    <div class="accordion-content">
      <p><b>힙은 완전 이진 트리 기반의 자료구조로, 부모 노드와 자식 노드 간에 특정 대소 관계가 항상 성립하는 특징</b>을 가집니다.</p>
      <p>힙의 종류는 크게 두 가지가 있습니다. <b>최대 힙</b>은 부모 노드가 항상 자식 노드보다 크거나 같아서, 루트에 가장 큰 값이 위치합니다. 반대로 <b>최소 힙</b>은 부모 노드가 항상 자식 노드보다 작거나 같아서, 루트에 가장 작은 값이 위치합니다.</p>
      <p>힙의 핵심 장점은 <b>최댓값이나 최솟값을 O(1)로 즉시 조회</b>할 수 있다는 것입니다. 삽입과 삭제 연산은 트리의 균형을 유지하기 위해 재정렬이 필요하므로 O(log n)이 소요됩니다.</p>
      <p>힙은 다양한 곳에서 활용됩니다. 가장 대표적인 것이 <b>우선순위 큐</b>의 구현이며, 자바에서는 PriorityQueue가 내부적으로 힙을 사용합니다. 그 외에도 힙 정렬, 다익스트라 알고리즘에서 최단 경로 탐색, 그리고 운영체제의 작업 스케줄링 등에 활용됩니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q12. 우선순위 큐(Priority Queue)란 무엇이며 어떻게 구현하나요?</b></summary>
    <div class="accordion-content">
      <p><b>우선순위 큐는 들어온 순서가 아닌 우선순위가 높은 데이터가 먼저 나가는 자료구조</b>입니다. 일반 큐가 선입선출이라면, 우선순위 큐는 우선순위 기준으로 정렬되어 처리됩니다.</p>
      <p>우선순위 큐를 구현하는 방법은 여러 가지가 있습니다. 배열이나 연결 리스트로 구현할 수도 있지만, <b>가장 효율적인 방법은 힙</b>을 사용하는 것입니다. 배열로 구현하면 삽입은 O(1)이지만 삭제 시 최댓값 또는 최솟값을 찾는 데 O(n)이 걸립니다. 반면 힙으로 구현하면 <b>삽입과 삭제 모두 O(log n)</b>이고, <b>최우선 데이터 조회는 O(1)</b>로 매우 효율적입니다.</p>
      <p>자바에서는 <b>PriorityQueue</b> 클래스가 제공되며, 기본적으로 최소 힙으로 동작합니다. 최대 힙이 필요한 경우에는 Comparator를 통해 정렬 기준을 변경할 수 있습니다.</p>
      <p>우선순위 큐는 <b>다익스트라 알고리즘</b>에서 최단 거리 노드를 선택할 때, 운영체제의 프로세스 스케줄링, 그리고 네트워크 트래픽 관리 등 우선순위 기반 처리가 필요한 다양한 상황에서 활용됩니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q13. 그래프(Graph)란 무엇이며 트리와의 차이점은?</b></summary>
    <div class="accordion-content">
      <p><b>그래프는 정점과 간선으로 이루어진 자료구조로, 객체 간의 관계를 표현</b>합니다. 트리도 그래프의 일종이지만, 몇 가지 중요한 차이점이 있습니다.</p>
      <p>첫째, <b>사이클의 유무</b>입니다. 트리는 사이클이 없는 구조이지만, 그래프는 사이클이 존재할 수 있습니다. 둘째, <b>루트 노드의 유무</b>입니다. 트리는 반드시 하나의 루트 노드가 있고 계층 구조를 가지지만, 그래프는 루트 개념이 없고 모든 정점이 동등합니다. 셋째, <b>부모-자식 관계</b>입니다. 트리는 부모와 자식 간의 방향성이 명확하지만, 그래프는 이러한 관계가 없습니다.</p>
      <p>그래프는 간선의 방향 유무에 따라 <b>방향 그래프와 무방향 그래프</b>로 나뉘고, 간선에 가중치가 있는지에 따라 <b>가중치 그래프</b>로 구분됩니다.</p>
      <p>그래프는 <b>소셜 네트워크의 친구 관계, 지도에서의 경로 탐색, 네트워크 라우팅</b> 등 복잡한 연결 관계를 표현해야 하는 상황에서 활용됩니다. 정리하면, 트리는 계층 구조에 적합하고, 그래프는 자유로운 연결 관계를 표현하는 데 적합합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q14. 그래프의 표현 방법인 인접 행렬과 인접 리스트를 비교해주세요.</b></summary>
    <div class="accordion-content">
      <p><b>인접 행렬과 인접 리스트는 그래프를 표현하는 두 가지 대표적인 방법이며, 메모리 사용량과 연산 효율에서 차이</b>가 있습니다.</p>
      <p><b>인접 행렬</b>은 정점 수를 V라고 할 때 V곱하기V 크기의 이차원 배열로 표현합니다. 두 정점이 연결되어 있으면 1, 아니면 0으로 표시합니다. 장점은 두 정점 간 연결 여부를 O(1)로 바로 확인할 수 있다는 것입니다. 단점은 공간 복잡도가 O(V²)로, 정점은 많지만 간선이 적은 희소 그래프에서는 메모리 낭비가 심합니다.</p>
      <p><b>인접 리스트</b>는 각 정점마다 연결된 정점들을 리스트로 저장합니다. 공간 복잡도가 O(V+E)로 실제 간선 수만큼만 메모리를 사용하므로 효율적입니다. 또한 특정 정점의 인접 정점들을 순회하는 것이 빠릅니다. 단점은 두 정점 간 연결 여부를 확인하려면 리스트를 순회해야 해서 최악의 경우 O(V)가 걸립니다.</p>
      <p>따라서 <b>간선이 많은 밀집 그래프에는 인접 행렬</b>이, <b>간선이 적은 희소 그래프에는 인접 리스트</b>가 적합합니다. 실무에서는 대부분 희소 그래프이기 때문에 인접 리스트가 더 많이 사용됩니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q15. DFS(깊이 우선 탐색)와 BFS(너비 우선 탐색)의 차이점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p><b>DFS와 BFS는 그래프를 탐색하는 대표적인 두 가지 방법으로, 탐색 방향과 사용하는 자료구조에서 차이</b>가 있습니다.</p>
      <p><b>DFS, 깊이 우선 탐색</b>은 한 방향으로 끝까지 깊이 들어간 후 더 이상 갈 곳이 없으면 되돌아와서 다른 경로를 탐색하는 방식입니다. 내부적으로 <b>스택 또는 재귀 호출</b>을 사용합니다. 모든 경로를 탐색해야 하는 경우나 백트래킹 문제에 적합하며, 미로 탐색이나 사이클 검출 등에 활용됩니다.</p>
      <p><b>BFS, 너비 우선 탐색</b>은 시작 정점에서 가까운 정점부터 차례대로 방문하는 방식입니다. 내부적으로 <b>큐</b>를 사용합니다. 가까운 것부터 탐색하기 때문에 <b>최단 경로를 보장</b>해야 하는 문제에 적합하며, 최단 거리 탐색이나 레벨별 순회 등에 활용됩니다.</p>
      <p>정리하면, <b>모든 경로를 탐색하거나 경로의 특징을 파악해야 할 때는 DFS</b>를, <b>최단 경로나 최소 단계를 찾아야 할 때는 BFS</b>를 선택하면 됩니다. 두 알고리즘 모두 시간 복잡도는 O(V+E)로 동일합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q16. 선형 자료구조와 비선형 자료구조의 차이점은?</b></summary>
    <div class="accordion-content">
      <p><b>선형 자료구조와 비선형 자료구조의 가장 큰 차이는 데이터 간의 관계 구조</b>입니다. 선형은 일렬로 나열되고, 비선형은 계층적이거나 네트워크 형태로 연결됩니다.</p>
      <p><b>선형 자료구조</b>는 데이터가 순차적으로 나열되어 하나의 데이터 뒤에 하나의 데이터만 존재합니다. 대표적으로 배열, 연결 리스트, 스택, 큐가 있습니다. 구조가 단순해서 구현이 쉽고, 순차적으로 탐색하면 모든 데이터에 접근할 수 있습니다.</p>
      <p><b>비선형 자료구조</b>는 하나의 데이터 뒤에 여러 개의 데이터가 연결될 수 있는 구조입니다. 대표적으로 트리와 그래프가 있습니다. 계층 관계나 복잡한 연결 관계를 표현할 수 있으며, 탐색 시에는 DFS나 BFS 같은 별도의 알고리즘이 필요합니다.</p>
      <p>따라서 <b>순서가 중요하거나 단순한 데이터 관리에는 선형 자료구조</b>가 적합하고, <b>계층 구조나 객체 간 관계를 표현해야 할 때는 비선형 자료구조</b>가 적합합니다. 예를 들어, 작업 대기열은 큐로, 조직도나 파일 시스템은 트리로, 소셜 네트워크는 그래프로 표현하는 것이 자연스럽습니다.</p>
    </div>
  </details>

  </div>
</details>

<!-- ② 심화 면접 Q&A -->
<details>
  <summary><span class="accordion-title">💡 추가 예상 질문 Q&A</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <details>
    <summary style="font-size:1rem;"><b>Q17. 원형 큐(Circular Queue)란 무엇이며 일반 큐와의 차이점은?</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q18. 덱(Deque)이란 무엇이며 어떤 상황에서 유용한가요?</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q19. 트라이(Trie) 자료구조의 특징과 사용 목적은 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q20. B-Tree와 B+Tree의 차이점과 각각의 사용 용도는?</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q21. 레드-블랙 트리(Red-Black Tree)란 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q22. AVL 트리란 무엇이며 언제 사용하나요?</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q23. 배열의 시간 복잡도(접근, 삽입, 삭제)를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q24. 연결 리스트의 시간 복잡도(접근, 삽입, 삭제)를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q25. 단일 연결 리스트와 이중 연결 리스트의 차이점은?</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q26. 해시 테이블의 시간 복잡도는 어떻게 되나요?</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q27. 체이닝(Chaining)과 오픈 어드레싱(Open Addressing)의 차이점은?</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q28. 트리의 순회 방법들(전위, 중위, 후위)을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q29. 완전 이진 트리와 포화 이진 트리의 차이점은?</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q30. 힙 정렬의 시간 복잡도와 동작 과정을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q31. 최소 신장 트리(MST)란 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q32. 배열 기반 자료구조와 링크 기반 자료구조의 장단점은?</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q33. 자료구조 선택 시 고려해야 할 요소들은 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q34. 동적 배열의 크기 조정 방식과 시간 복잡도는?</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q35. 그래프에서 사이클을 찾는 방법은?</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q29. 완전 이진 트리와 포화 이진 트리의 차이점은?</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

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
