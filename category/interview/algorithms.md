---
layout: default
title: "알고리즘 면접 대비 — 완전 정리"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>알고리즘 면접 대비 — 기본·심화 Q&A + 개념 요약</h2>
  <p>구성: ① 기본 면접 Q&A → ② 심화 면접 Q&A → ③ 추가 예상 질문 Q&A → ④ 알고리즘 개념 요약</p>
</section>

<!-- ① 기본 면접 Q&A -->
<details open>
  <summary><span class="accordion-title">📋 기본 면접 Q&A</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <details>
    <summary style="font-size:1rem;"><b>Q1. 알고리즘이란 무엇이고, 좋은 알고리즘의 조건은 무엇인가요?</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
    <div class="accordion-content">
      <p>알고리즘은 문제를 해결하기 위한 명확하고 체계적인 절차나 방법을 의미합니다. 입력을 받아서 원하는 출력을 생성하는 일련의 단계들로 구성됩니다. 좋은 알고리즘의 조건으로는 정확성, 효율성, 명확성, 유한성, 그리고 일반성이 있습니다. 특히 시간 복잡도와 공간 복잡도가 낮을수록, 그리고 다양한 입력 크기에 대해 안정적으로 동작할수록 좋은 알고리즘이라고 할 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q2. 시간 복잡도와 공간 복잡도를 설명하고, Big O 표기법의 의미는 무엇인가요?</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
    <div class="accordion-content">
      <p>시간 복잡도는 알고리즘이 실행되는 데 걸리는 시간을 입력 크기에 대한 함수로 나타낸 것이고, 공간 복잡도는 알고리즘이 사용하는 메모리 공간을 나타낸 것입니다. Big O 표기법은 알고리즘의 성능을 최악의 경우를 기준으로 상한선을 표현하는 방법입니다. 입력 크기가 커질 때의 성장률에 초점을 맞춰서, 상수나 낮은 차수의 항들을 무시하고 가장 큰 차수의 항만 고려합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q3. 버블 정렬과 퀵 정렬의 차이점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>버블 정렬은 인접한 두 원소를 비교하여 큰 값을 뒤로 보내는 과정을 반복하는 알고리즘입니다. 구현이 간단하지만 시간 복잡도가 항상 O(n²)로 비효율적입니다. 퀵 정렬은 분할 정복 방식으로 피벗을 선택해서 작은 값들과 큰값들을 나누어 재귀적으로 정렬하는 알고리즘입니다. 평균적으로 O(n log n)의 우수한 성능을 보이지만, 최악의 경우 O(n²)가 될 수 있습니다. 실제로는 퀵 정렬이 캐시 효율성과 상수 인수 때문에 더 빠른 경우가 많습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q4. 병합 정렬(Merge Sort)의 동작 원리와 특징을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>병합 정렬은 분할 정복 기법을 사용하여 배열을 반으로 나누고, 각각을 재귀적으로 정렬한 후 병합하는 알고리즘입니다. 시간 복잡도가 항상 O(n log n)으로 안정적이며, 안정 정렬이라는 장점이 있습니다. 하지만 추가적인 메모리 공간이 O(n) 필요하다는 단점이 있습니다. 큰 데이터셋이나 안정성이 중요한 경우, 그리고 최악의 경우 성능이 보장되어야 하는 시스템에서 자주 사용됩니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q5. 이진 탐색(Binary Search)의 조건과 시간 복잡도를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>이진 탐색은 정렬된 배열에서 특정 값을 찾는 알고리즘입니다. 배열의 중간 원소와 찾는 값을 비교하여 탐색 범위를 절반씩 줄여나갑니다. 반드시 정렬된 상태에서만 사용할 수 있다는 전제 조건이 있습니다. 시간 복잡도는 O(log n)으로 매우 효율적이며, 공간 복잡도는 반복문으로 구현하면 O(1), 재귀로 구현하면 O(log n)입니다. 대용량 데이터에서 검색 성능이 중요한 시스템에 널리 활용됩니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q6. 깊이 우선 탐색(DFS)과 너비 우선 탐색(BFS)의 차이점은 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p>DFS는 그래프나 트리에서 한 경로를 끝까지 탐색한 후 다른 경로를 탐색하는 방식입니다. 스택이나 재귀를 사용하여 구현하며, 메모리 사용량이 적고 목표 노드가 깊은 곳에 있을 때 유리합니다. BFS는 현재 정점에서 인접한 모든 정점을 먼저 탐색하는 방식입니다. 큐를 사용하여 구현하며, 최단 경로를 찾거나 목표 노드가 얕은 곳에 있을 때 효율적입니다. 두 알고리즘 모두 시간 복잡도는 O(V + E)입니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q7. 동적 계획법(Dynamic Programming)이란 무엇이고 언제 사용하나요?</b></summary>
    <div class="accordion-content">
      <p>동적 계획법은 복잡한 문제를 작은 하위 문제들로 나누어 해결하고, 그 결과를 저장해두어 중복 계산을 피하는 알고리즘 기법입니다. 최적 부분 구조와 중복되는 하위 문제라는 두 조건을 만족할 때 사용할 수 있습니다. 피보나치 수열, 최장 공통 부분 수열, 배낭 문제 등에 적용됩니다. 메모이제이션(하향식)이나 태뷸레이션(상향식) 방식으로 구현하며, 시간 복잡도를 지수에서 다항식으로 크게 개선할 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q8. 욕심쟁이 알고리즘(Greedy Algorithm)의 특징과 한계는 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p>욕심쟁이 알고리즘은 각 단계에서 가장 좋아 보이는 선택을 하는 방식으로 문제를 해결합니다. 구현이 간단하고 실행 시간이 빠르다는 장점이 있지만, 항상 최적해를 보장하지는 않습니다. 활동 선택 문제, 최소 신장 트리(크러스칼, 프림), 다익스트라 알고리즘 등에서 최적해를 구할 수 있습니다. 욕심쟁이 선택 속성과 최적 부분 구조를 만족하는 문제에서만 올바른 해를 구할 수 있으므로, 적용 전에 이를 증명하는 것이 중요합니다.</p>
    </div>
  </details>

  </div>
