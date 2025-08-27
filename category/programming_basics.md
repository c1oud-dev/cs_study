---
layout: default
title: "기초 프로그래밍 완전 정리"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>기초 프로그래밍 완전 정리 - 개념부터 면접까지</h2>
</section>

<!-- 면접 예상 질문 및 답변 (최상단) -->
<details open>
<summary><span class="accordion-title">면접 예상 질문 및 답변</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">
<details>
    <summary><b>Q1: 컴파일 언어와 인터프리터 언어의 차이점을 설명해주세요.</b></summary>
    <div class="accordion-content">
    <p><b>A:</b> 컴파일 언어는 소스코드를 실행 전에 기계어로 번역하여 실행 파일을 만드는 방식입니다. 실행 속도가 빠르고 배포 시 소스코드가 노출되지 않지만, 플랫폼에 종속적이고 컴파일 시간이 필요합니다. 인터프리터 언어는 코드를 한 줄씩 읽어가며 즉시 실행하는 방식으로, 플랫폼 독립적이고 개발과 테스트가 빠르지만 실행 속도가 상대적으로 느립니다.</p>
    </div>
</details>

<details>
    <summary><b>Q2: Call by Value와 Call by Reference의 차이점을 설명해주세요.</b></summary>
    <div class="accordion-content">
    <p><b>A:</b> Call by Value는 함수 호출 시 인자의 값 자체를 복사해서 전달하는 방식입니다. 함수 내에서 매개변수 값을 변경해도 원본 데이터에는 영향을 주지 않습니다. Call by Reference는 변수의 메모리 주소를 전달하는 방식으로, 함수 내에서 매개변수를 통해 원본 데이터를 직접 수정할 수 있습니다.</p>
    </div>
</details>

<details>
    <summary><b>Q3: 스택과 힙 메모리의 차이점을 설명해주세요.</b></summary>
    <div class="accordion-content">
    <p><b>A:</b> 스택 메모리는 지역변수와 매개변수가 저장되는 영역으로 LIFO 구조를 가지며 자동으로 메모리 관리가 됩니다. 힙 메모리는 동적으로 할당되는 메모리로 객체나 배열 등이 저장되며, 프로그래머가 직접 관리하거나 가비지 컬렉션을 통해 관리됩니다. 스택은 빠르지만 크기가 제한적이고, 힙은 상대적으로 느리지만 큰 메모리 공간을 사용할 수 있습니다.</p>
    </div>
</details>

<details>
    <summary><b>Q4: 재귀함수의 장단점을 설명해주세요.</b></summary>
    <div class="accordion-content">
    <p><b>A:</b> 재귀함수의 장점은 복잡한 문제를 간단하고 직관적으로 해결할 수 있고, 코드가 간결해진다는 점입니다. 단점은 함수 호출이 반복되면서 스택 메모리를 많이 사용하고, 잘못 구현하면 무한루프에 빠질 수 있으며, 일반적으로 반복문보다 성능이 떨어진다는 점입니다.</p>
    </div>
</details>

<details>
    <summary><b>Q5: 배열의 장단점을 설명해주세요.</b></summary>
    <div class="accordion-content">
    <p><b>A:</b> 배열의 장점은 인덱스를 통해 O(1) 시간에 원소에 접근할 수 있고, 메모리를 연속적으로 할당해 캐시 효율성이 좋으며, 메모리 오버헤드가 적다는 점입니다. 단점은 크기가 고정되어 있어 유연성이 떨어지고, 중간에 원소를 삽입하거나 삭제할 때 다른 원소들을 이동시켜야 해서 비효율적이라는 점입니다.</p>
    </div>
</details>

<details>
    <summary><b>Q6: 정적 타입과 동적 타입 언어의 차이점을 설명해주세요.</b></summary>
    <div class="accordion-content">
    <p><b>A:</b> 정적 타입 언어는 변수의 타입을 컴파일 시점에 결정하고 검사하는 언어로, 타입 안정성이 높고 실행 속도가 빠르지만 코드가 상대적으로 복잡합니다. 동적 타입 언어는 실행 시점에 타입이 결정되는 언어로, 코드 작성이 간단하고 유연하지만 런타임 에러 가능성이 있고 실행 속도가 상대적으로 느립니다.</p>
    </div>
</details>