</details>

<!-- ② 심화 면접 Q&A -->
<details>
  <summary><span class="accordion-title">🚀 심화 면접 Q&A</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <details>
    <summary style="font-size:1rem;"><b>Q9. 다익스트라 알고리즘과 벨만-포드 알고리즘의 차이점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>다익스트라 알고리즘은 음이 아닌 가중치를 가진 그래프에서 단일 출발점 최단 경로를 구하는 욕심쟁이 알고리즘입니다. 우선순위 큐를 사용하여 O((V+E) log V)의 시간 복잡도를 가집니다. 벨만-포드 알고리즘은 음의 가중치도 처리할 수 있으며, 음의 사이클까지 탐지할 수 있습니다. 하지만 시간 복잡도가 O(VE)로 더 느립니다. GPS 내비게이션처럼 실시간성이 중요한 곳에서는 다익스트라를, 금융 시스템처럼 음의 값이 존재할 수 있는 경우에는 벨만-포드를 사용합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q10. 플로이드-워셜 알고리즘은 언제 사용하며, 어떤 특징이 있나요?</b></summary>
    <div class="accordion-content">
      <p>플로이드-워셜 알고리즘은 모든 정점 쌍 간의 최단 경로를 구하는 동적 계획법 기반 알고리즘입니다. 시간 복잡도는 O(V³)이지만 구현이 간단하고, 음의 가중치도 처리할 수 있으며 음의 사이클도 탐지할 수 있습니다. 그래프의 크기가 작고(보통 V ≤ 400) 모든 쌍의 최단 경로가 필요한 경우에 적합합니다. 네트워크 라우팅, 게임에서의 경로 찾기, 관계 분석 등에 활용됩니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q11. 최소 신장 트리를 구하는 크러스칼과 프림 알고리즘을 비교해주세요.</b></summary>
    <div class="accordion-content">
      <p>크러스칼 알고리즘은 간선을 가중치 순으로 정렬한 후, 사이클을 만들지 않는 간선들을 선택하는 방식입니다. Union-Find 자료구조를 사용하며, 시간 복잡도는 O(E log E)입니다. 희소 그래프에서 유리합니다. 프림 알고리즘은 임의의 정점에서 시작하여 연결된 간선 중 최소 가중치를 가진 것을 선택해 나가는 방식입니다. 우선순위 큐를ㅡ사용하면 O(E log V)의 시간 복잡도를 가지며, 조밀한 그래프에서 더 효율적입니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q12. 백트래킹과 분할 정복의 차이점은 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p>백트래킹은 해를 찾는 도중 막다른 길에 도달하면 이전 상태로 되돌아가서 다른 경로를 시도하는 기법입니다. N-Queen, 스도쿠, 조합 탐색 등에 사용되며, 가지치기를 통해 불필요한 탐색을 줄입니다. 분할 정복은 문제를 작은 하위 문제들로 나누어 해결한 후 결합하는 방식입니다. 병합 정렬, 퀵 정렬, 이진 탐색 등에 사용되며, 보통 재귀적으로 구현됩니다. 백트래킹은 해 공간을 체계적으로 탐색하는 완전 탐색 기법이고, 분할 정복은 효율적인 문제 해결 패러다임입니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q13. KMP 문자열 매칭 알고리즘의 핵심 아이디어를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>KMP 알고리즘은 패턴과 텍스트가 불일치할 때, 이전에 일치했던 정보를 활용해서 패턴을 효율적으로 이동시키는 알고리즘입니다. 핵심은 부분 매치 테이블(실패 함수)을 미리 계산하는 것입니다. 이 테이블은 패턴의 각 위치 에서 접두사와 접미사가 일치하는 최대 길이를 저장합니다. 불일치 발생 시 패턴을 처음부터 비교하지 않고 적절한 위치로 이동시켜 O(n + m)의 시간 복잡도를 달성합니다. 텍스트 에디터나 검색 엔진에서 활용됩니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q14. 위상 정렬(Topological Sort)이란 무엇이고 어떻게 구현하나요?</b></summary>
    <div class="accordion-content">
      <p>위상 정렬은 방향 비사이클 그래프(DAG)에서 모든 간선 (u, v)에 대해 u가 v보다 먼저 오도록 정점들을 선형으로 나열하는 것입니다. 작업 스케줄링, 컴파일 순서 결정, 전공 이수 순서 등에 활용됩니다. 구현 방법으로는 DFS를 사용한 방법과 진입 차수를 이용한 칸(Kahn) 알고리즘이 있습니다. 칸 알고리즘은 진입 차수가 0인 정점부터 큐에 넣고 처리하면서, 연결된 정점들의 진입 차수를 감소시키는 방식입니다. 시간 복잡도는 O(V + E)입니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q15. 강연결 성분(Strongly Connected Component)을 찾는 방법을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>강연결 성분은 방향 그래프에서 서로 도달 가능한 정점들의 최대 집합입니다. 대표적인 알고리즘으로는 코사라주(Kosaraju) 알고리즘과 타잔(Tarjan) 알고리즘이 있습니다. 코사라주 알고리즘은 원래 그래프에서 DFS로 종료 시간을 기록하고, 전치 그래프에서 종료 시간 역순으로 DFS를 수행합니다. 타잔 알고리즘은 한 번의 DFS로 low-link 값을 계산하여 강연결 성분을 찾습니다. 둘 다 O(V + E)의 시간 복잡도를 가지며, 웹 페이지 클러스터링이나 소셜 네트워크 분석에 활용됩니다.</p>
    </div>
  </details>

  </div>