<details>
    <summary><b>Q7: 전역변수와 지역변수의 차이점과 사용 시 주의사항을 설명해주세요.</b></summary>
    <div class="accordion-content">
    <p><b>A:</b> 전역변수는 프로그램 전체에서 접근 가능한 변수로 메모리에 프로그램 시작부터 종료까지 계속 존재합니다. 지역변수는 특정 함수나 블록 내에서만 접근 가능한 변수로 해당 범위를 벗어나면 메모리에서 해제됩니다. 전역변수는 남용하면 코드의 복잡성이 증가하고 디버깅이 어려워지므로, 꼭 필요한 경우가 아니라면 지역변수를 사용하는 것이 좋습니다.</p>
    </div>
</details>

<details>
    <summary><b>Q8: break문과 continue문의 차이점을 설명해주세요.</b></summary>
    <div class="accordion-content">
    <p><b>A:</b> break문은 현재 실행 중인 반복문이나 switch문을 완전히 빠져나가는 제어문입니다. continue문은 현재 반복을 중단하고 다음 반복으로 건너뛰는 제어문으로, 반복문 자체는 계속 실행됩니다.</p>
    </div>
</details>

  </div>
</details>

<!-- 추가 면접 예상 질문 (최상단 두번째) -->
<details>
  <summary><span class="accordion-title">추가 면접 예상 질문</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">
    
<h3>기초 개념</h3>
<details><summary>프로그래밍 패러다임에 대해 설명해주세요.</summary><div class="accordion-content">
<p>프로그래밍 패러다임은 프로그래밍의 관점이나 방식을 의미합니다. 주요 패러다임으로는 절차적 프로그래밍(순차적 명령어 실행), 객체지향 프로그래밍(객체 간 상호작용), 함수형 프로그래밍(함수의 조합), 선언형 프로그래밍(무엇을 할지 선언) 등이 있습니다. 각각은 문제 해결 방식과 코드 구조화 방법이 다르며, 프로젝트 특성에 따라 적절한 패러다임을 선택해야 합니다.</p>
</div></details>

<details><summary>변수명 규칙을 정하는 이유가 무엇인가요?</summary><div class="accordion-content">
<p>변수명 규칙은 코드의 가독성과 유지보수성을 향상시키기 위해서입니다. 일관된 명명 규칙을 따르면 다른 개발자가 코드를 이해하기 쉽고, 변수의 용도를 명확히 파악할 수 있습니다. 또한 예약어 충돌을 방지하고, 컴파일러나 인터프리터가 올바르게 식별할 수 있도록 도와줍니다. 협업 환경에서는 팀의 코딩 컨벤션 통일에도 중요한 역할을 합니다.</p>
</div></details>

<details><summary>상수를 사용하는 이유가 무엇인가요?</summary><div class="accordion-content">
<p>상수를 사용하는 이유는 첫째, 값의 변경을 방지하여 프로그램의 안정성을 높이기 위해서입니다. 둘째, 의미 있는 이름을 부여해 코드 가독성을 향상시킵니다. 셋째, 매직넘버를 제거하여 코드의 의도를 명확히 표현할 수 있습니다. 넷째, 값 변경이 필요한 경우 한 곳에서만 수정하면 되므로 유지보수가 용이합니다.</p></div></details>

<details><summary>타입 캐스팅이란 무엇이고 언제 사용하나요?</summary><div class="accordion-content">
<p>타입 캐스팅은 하나의 데이터 타입을 다른 데이터 타입으로 변환하는 과정입니다. 명시적 캐스팅은 프로그래머가 직접 타입을 변환하는 것이고, 암시적 캐스팅은 시스템이 자동으로 변환하는 것입니다. 서로 다른 타입의 변수 간 연산이 필요할 때, API 호출 시 매개변수 타입이 다를 때, 또는 더 큰 범위의 타입에서 작은 범위로 변환할 때 사용합니다.</p></div></details>

<h3>제어문 및 함수</h3>
<details><summary>for문과 while문의 적절한 사용 시기를 설명해주세요.</summary><div class="accordion-content">
<p>for문은 반복 횟수가 명확할 때 사용하는 것이 적절합니다. 배열 순회, 특정 횟수만큼 반복 실행, 카운터 기반 반복에서 주로 사용됩니다. while문은 조건에 따라 반복 횟수가 달라질 때 사용합니다. 사용자 입력 처리, 파일 끝까지 읽기, 특정 조건 만족까지 대기하는 경우 등에 적합합니다. 코드의 의도를 명확히 전달하는 것이 선택 기준이 되어야 합니다.</p></div></details>

<details><summary>switch문과 if-else문의 성능 차이가 있나요?</summary><div class="accordion-content">
<p>일반적으로 switch문이 if-else문보다 성능이 좋을 수 있습니다. switch문은 점프 테이블을 사용해 O(1) 시간에 해당 케이스로 이동할 수 있지만, if-else문은 조건을 순차적으로 검사해 최악의 경우 O(n) 시간이 걸립니다. 하지만 최신 컴파일러들이 최적화를 수행하므로 실제 성능 차이는 크지 않을 수 있습니다. 성능보다는 코드의 가독성과 유지보수성을 고려해 적절한 구문을 선택하는 것이 중요합니다.</p></div></details>

<details><summary>함수를 사용하는 이유와 장점을 설명해주세요.</summary><div class="accordion-content">
<p>함수를 사용하는 주요 이유는 코드 재사용성 향상입니다. 한 번 작성한 함수를 여러 곳에서 호출할 수 있어 중복 코드를 줄입니다. 또한 프로그램을 작은 단위로 분할하여 복잡성을 관리하고, 각 함수가 특정 기능을 담당하므로 디버깅과 테스트가 쉬워집니다. 함수명을 통해 코드의 의도를 명확히 표현할 수 있고, 팀 개발 시 업무 분담도 용이해집니다.</p></div></details>

<details><summary>매개변수와 인수의 차이점을 설명해주세요.</summary><div class="accordion-content">
<p>매개변수(Parameter)는 함수를 정의할 때 선언하는 변수로, 함수가 받을 값의 형태를 정의합니다. 인수(Argument)는 함수를 호출할 때 실제로 전달하는 값입니다. 즉, 매개변수는 함수 정의 시의 형식적인 변수이고, 인수는 함수 호출 시의 실제 값입니다. 매개변수는 함수 내부에서 지역변수로 동작하며, 인수의 값을 받아 처리합니다.</p></div></details>

<h3>메모리 및 성능</h3>
<details><summary>메모리 누수란 무엇이고 어떻게 방지할 수 있나요?</summary><div class="accordion-content">
<p>메모리 누수는 프로그램이 할당한 메모리를 사용 후 적절히 해제하지 않아 사용 가능한 메모리가 점점 줄어드는 현상입니다. 동적으로 할당한 메모리를 free/delete 하지 않거나, 순환 참조로 가비지 컬렉션이 되지 않을 때 발생합니다. 방지 방법으로는 할당한 메모리는 반드시 해제하고, RAII 패턴이나 스마트 포인터 사용, 메모리 프로파일링 도구 활용, 코드 리뷰를 통한 검증 등이 있습니다.</p></div></details>

<details><summary>가비지 컬렉션이 작동하는 원리를 간단히 설명해주세요.</summary><div class="accordion-content">
<p>가비지 컬렉션은 프로그램에서 더 이상 사용하지 않는 메모리를 자동으로 찾아 해제하는 메커니즘입니다. 주로 루트 객체(전역변수, 스택의 지역변수)에서 시작하여 참조 가능한 모든 객체를 표시하고, 표시되지 않은 객체들을 가비지로 판단해 메모리를 해제합니다. 주요 알고리즘으로는 Mark & Sweep, 참조 카운팅, 세대별 수집 등이 있으며, 각각 장단점이 다릅니다.</p></div></details>

<details><summary>프로그램 성능 최적화를 위해 어떤 점들을 고려해야 하나요?</summary><div class="accordion-content">
<p>먼저 프로파일링을 통해 병목 지점을 파악해야 합니다. 알고리즘과 자료구조 선택이 가장 큰 영향을 미치므로 시간복잡도가 낮은 것을 선택해야 합니다. 메모리 사용량 최적화, 불필요한 연산 제거, 캐싱 활용, 데이터베이스 쿼리 최적화 등도 중요합니다. 하지만 가독성과 유지보수성을 희생하면서까지 최적화하는 것은 지양해야 하며, 실제로 성능 문제가 되는 부분에만 집중적으로 최적화를 적용해야 합니다.</p></div></details>