</details>

<!-- ③ 추가 예상 질문 Q&A -->
<details>
  <summary><span class="accordion-title">💡 추가 예상 질문 Q&A</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <details>
    <summary style="font-size:1rem;"><b>Q16. 네트워크 플로우(Network Flow) 문제와 최대 플로우를 구하는 방법은?</b></summary>
    <div class="accordion-content">
      <p>네트워크 플로우는 source에서 sink로 가는 유량의 최대값을 구하는 문제입니다. 각 간선에는 용량 제한이 있고, 플로우 보존 법칙을 만족해야 합니다. 포드-풀커슨 알고리즘은 증가 경로를 반복적으로 찾아서 플로우를 증가시키는 방법으로, 에드몬드-카프 알고리즘은 BFS로 최단 증가 경로를 찾아 O(VE²)의 시간 복잡도를 달성합니다. 디닉 알고리즘은 레벨 그래프를 구성해서 더 효율적으로 해결합니다. 이분 매칭, 최소 컷, 프로젝트 선택 문제 등으로 응용할 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q17. 유니온 파인드(Union-Find)에서 경로 압축과 랭크 결합의 효과는?</b></summary>
    <div class="accordion-content">
      <p>Union-Find는 서로소 집합을 관리하는 자료구조로, 최적화 없이는 연산 시간이 트리의 높이에 비례합니다. 경로 압축은 Find 연산 중에 방문한 모든 노드를 루트에 직접 연결하여 트리의 높이를 줄입니다. 랭크에 의한 결합은 항상 높이가 낮은 트리를 높은 트리에 붙여서 전체 높이 증가를 최소화합니다. 이 두 최적화를 함께 사용하면 m번의 연산에 대해 O(m α(n))의 시간 복잡도를 달성하며, 여기서 α는 아커만 함수의 역함수로 실질적으로 상수입니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q18. A* 알고리즘이 다익스트라보다 빠른 이유는 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p>A* 알고리즘은 다익스트라 알고리즘에 휴리스틱 함수를 추가한 최적 우선 탐색 알고리즘입니다. 각 정점에서 목적지까지의 예상 비용(휴리스틱)을 계산하여, 더 유망한 경로를 우선적으로 탐색합니다. 휴리스틱이 허용 가능(실제 비용을 과대 추정하지 않음)하고 일관성이 있다면 최적해를 보장하면서도 탐색 공간을 크게 줄일 수 있습니다. 게임 AI의 길찾기, 로봇 경로 계획, GPS 내비게이션 등에서 활용되며, 적절한 휴리스틱을 사용하면 다익스트라보다 훨씬 적은 노드를 방문하여 해를 찾을 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q19. 분할 정복에서 마스터 정리(Master Theorem)를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>마스터 정리는 분할 정복 알고리즘의 시간 복잡도를 쉽게 계산할 수 있게 해주는 공식입니다. T(n) = aT(n/b) + f(n) 형태의 점화식에서 a는 부문제의 개수, b는 분할 비율, f(n)은 분할과 결합에 드는 비용입니다. f(n)과 n^(log_b a)의 크기 관계에 따라 세 가지 경우로 나누어 시간 복잡도를 결정합니다. 예를 들어, 병합 정렬은 T(n) = 2T(n/2) + O(n)으로 두 번째 경우에 해당하여 O(n log n)이 됩니다. 이를 통해 복잡한 분할 정복 알고리즘의 성능을 빠르게 분석할 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q20. 해시 기반 알고리즘들(블룸 필터, 해시 조인 등)의 활용 사례는?</b></summary>
    <div class="accordion-content">
      <p>해시 기반 알고리즘들은 평균적으로 상수 시간 접근이 가능한 해시 테이블의 특성을 활용합니다. 블룸 필터는 확률적 자료구조로 거짓 양성은 있지만 거짓 음성은 없어서, 대용량 데이터에서 "확실히 없음"을 빠르게 판단할 수 있습니다. 해시 조인은 데이터베이스에서 두 테이블을 조인할 때 작은 테이블을 해시 테이블로 만들어 효율적으로 매칭하는 방법입니다. 카운팅 정렬도 해시의 아이디어를 사용하여 O(n + k) 시간에 정렬을 수행합니다. 이러한 기법들은 메모리가 충분하고 키의 분포가 균등할 때 매우 효율적입니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q21. 온라인 알고리즘과 오프라인 알고리즘의 차이점은 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p>온라인 알고리즘은 입력이 순차적으로 주어질 때 미래의 입력을 알지 못한 상태에서 즉시 결정을 내려야 하는 알고리즘입니다. 경쟁 비율(competitive ratio)로 성능을 측정하며, 최적 오프라인 알고리즘 대비 얼마나 나쁜지를 나타냅니다. 캐시 교체, 온라인 빈 패킹, 스케줄링 등이 대표적인 예입니다. 오프라인 알고리즘은 모든 입력을 미리 알고 있어서 전체 최적해를 구할 수 있습니다. 실시간 시스템이나 스트리밍 데이터 처리에서는 온라인 알고리즘이 필수적이며, 근사 알고리즘과 결합되어 실용적인 해를 제공합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q22. 병렬 알고리즘의 성능 척도와 설계 원칙은 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p>병렬 알고리즘의 성능은 작업량(work), 깊이(depth), 병렬성(parallelism)으로 측정됩니다. 작업량은 순차 실행 시간이고, 깊이는 가장 긴 의존성 경로의 길이입니다. 가속비는 순차 시간을 병렬 시간으로 나눈 값이며, 효율성은 가속비를 프로세서 수로 나눈 것입니다. 좋은 병렬 알고리즘 설계를 위해서는 작업을 독립적인 부분으로 나누고, 통신 오버헤드를 최소화하며, 로드 밸런싱을 고려해야 합니다. 분할 정복, 파이프라인, 데이터 병렬성 등의 패턴을 활용할 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q23. 근사 알고리즘은 언제 필요하고 어떻게 평가하나요?</b></summary>
    <div class="accordion-content">
      <p>근사 알고리즘은 NP-hard 문제처럼 최적해를 구하기 어려운 경우에 합리적인 시간 내에 근사해를 구하는 알고리즘입니다. 근사 비율(approximation ratio)로 성능을 평가하며, 이는 근사해와 최적해의 비율입니다. 예를 들어, 정점 커버 문제의 2-근사 알고리즘은 최적해의 2배 이하의 해를 보장합니다. PTAS(Polynomial-Time Approximation Scheme)는 임의의 ε > 0에 대해 (1+ε)-근사 알고리즘을 제공합니다. TSP, 배낭 문제, 집합 커버 등에서 활용되며, 실용적인 문제 해결에 매우 중요한 역할을 합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q24. 스트리밍 알고리즘의 특징과 대표적인 기법들은?</b></summary>
    <div class="accordion-content">
      <p>스트리밍 알고리즘은 메모리 제약이 있는 환경에서 대용량 데이터를 한 번만 순회하면서 처리하는 알고리즘입니다. 데이터 전체를 저장할 수 없으므로 스케치나 샘플링 기법을 사용합니다. Count-Min Sketch는 빈도수 추정에, HyperLogLog는 카디널리티 추정에 사용됩니다. 저장소 샘플링은 일정 크기의 무작위 샘플을 유지하고, 슬라이딩 윈도우는 최근 일정 기간의 데이터만 처리합니다. 빅데이터 처리, 네트워크 모니터링, 실시간 분석에서 핵심적인 역할을 합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q25. 양자 알고리즘과 고전 알고리즘의 근본적인 차이점은?</b></summary>
    <div class="accordion-content">
      <p>양자 알고리즘은 중첩(superposition)과 얽힘(entanglement) 같은 양자역학적 현상을 활용하여 계산을 수행합니다. 고전 비트와 달리 큐비트는 0과 1의 중첩 상태를 가질 수 있어 병렬 계산이 가능합니다. 쇼어 알고리즘은 소인수분해를 다항 시간에 해결하고, 그로버 알고리즘은 정렬되지 않은 데이터베이스 검색을 제곱근 시간에 수행합니다. 하지만 양자 측정 시 확률적 결과를 얻고, 양자 상태는 매우 불안정하다는 한계가 있습니다. 암호학, 최적화, 시뮬레이션 분야에서 혁신적인 성능 향상을 기대할 수 있습니다.</p>
    </div>
  </details>

  </div>