<h3>실무 관련</h3>
<details><summary>코드 가독성을 높이기 위한 방법들을 제시해주세요.</summary><div class="accordion-content">
<p>의미 있는 변수명과 함수명을 사용하고, 일관된 코딩 컨벤션을 따라야 합니다. 함수는 하나의 기능만 수행하도록 작게 만들고, 적절한 주석을 달되 코드 자체가 설명이 될 수 있도록 작성합니다. 중첩 깊이를 줄이고, 매직넘버 대신 상수를 사용하며, 코드 블록 간 공백을 적절히 활용해 시각적 구분을 명확히 합니다. 복잡한 조건문은 별도 함수로 추출하는 것도 좋은 방법입니다.</p></div></details>

<details><summary>디버깅을 효과적으로 하기 위한 방법은 무엇인가요?</summary><div class="accordion-content">
<p>문제를 재현할 수 있는 최소한의 코드를 작성하고, 디버거를 활용해 단계별로 실행하면서 변수 상태를 확인합니다. 로그를 적절히 활용하여 프로그램 흐름을 추적하고, 단위 테스트를 작성해 함수별로 검증합니다. 코드 리뷰를 통해 다른 시각에서 문제를 바라보고, 문제 해결 과정을 문서화하여 유사한 문제 발생 시 참고할 수 있도록 합니다. 무엇보다 문제를 정확히 정의하고 가정을 검증하는 것이 중요합니다.</p></div></details>

<details><summary>좋은 함수를 작성하기 위한 원칙들을 설명해주세요.</summary><div class="accordion-content">
<p>단일 책임 원칙에 따라 하나의 함수는 하나의 기능만 수행해야 합니다. 함수명은 기능을 명확히 표현하고, 매개변수 개수는 가능한 적게 유지합니다. 사이드 이펙트를 최소화하고, 같은 입력에 대해 항상 같은 출력을 반환하도록 작성합니다. 적절한 길이를 유지하고(보통 20-30줄 이내), 중첩 깊이를 줄여 가독성을 높입니다. 예외 상황에 대한 처리도 포함하고, 함수의 전제 조건과 후행 조건을 명확히 정의합니다.</p></div></details>
  </div>
</details>

<!-- 기초(1~9)를 한 곳의 아코디언으로 묶기 -->
<details>
  <summary><span class="accordion-title">기초 (1~9) — 프로그래밍 언어 기초, 변수/상수, 데이터 타입, 연산자, 제어문, 함수, 배열, 문자열, 메모리 관리</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

<!-- 1. 프로그래밍 언어 기초 -->
<details>
<summary><b>1. 프로그래밍 언어 기초</b></summary>
<div class="accordion-content">
<h3>1.1 프로그래밍 언어란?</h3>
<p>컴퓨터와 소통하기 위한 언어로, 인간의 논리를 컴퓨터가 이해할 수 있는 형태로 변환해주는 도구입니다.</p>

<h3>1.2 컴파일 vs 인터프리터</h3>
<ul>
    <li><b>컴파일 언어</b>: 전체 소스코드를 미리 기계어로 번역 (C, Java, C++)
    <ul>
        <li>장점: 실행 속도 빠름, 배포 시 소스코드 노출 안됨</li>
        <li>단점: 플랫폼 종속적, 컴파일 시간 필요</li>
    </ul>
    </li>
    <li><b>인터프리터 언어</b>: 코드를 한 줄씩 읽어가며 실행 (Python, JavaScript)
    <ul>
        <li>장점: 플랫폼 독립적, 개발과 테스트가 빠름</li>
        <li>단점: 실행 속도가 상대적으로 느림</li>
    </ul>
    </li>
</ul>

<h3>1.3 정적 vs 동적 타입</h3>
<ul>
    <li><b>정적 타입</b>: 변수 타입을 미리 선언 (Java, C++)</li>
    <li><b>동적 타입</b>: 실행 시 타입이 결정 (Python, JavaScript)</li>
</ul>
</div>
</details>

<!-- 2. 변수와 상수 -->
<details>
<summary><b>2. 변수와 상수</b></summary>
<div class="accordion-content">
<h3>2.1 변수 (Variable)</h3>
<p>값을 저장하는 메모리 공간에 붙인 이름입니다. 프로그램 실행 중 값이 변경될 수 있습니다.</p>

<h3>2.2 상수 (Constant)</h3>
<p>한 번 초기화되면 값을 변경할 수 없는 변수입니다.</p>

<h3>2.3 변수명 규칙</h3>
<ul>
    <li>영문자, 숫자, 언더스코어 사용 가능</li>
    <li>숫자로 시작할 수 없음</li>
    <li>예약어 사용 불가</li>
    <li>camelCase 또는 snake_case 사용</li>
</ul>

<h3>2.4 스코프 (Scope)</h3>
<p>변수가 접근 가능한 범위를 의미합니다.</p>
<ul>
    <li><b>전역 스코프</b>: 프로그램 전체에서 접근 가능</li>
    <li><b>지역 스코프</b>: 특정 함수나 블록 내에서만 접근 가능</li>
</ul>
</div>
</details>

<!-- 3. 데이터 타입 -->
<details>
<summary><b>3. 데이터 타입</b></summary>
<div class="accordion-content">
<h3>3.1 기본 데이터 타입 (Primitive Types)</h3>
<ul>
    <li><b>정수형</b>: int, long (1, 100, -50)</li>
    <li><b>실수형</b>: float, double (3.14, 2.7)</li>
    <li><b>문자형</b>: char ('A', 'z')</li>
    <li><b>불린형</b>: boolean (true, false)</li>
</ul>

<h3>3.2 참조 데이터 타입 (Reference Types)</h3>
<ul>
    <li><b>문자열</b>: String ("Hello", "World")</li>
    <li><b>배열</b>: Array ([1, 2, 3, 4])</li>
    <li><b>객체</b>: Object</li>
</ul>

<h3>3.3 타입 변환</h3>
<ul>
    <li><b>명시적 변환</b>: 프로그래머가 직접 타입 변환</li>
    <li><b>암시적 변환</b>: 시스템이 자동으로 타입 변환</li>
</ul>
</div>
</details>

<!-- 4. 연산자 -->
<details>
<summary><b>4. 연산자</b></summary>
<div class="accordion-content">
<h3>4.1 산술 연산자</h3>
<p><code>+</code> (덧셈), <code>-</code> (뺄셈), <code>*</code> (곱셈), <code>/</code> (나눗셈), <code>%</code> (나머지)</p>

<h3>4.2 비교 연산자</h3>
<p><code>==</code> (같음), <code>!=</code> (다름), <code>&gt;</code> (초과), <code>&lt;</code> (미만), <code>&gt;=</code> (이상), <code>&lt;=</code> (이하)</p>

<h3>4.3 논리 연산자</h3>
<p><code>&amp;&amp;</code> (AND), <code>||</code> (OR), <code>!</code> (NOT)</p>

<h3>4.4 대입 연산자</h3>
<p><code>=</code> (대입), <code>+=</code>, <code>-=</code>, <code>*=</code>, <code>/=</code> (복합 대입)</p>

<h3>4.5 증감 연산자</h3>
<p><code>++</code> (증가), <code>--</code> (감소)</p>
<ul>
    <li><b>전위</b>: <code>++a</code> (값을 먼저 증가시킨 후 사용)</li>
    <li><b>후위</b>: <code>a++</code> (값을 사용한 후 증가)</li>
</ul>
</div>
</details>

<!-- 5. 제어문 -->
<details>
<summary><b>5. 제어문</b></summary>
<div class="accordion-content">
<h3>5.1 조건문 (Conditional Statements)</h3>
<pre><code>if (조건) {
    // 조건이 참일 때 실행
    } else if (다른조건) {
    // 다른 조건이 참일 때 실행
    } else {
    // 모든 조건이 거짓일 때 실행
    }</code></pre>

        <pre><code>switch (변수) {
    case 값1:
        // 실행문
        break;
    case 값2:
        // 실행문
        break;
    default:
        // 기본 실행문
}</code></pre>

<h3>5.2 반복문 (Loop Statements)</h3>
<ul>
    <li><b>for문</b>: 정확한 반복 횟수를 알 때 사용합니다.</li>
    <li><b>while문</b>: 조건이 참인 동안 반복 실행합니다.</li>
    <li><b>do-while문</b>: 최소 한 번은 실행하고 조건을 검사합니다.</li>
</ul>