</details>

<!-- ④ 알고리즘 개념 요약 노트 -->
<details>
  <summary><span class="accordion-title">📚 알고리즘 개념 요약 노트</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <h3>🔄 정렬 알고리즘</h3>
  <p><b>버블 정렬 (Bubble Sort)</b></p>
  <p>인접 원소 비교 및 교환</p>
  <p>시간: O(n²), 공간: O(1)</p>
  <p>안정 정렬, 구현 간단</p>
  <p><b>선택 정렬 (Selection Sort)</b></p>
  <p>최솟값을 찾아서 앞으로 이동</p>
  <p>시간: O(n²), 공간: O(1)</p>
  <p>불안정 정렬, 교환 횟수 적음</p>
  <p><b>삽입 정렬 (Insertion Sort)</b></p>
  <p>정렬된 부분에 하나씩 삽입</p>
  <p>시간: O(n²), 공간: O(1)</p>
  <p>안정 정렬, 부분적으로 정렬된 경우 빠름</p>
  <p><b>퀵 정렬 (Quick Sort)</b></p>
  <p>피벗 기준 분할 후 재귀 정렬</p>
  <p>평균: O(n log n), 최악: O(n²)</p>
  <p>제자리 정렬, 캐시 효율성 좋음</p>
  <p><b>병합 정렬 (Merge Sort)</b></p>
  <p>분할 정복, 병합 과정에서 정렬</p>
  <p>시간: O(n log n), 공간: O(n)</p>
  <p>안정 정렬, 성능 일정</p>
  <p><b>힙 정렬 (Heap Sort)</b></p>
  <p>최대 힙 구성 후 루트를 제거</p>
  <p>시간: O(n log n), 공간: O(1)</p>
  <p>불안정 정렬, 제자리 정렬</p>

  <h3>🔍 탐색 알고리즘</h3>
  <p><b>선형 탐색 (Linear Search)</b></p>
  <p>순차적으로 하나씩 확인</p>
  <p>시간: O(n), 정렬 불필요</p>
  <p>간단한 구조, 작은 데이터에 적합</p>
  <p><b>이진 탐색 (Binary Search)</b></p>
  <p>중간값과 비교하여 절반씩 제거</p>
  <p>시간: O(log n), 정렬된 배열 필요</p>
  <p>대용량 데이터에서 효율적</p>

  <h3>🌐 그래프 알고리즘</h3>
  <p><b>깊이 우선 탐색 (DFS)</b></p>
  <p>스택/재귀, 한 경로를 끝까지</p>
  <p>시간: O(V + E), 공간: O(V)</p>
  <p>경로 존재성, 위상 정렬, 강연결 성분</p>
  <p><b>너비 우선 탐색 (BFS)</b></p>
  <p>큐 사용, 레벨별 탐색</p>
  <p>시간: O(V + E), 공간: O(V)</p>
  <p>최단 경로, 연결 성분</p>
  <p><b>다익스트라 (Dijkstra)</b></p>
  <p>음이 아닌 가중치 최단 경로</p>
  <p>시간: O((V + E) log V)</p>
  <p>GPS, 네트워크 라우팅</p>
  <p><b>벨만-포드 (Bellman-Ford)</b></p>
  <p>음의 가중치 허용, 음의 사이클 탐지</p>
  <p>시간: O(VE)</p>
  <p>금융 시스템, 거리 벡터 라우팅</p>
  <p><b>플로이드-워셜 (Floyd-Warshall)</b></p>
  <p>모든 쌍 최단 경로</p>
  <p>시간: O(V³)</p>
  <p>작은 그래프, 경유 최적화</p>
  <p><b>크러스칼 (Kruskal)</b></p>
  <p>간선 정렬 후 MST 구성</p>
  <p>시간: O(E log E)</p>
  <p>희소 그래프에 유리</p>
  <p><b>프림 (Prim)</b></p>
  <p>정점 중심 MST 구성</p>
  <p>시간: O(E log V)</p>
  <p>조밀한 그래프에 유리</p>

  <h3>📊 동적 계획법 패턴</h3>
  <p><b>선형 DP</b></p>
  <p>1차원 배열 사용</p>
  <p>피보나치, 계단 오르기</p>
  <p>점화식: dp[i] = f(dp[i-1], dp[i-2], ...)</p>
  <p><b>2차원 DP</b></p>
  <p>격자, 매트릭스 문제</p>
  <p>최장 공통 부분 수열, 편집 거리</p>
  <p>점화식: dp[i][j] = f(dp[i-1][j], dp[i][j-1], ...)</p>
  <p><b>배낭 DP</b></p>
  <p>제한된 용량 내에서 최적화</p>
  <p>0-1 배낭, 무한 배낭</p>
  <p>점화식: dp[i][w] = max(dp[i-1][w], dp[i-1][w-weight[i]] + value[i])</p>
  <p><b>구간 DP</b></p>
  <p>구간을 나누어 최적화</p>
  <p>매트릭스 체인 곱셈, 회문 분할</p>
  <p>점화식: dp[i][j] = min/max(dp[i][k] + dp[k+1][j] + cost)</p>

  <h3>🎯 알고리즘 설계 기법</h3>
  <p><b>분할 정복 (Divide & Conquer)</b></p>
  <p>문제를 작게 나누어 해결 후 결합</p>
  <p>병합 정렬, 퀵 정렬, 이진 탐색</p>
  <p>시간 복잡도: 마스터 정리 활용</p>
  <p><b>욕심쟁이 (Greedy)</b></p>
  <p>매 순간 최선의 선택</p>
  <p>활동 선택, 허프만 코딩</p>
  <p>최적 부분 구조 + 욕심쟁이 선택 속성</p>
  <p><b>백트래킹 (Backtracking)</b></p>
  <p>해를 찾아가다 막히면 되돌아가기</p>
  <p>N-Queen, 스도쿠, 부분집합</p>
  <p>가지치기로 탐색 공간 축소</p>

  <h3>⚡ 시간 복잡도 비교</h3>
  <p>알고리즘 분류 최선 평균 최악 공간</p>
  <p>버블 정렬 O(n) O(n²) O(n²) O(1)</p>
  <p>퀵 정렬 O(n log n) O(n log n) O(n²) O(log n)</p>
  <p>병합 정렬 O(n log n) O(n log n) O(n log n) O(n)</p>
  <p>힙 정렬 O(n log n) O(n log n) O(n log n) O(1)</p>
  <p>이진 탐색 O(1) O(log n) O(log n) O(1)</p>
  <p>DFS/BFS O(V + E) O(V + E) O(V + E) O(V)</p>
  <p>다익스트라 O(E log V) O(E log V) O(E log V) O(V)</p>

  <h3>🎯 문제 유형별 알고리즘 선택</h3>
  <p><b>정렬이 필요한 경우:</b></p>
  <p>작은 데이터: 삽입 정렬</p>
  <p>일반적인 경우: 퀵 정렬 또는 병합 정렬</p>
  <p>안정성 필요: 병합 정렬</p>
  <p>메모리 제약: 힙 정렬</p>
  <p><b>최단 경로:</b></p>
  <p>단일 출발점, 음이 아닌 가중치: 다익스트라</p>
  <p>단일 출발점, 음의 가중치 가능: 벨만-포드</p>
  <p>모든 쌍, 작은 그래프: 플로이드-워셜</p>
  <p><b>최적화 문제:</b></p>
  <p>탐욕적 선택 가능: 욕심쟁이</p>
  <p>중복 부분 문제: 동적 계획법</p>
  <p>모든 경우 확인 필요: 백트래킹</p>
  <p><b>트리/그래프 탐색:</b></p>
  <p>경로 존재성: DFS</p>
  <p>최단 거리: BFS</p>
  <p>위상 정렬: DFS 또는 진입차수</p>

  <h3>💭 면접 성공 팁</h3>
  <p>1. 시간/공간 복잡도 정확히 분석</p>
  <p>2. 알고리즘 선택 이유 설명</p>
  <p>3. 최적화 방법이나 개선점 제시</p>
  <p>4. 실제 사용 사례나 응용 분야 언급</p>
  <p>5. 트레이드오프(시간 vs 공간) 언급</p>
  <p>6. 의사 코드나 핵심 아이디어 설명</p>
  <p>7. 특수한 경우나 엣지 케이스 고려</p>
  <p>8. 다른 알고리즘과의 비교 분석</p>

  </div>
</details>