<h3>5.3 제어문 키워드</h3>
<ul>
    <li><b>break</b>: 반복문 탈출</li>
    <li><b>continue</b>: 현재 반복을 건너뛰고 다음 반복 진행</li>
</ul>
</div>
</details>

<!-- 6. 함수 -->
<details>
<summary><b>6. 함수 (Function)</b></summary>
<div class="accordion-content">
<h3>6.1 함수의 정의</h3>
<p>특정 작업을 수행하는 코드 블록으로, 재사용 가능한 코드 단위입니다.</p>

<h3>6.2 함수의 구성 요소</h3>
<ul>
    <li><b>함수명</b>: 함수를 식별하는 이름</li>
    <li><b>매개변수</b>: 함수에 전달되는 값</li>
    <li><b>반환값</b>: 함수가 실행 후 돌려주는 값</li>
    <li><b>함수 몸체</b>: 실제 실행되는 코드</li>
</ul>

<h3>6.3 함수의 장점</h3>
<ul>
    <li>코드 재사용성 향상</li>
    <li>프로그램 구조화</li>
    <li>디버깅 용이</li>
    <li>유지보수 편의성</li>
</ul>

<h3>6.4 매개변수 전달 방식</h3>
<ul>
    <li><b>Call by Value</b>: 값 자체를 복사해서 전달</li>
    <li><b>Call by Reference</b>: 메모리 주소를 전달</li>
</ul>

<h3>6.5 재귀 함수 (Recursive Function)</h3>
<p>함수가 자기 자신을 호출하는 함수입니다.</p>
<ul>
    <li><b>기저 조건</b>: 재귀 호출을 멈추는 조건 (필수)</li>
    <li><b>재귀 호출</b>: 자기 자신을 호출하는 부분</li>
</ul>
</div>
</details>

<!-- 7. 배열 -->
<details>
<summary><b>7. 배열 (Array)</b></summary>
<div class="accordion-content">
<h3>7.1 배열의 정의</h3>
<p>같은 타입의 여러 데이터를 연속된 메모리 공간에 저장하는 자료구조입니다.</p>

<h3>7.2 배열의 특징</h3>
<ul>
    <li>인덱스를 통한 빠른 접근 (O(1))</li>
    <li>메모리 효율적 저장</li>
    <li>크기가 고정적 (정적 배열의 경우)</li>
    <li>연속된 메모리 할당</li>
</ul>

<h3>7.3 다차원 배열</h3>
<ul>
    <li><b>1차원 배열</b>: 일렬로 나열된 데이터</li>
    <li><b>2차원 배열</b>: 행과 열로 구성된 테이블 형태</li>
    <li><b>3차원 이상</b>: 더 복잡한 차원 구조</li>
</ul>
</div>
</details>

<!-- 8. 문자열 -->
<details>
<summary><b>8. 문자열 (String)</b></summary>
<div class="accordion-content">
<h3>8.1 문자열의 특징</h3>
<ul>
    <li>문자들의 연속된 집합</li>
    <li>대부분 언어에서 불변(Immutable) 객체</li>
    <li>다양한 조작 메서드 제공</li>
</ul>

<h3>8.2 문자열 처리 연산</h3>
<ul>
    <li>연결(Concatenation)</li>
    <li>부분 문자열 추출(Substring)</li>
    <li>길이 계산(Length)</li>
    <li>검색(Search)</li>
    <li>치환(Replace)</li>
</ul>
</div>
</details>

<!-- 9. 메모리 관리 -->
<details>
<summary><b>9. 메모리 관리</b></summary>
<div class="accordion-content">
<h3>9.1 스택 메모리</h3>
<ul>
    <li>지역 변수, 매개변수 저장</li>
    <li>LIFO(Last In First Out) 구조</li>
    <li>자동 메모리 관리</li>
    <li>크기가 제한적</li>
</ul>

<h3>9.2 힙 메모리</h3>
<ul>
    <li>동적으로 할당되는 메모리</li>
    <li>객체, 배열 등이 저장</li>
    <li>수동 또는 가비지 컬렉션으로 관리</li>
    <li>상대적으로 큰 메모리 공간</li>
</ul>

<h3>9.3 가비지 컬렉션</h3>
<p>더 이상 사용하지 않는 메모리를 자동으로 해제하는 메커니즘입니다.</p>
</div>
</details>

  </div>
</details>
