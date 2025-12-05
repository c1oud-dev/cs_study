---
layout: default
title: "Java Interview — 완벽 가이드"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>자바 면접 대비</h2>
  <p>구성: 📋 기본 면접 Q&A → 💡 추가 예상 질문 Q&A → 📚 자바 개념 요약 노트</p>
</section>

<details open>
  <summary><span class="accordion-title">📋 기본 면접 Q&A</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">
<details>
  <summary style="font-size:1rem;"><b>Q1. 자바의 특징과 장점은 무엇인가요?</b>
    <span style="float:right;">✅🟩🟩🟩🟩</span>
  </summary>
  <div class="accordion-content">
    <p>자바의 특징과 장점은 크게 세 가지로 정리할 수 있을 것 같습니다. 첫째, 자바는 플랫폼에 독립적인 객체지향 언어입니다. JVM 위에서 동작하기 때문에 한 번 작성한 코드를 운영체제에 상관없이 실행할 수 있고, 클래스·상속·캡슐화·다형성과 같은 객체지향 개념을 잘 지원해서 유지보수성과 재사용성이 높습니다.</p>
    <p>둘째, 자동 메모리 관리와 높은 안정성입니다. 가비지 컬렉션으로 메모리를 자동으로 회수해 주기 때문에 개발자가 메모리 해제에 직접 신경 쓰지 않아도 되고, 정적 타입 언어라 컴파일 단계에서 많은 오류를 사전에 잡을 수 있어 안정적인 서비스 개발에 유리합니다.</p>
    <p>셋째, 풍부한 생태계와 검증된 프레임워크입니다. 표준 라이브러리가 풍부하고, Spring / Spring Boot 같은 프레임워크가 잘 갖춰져 있어서 웹·백엔드 애플리케이션을 빠르게 개발할 수 있습니다. 멀티스레딩과 동시성 지원도 좋아서 대규모 트래픽을 처리하는 서버 개발에 많이 사용되고 있고, 커뮤니티와 자료가 많아 학습과 문제 해결이 쉽다는 점도 장점이라고 생각합니다.</p>
  </div>
</details>
<details>

  <summary style="font-size:1rem;"><b>Q2. JVM, JRE, JDK의 차이점을 설명해주세요.</b>
    <span style="float:right;">✅🟩🟩🟩🟩</span>
  </summary>
  <div class="accordion-content">
    <p>JVM, JRE, JDK는 자바 프로그램이 실행되는 환경과 개발 도구를 단계별로 나눈 개념이라고 생각합니다.</p>
    <p>먼저 JVM(Java Virtual Machine) 은 자바 바이트코드를 실제 운영체제에서 실행해 주는 가상 머신입니다. 자바가 “Write Once, Run Anywhere”를 실현할 수 있는 핵심이고, 메모리 관리, GC, 스레드 관리 등을 담당합니다.</p>
    <p>JRE(Java Runtime Environment) 는 자바 프로그램을 실행하기 위한 환경입니다. 내부에 JVM과 자바 표준 라이브러리(API)들이 포함되어 있어서, “자바 프로그램을 돌리기만 할 때” 필요한 구성이라고 볼 수 있습니다.</p>
    <p>JDK(Java Development Kit) 는 이름 그대로 자바 개발을 위한 키트입니다. JRE를 포함하고 있고, 여기에 javac 같은 컴파일러, 디버거, 도큐먼트 생성 도구 같은 개발 도구들이 추가로 들어 있습니다. 그래서 자바 애플리케이션을 만들고 빌드할 때는 JDK가 필요합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q3. 객체지향 프로그래밍의 4대 특징을 설명해주세요.</b>
    <span style="float:right;">✅🟩🟩🟩🟩</span>
  </summary>
  <div class="accordion-content">
    <p>객체지향 프로그래밍의 4대 특징은 추상화, 캡슐화, 상속, 다형성입니다.</p>
    <p>먼저 추상화는 복잡한 현실 세계의 대상에서 필요한 속성과 행동만 선별해서 모델링하는 것입니다. 중요한 공통 개념만 코드로 표현함으로써 복잡도를 줄이고 도메인을 명확하게 표현할 수 있게 해줍니다.</p>
    <p>캡슐화는 데이터와 그 데이터를 다루는 메서드를 하나로 묶고, 접근 제어자를 통해 외부에서 직접 접근을 제한하는 것입니다. 이를 통해 객체의 내부 상태를 보호하고, 외부에는 필요한 인터페이스만 공개해서 안정성과 응집도를 높입니다.</p>
    <p>상속은 기존 클래스를 기반으로 새로운 클래스를 정의해 공통된 속성과 기능을 재사용하는 것입니다. 중복 코드를 줄이고, 공통 로직을 상위 클래스에 모아 관리할 수 있어서 유지보수성과 확장성이 좋아집니다.</p>
    <p>마지막으로 다형성은 같은 메시지(메서드 호출)에 대해 실제 객체 타입에 따라 다른 동작을 수행할 수 있는 능력입니다. 주로 오버라이딩과 인터페이스를 통해 구현되고, 이를 통해 클라이언트 코드를 수정하지 않고도 새로운 구현체를 쉽게 추가할 수 있어 유연한 설계를 가능하게 합니다.</p>
    <p>정리하면, 이 네 가지 특징을 통해 객체지향은 복잡도를 관리하면서도 재사용성과 유연성을 높이고, 변경에 강한 구조를 만들 수 있게 해준다고 생각합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q4. String, StringBuffer, StringBuilder의 차이점은?</b>
  <span style="float:right;">✅🟩🟩🟩🟩</span></summary>
  <div class="accordion-content">
    <p>String, StringBuffer, StringBuilder의 차이는 불변 여부, 스레드 안전성, 성능/사용 목적 관점에서 나눠서 이해하고 있습니다.</p>
    <p>먼저 String은 불변(Immutable) 객체입니다. 한 번 생성되면 내부 값이 변하지 않고, 문자열을 더하거나 수정하는 연산을 하면 항상 새로운 String 객체가 생성됩니다. 그래서 코드가 직관적이고 안전하지만, 문자열을 자주 변경하는 상황에서는 객체가 많이 생성돼서 메모리와 성능에 부담이 될 수 있습니다.</p>
    <p>StringBuffer와 StringBuilder는 둘 다 가변(Mutable)한 문자열을 다루기 위한 클래스입니다. 내부 버퍼에서 내용을 직접 수정하기 때문에, 반복적인 추가/삭제/수정에 대해 String보다 성능이 좋습니다.</p>
    <p>이 둘의 가장 큰 차이는 스레드 안전성입니다.</p>
    <ul>
      <li>StringBuffer는 메서드들이 synchronized로 동기화되어 있어서 멀티스레드 환경에서 동시에 같은 인스턴스를 사용할 때 스레드 안전(Thread-safe) 합니다. 대신 동기화 비용 때문에 상대적으로 성능이 떨어질 수 있습니다.</li>
      <li>StringBuilder는 동기화를 지원하지 않아서 스레드 안전하지 않지만, 그만큼 불필요한 락이 없기 때문에 단일 스레드 환경에서는 가장 빠른 문자열 변경 클래스로 사용할 수 있습니다.</li>
    </ul>
    <p>정리하면,</p>
    <ul>
      <li>String: 불변, 간단하고 안전하지만 잦은 변경에는 비효율적</li>
      <li>StringBuffer: 가변, 스레드 안전, 멀티스레드 환경에서 문자열을 자주 변경할 때 사용.</li>
      <li>StringBuilder: 가변, 스레드 미보장, 단일 스레드에서 성능이 가장 중요할 때 우선적으로 선택</li>
    </ul>
    <p>실제 개발에서는 일반적인 단일 스레드 로직에는 StringBuilder를 기본으로 사용하고, 공유 객체를 여러 스레드에서 함께 수정해야 한다면 StringBuffer를 고려하는 편입니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q5. 접근 제한자(Access Modifier)의 종류와 특징은?</b>
  <span style="float:right;">✅🟩🟩🟩🟩</span></summary>
  <div class="accordion-content">
    <p>자바에서 접근 제한자는 크게 public, protected, (default), private 이렇게 네 가지가 있고, 이를 통해 클래스나 필드, 메서드의 접근 범위를 제어해서 캡슐화를 강화한다고 이해하고 있습니다.</p>
    <p>먼저 public은 가장 개방적인 접근 제한자로, 어디서든지 접근이 가능합니다. 패키지나 클래스 위치에 상관 없이 사용할 수 있어서, 외부에 공개해야 하는 API나 서비스 인터페이스 같은 부분에 주로 사용합니다.</p>
    <p>반대로 private은 가장 폐쇄적인 제한자로, 선언된 클래스 내부에서만 접근이 가능합니다. 다른 클래스는 물론이고, 같은 패키지의 클래스에서도 접근할 수 없기 때문에, 객체의 내부 상태를 감추고 외부에서는 메서드를 통해서만 조작하도록 만들 때 사용합니다. 캡슐화 측면에서 가장 중요한 키워드라고 생각합니다.</p>
    <p>default, 즉 아무 접근 제한자를 쓰지 않았을 때는 흔히 패키지 프라이빗(package-private) 이라고 부르고, 같은 패키지 내에서는 접근 가능하지만, 다른 패키지에서는 접근할 수 없습니다. 외부에는 공개할 필요는 없지만, 같은 패키지 내부에서만 공유하고 싶은 경우에 사용합니다. (참고로, 최상위 클래스는 public이거나 default 둘 중 하나만 사용할 수 있습니다.)</p>
    <p>마지막으로 protected는 같은 패키지 내에서는 접근 가능하고, 다른 패키지라 하더라도 상속 관계에 있는 자식 클래스에서는 접근이 허용됩니다. 그래서 주로 상속을 고려한 설계에서, 완전히 숨기지는 않되 자식 클래스가 재사용하거나 확장할 수 있도록 열어두고 싶을 때 사용합니다.</p>
    <p>정리하자면, 자바의 접근 제한자는 public → protected → default → private 순으로 점점 범위가 좁아지고, 실제로는 일단 private을 기본으로 두고, 정말 필요한 최소 범위까지만 접근을 열어주는 방향으로 사용하는 것이 캡슐화와 유지보수 측면에서 바람직하다고 생각합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q6. 오버로딩(Overloading)과 오버라이딩(Overriding)의 차이점은?</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
  <div class="accordion-content">
    <p>오버로딩과 오버라이딩은 이름은 비슷하지만, 목적과 발생 시점, 사용하는 자리가 완전히 다르다고 이해하고 있습니다.</p>
    <p>먼저 오버로딩(Overloading) 은 같은 클래스 안에서 메서드 이름은 같게 두되, 매개변수 목록을 다르게 정의하는 것을 말합니다. 매개변수의 개수, 타입, 순서를 바꿔서 여러 버전의 메서드를 제공하는 방식이고, 호출 시점에 컴파일러가 전달된 인자의 타입과 개수를 보고 어떤 메서드를 부를지 결정합니다. 그래서 오버로딩은 보통 컴파일 타임에 결정되는 정적 바인딩으로 분류되고, 같은 의미의 기능을 인자만 다르게 받고 싶을 때 사용해서 API를 더 직관적이고 편리하게 만드는 역할을 합니다. 이때 반환 타입만 다르고 매개변수가 같다면 오버로딩으로 인정되지 않는다는 제약도 있습니다.</p>
    <p>반면에 오버라이딩(Overriding) 은 상속 관계에서 자식 클래스가 부모 클래스의 메서드를 재정의하는 것입니다. 이름, 매개변수, 반환 타입이 부모와 동일해야 하고(또는 자바에서 허용하는 공변 반환 타입), 접근 제한자는 더 좁아질 수 없다는 등의 규칙을 따릅니다. 이렇게 재정의된 메서드는 실제 객체의 타입에 따라 런타임에 어떤 구현이 호출될지 결정되기 때문에, 오버라이딩은 런타임 다형성을 구현하는 핵심 메커니즘이라고 볼 수 있습니다. 이를 통해 상위 타입으로 코드를 작성해 두고, 실제 구현만 교체하면서 유연하게 확장 가능한 구조를 만들 수 있습니다.</p>
    <p>정리하면, 오버로딩은 같은 클래스 안에서 “같은 이름 + 다른 파라미터”로 메서드를 여러 개 두어 호출 편의성과 가독성을 높이는 기능이고, 오버라이딩은 상속 관계에서 “같은 시그니처”의 메서드를 재정의해서 객체의 실제 타입에 따른 다른 동작을 가능하게 하는 기능입니다. 시점으로 보면 오버로딩은 컴파일 타임에, 오버라이딩은 런타임에 메서드가 결정된다는 점에서 차이가 있다고 생각합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q7. 추상 클래스(Abstract Class)와 인터페이스(Interface)의 차이점은?</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
  <div class="accordion-content">
    <p>추상 클래스와 인터페이스는 둘 다 추상화를 위한 도구지만, 저는 보통 “공통 구현을 공유하느냐 / 순수한 규약이냐”를 기준으로 구분해서 이해하고 있습니다.</p>
    <p>먼저 추상 클래스(Abstract Class) 는 “공통된 상태와 기본 동작을 어느 정도 가지고 있는 상위 타입”에 가깝습니다. 필드, 생성자, 일반 메서드, 추상 메서드를 모두 가질 수 있고, 일반 메서드를 통해 공통 로직을 미리 구현해 두고 자식 클래스가 이를 상속 받아 재사용할 수 있습니다. 또 한 클래스만 extends 할 수 있기 때문에, 상속 계층에서 공통 기능을 묶는 용도로 많이 사용합니다.</p>
    <p>반면 인터페이스(Interface) 는 “이 타입을 구현하는 클래스라면 반드시 제공해야 하는 기능의 규약”을 정의하는 역할에 더 가깝습니다. 원래는 전부 추상 메서드만 가질 수 있었지만, 현재는 default 메서드와 static 메서드도 허용되면서 일부 공통 구현도 가질 수 있게 됐습니다. 그럼에도 불구하고 필드는 항상 public static final이고, 여전히 “어떤 동작을 할 수 있는지”를 명세하는 데 초점이 맞춰져 있습니다. 또 인터페이스는 여러 개를 동시에 구현(implements)할 수 있어서, 클래스 계층과 별개로 기능 단위의 계약을 조합할 때 유리합니다.</p>
    <p>정리하면,</p>
    <ul>
      <li>추상 클래스는 “공통된 속성과 기본 구현을 나누는 상위 클래스”에 가깝고, 한 클래스만 상속할 수 있으며,</li>
      <li>인터페이스는 “구현해야 할 동작의 규약”에 가깝고, 여러 개를 동시에 구현할 수 있습니다.</li>
    </ul>
    <p>실제 설계에서는 상속 관계로 강하게 묶고 공통 구현을 공유해야 하면 추상 클래스를, 타입 계층과는 별개로 여러 클래스에 공통으로 적용할 수 있는 규약을 정의하고 싶을 때는 인터페이스를 선택하는 편입니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q8. 컬렉션 프레임워크의 주요 인터페이스들을 설명해주세요.</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
  <div class="accordion-content">
    <p>자바 컬렉션 프레임워크의 주요 인터페이스는 List, Set, Map, 그리고 그 상위 개념인 Collection 정도로 정리해서 이해하고 있습니다.</p>
    <p>먼저 가장 상위에는 Collection 인터페이스가 있고, 여기에서 add, remove, size 같은 공통적인 자료구조 동작을 정의합니다. List, Set, Queue 같은 인터페이스들이 이 Collection을 기반으로 특화된 형태로 확장됩니다. (참고로 Map은 구조가 달라서 Collection을 상속받지는 않습니다.)</p>
    <p>그 아래에서 List 인터페이스는 순서가 있는 데이터 집합을 표현합니다. 인덱스로 요소에 접근할 수 있고, 중복을 허용합니다. ArrayList, LinkedList 같은 구현체들이 있고, 순서가 중요하거나 같은 값을 여러 번 저장해야 할 때 사용합니다.</p>
    <p>Set 인터페이스는 중복을 허용하지 않는 집합 구조입니다. 요소의 유일성이 중요할 때 사용하고, 구현체에 따라 정렬 여부가 달라집니다. 예를 들어 HashSet은 순서를 보장하지 않고, LinkedHashSet은 입력 순서를, TreeSet은 정렬 순서를 유지합니다.</p>
    <p>Queue 인터페이스는 선입선출(FIFO) 구조를 표현하고, 주로 작업 대기열이나 버퍼처럼 순서대로 처리해야 하는 데이터에 사용됩니다. LinkedList, PriorityQueue 등이 대표적인 구현체입니다.</p>
    <p>마지막으로 Map 인터페이스는 키-값 쌍으로 데이터를 저장하는 구조입니다. 키는 중복될 수 없고, 값은 중복을 허용합니다. 키로 값을 빠르게 조회하는 것이 목적일 때 사용하고, HashMap, LinkedHashMap, TreeMap 같은 구현체가 있습니다.</p>
    <p>정리하면, Collection은 공통적인 자료구조 동작을 모아둔 상위 개념이고, 그 아래에서 List는 순서가 있고 중복을 허용하는 구조, Set은 중복을 허용하지 않는 집합 구조, Queue는 먼저 들어온 걸 먼저 처리하는 대기열 구조라고 이해하고 있습니다. 그리고 Map은 컬렉션 계열과는 조금 다르게, 키-값 쌍으로 데이터를 저장하면서 키로 빠르게 값을 조회할 때 사용하는 구조라고 정리해서 기억하고 있습니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q9. ArrayList와 LinkedList의 차이점은?</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
  <div class="accordion-content">
    <p>ArrayList와 LinkedList의 차이는 내부 자료구조와 그로 인한 성능 특성으로 구분해서 이해하고 있습니다.</p>
    <p>먼저 ArrayList는 배열 기반의 리스트입니다. 내부적으로 연속된 메모리 공간을 사용하기 때문에 인덱스로 접근할 때 O(1)에 가까운 시간에 아주 빠르게 접근할 수 있습니다. 그 대신 중간에 요소를 삽입하거나 삭제할 때는 뒤에 있는 요소들을 한 칸씩 밀거나 당겨야 해서 중간 삽입·삭제 비용이 상대적으로 큰 편입니다. 조회 위주이고, 주로 뒤에 추가하는 작업이 많을 때 적합해서 일반적인 상황에서 가장 많이 사용하는 리스트 구현체라고 생각합니다.</p>
    <p>반면에 LinkedList는 이중 연결 리스트 구조입니다. 각 노드가 이전 노드와 다음 노드를 가리키기 때문에, 어떤 위치를 이미 알고 있다는 전제하에서는 해당 위치에서의 삽입·삭제 자체는 O(1)에 가깝게 처리할 수 있습니다. 하지만 특정 인덱스를 찾기 위해서는 앞이나 뒤에서부터 차례대로 타고 들어가야 해서 인덱스 기반 접근과 검색은 O(n)으로 느린 편이고, 노드마다 포인터를 저장해야 해서 메모리 오버헤드와 캐시 효율 측면에서도 ArrayList보다 불리합니다.</p>
    <p>정리하면, 조회가 많고 인덱스로 자주 접근하는 경우에는 ArrayList를 우선적으로 선택하는 편이고, 특정 위치에서의 삽입·삭제가 자주 일어나고 리스트 크기가 아주 크지 않은 경우에는 LinkedList를 고려하는 것이 일반적인 기준이라고 생각합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q10. HashMap과 TreeMap의 차이점은?</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
  <div class="accordion-content">
    <p>HashMap과 TreeMap의 차이는 내부 자료구조, 정렬 여부, 성능 특성 관점에서 정리해서 설명할 수 있습니다.</p>
    <p>먼저 HashMap은 해시 테이블 기반의 Map입니다. 키의 hashCode()를 사용해서 버킷 위치를 계산하고, 그 위치에 값을 저장하는 방식이라서 평균적으로 put, get 연산이 O(1)에 가깝게 매우 빠릅니다. 다만 해시값을 기준으로 저장되기 때문에 키의 순서를 보장하지 않고, 순회할 때의 순서도 예측할 수 없습니다. 그리고 보통은 null 키 1개, null 값 여러 개를 허용합니다. 그래서 정렬이 필요 없고, 빠른 조회/삽입이 중요한 일반적인 케이스에서 가장 많이 사용하는 구현체라고 생각합니다.</p>
    <p>반면에 TreeMap은 이진 검색 트리(구체적으로는 레드-블랙 트리) 기반의 Map입니다. 키를 정렬 기준(자연 순서 또는 Comparator)에 따라 오름차순으로 정렬해서 저장합니다. 이 때문에 put, get, remove 같은 연산의 시간 복잡도는 **O(log n)**으로 HashMap보다는 느리지만, 항상 정렬된 상태를 유지하기 때문에 범위 조회(subMap, headMap, tailMap)나 정렬된 순서로 순회할 때 강점이 있습니다. 또한 키를 정렬해야 하기 때문에 키 타입이 Comparable을 구현하거나, 생성 시 Comparator를 제공해야 하고, null 키는 허용하지 않는 것이 일반적인 구현입니다.</p>
    <p>정리하자면, 정렬이 필요 없고 성능이 가장 중요하면 HashMap을 우선적으로 선택하고, 키의 정렬 순서가 중요하거나 범위 검색이 자주 발생하는 경우에는 TreeMap을 사용하는 것이 적합하다고 생각합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q11. 예외 처리에서 Checked Exception과 Unchecked Exception의 차이점은?</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
  <div class="accordion-content">
    <p>예외 처리에서 Checked Exception과 Unchecked Exception의 차이는 예외 처리가 컴파일 시점에 강제되느냐, 그리고 언제 주로 발견되느냐로 설명할 수 있습니다.</p>
    <p>먼저 Checked Exception은 컴파일 시점에 “이 예외를 꼭 처리해라”라고 강제되는 예외입니다. IOException, SQLException 같은 것들이 대표적이고, 이런 메서드를 호출할 때는 반드시 try-catch로 잡거나, 메서드 선언부에 throws로 던진다고 명시해야 합니다. 보통 파일 접근, DB 접근처럼 외부 자원과의 통신 과정에서 충분히 예상 가능한 예외들을 Checked로 두고, 컴파일 단계에서부터 처리하도록 강제하는 개념입니다.</p>
    <p>반면에 Unchecked Exception은 흔히 말하는 런타임 예외로, 처리가 강제되지는 않습니다. RuntimeException을 상속하는 예외들이고, NullPointerException, ArrayIndexOutOfBoundsException처럼 주로 프로그래머의 실수나 논리 오류에서 발생하는 것들입니다. 이런 예외들은 모든 곳에 일일이 try-catch를 강제하기보다는, 코드 자체를 수정해서 예방하거나, 필요한 경우에만 상위 레벨에서 한 번에 처리하는 방식으로 다룹니다.</p>
    <p>정리해서 말하면, Checked Exception은 컴파일 시점에 예외 처리를 반드시 요구하는 예외이고, Unchecked Exception은 런타임에 발생하지만 개발자가 선택적으로 처리할 수 있는 예외라고 이해하고 있습니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q12. 가비지 컬렉션(Garbage Collection)이란 무엇인가요?</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
  <div class="accordion-content">
    <p>가비지 컬렉션은 JVM이 더 이상 사용되지 않는 객체들을 자동으로 찾아서 메모리에서 정리해 주는 메커니즘입니다. 자바에서는 개발자가 new로 객체를 만들기만 하고, 그 객체를 더 이상 참조하지 않게 되면, JVM의 가비지 컬렉터가 그 객체를 “쓸모없는 쓰레기”로 판단하고 메모리를 회수합니다.</p>
    <p>JVM 힙 메모리는 보통 Young Generation과 Old Generation으로 나뉘어 관리되고, 새로 생성된 객체는 Young 쪽에 먼저 들어갑니다. Young 영역에서 필요 없어진 객체들을 치우는 작업을 Minor GC, 오래 살아남아 Old 영역으로 올라간 객체들까지 대상으로 하는 큰 단위 수집을 Major GC 또는 Full GC라고 부릅니다.</p>
    <p>이 덕분에 자바 개발자는 C처럼 메모리를 일일이 해제하지 않아도 된다는 큰 장점이 있지만, 가비지 컬렉션이 실행되는 순간에는 Stop-the-world라고 해서 애플리케이션이 잠깐 멈출 수 있다는 비용도 있습니다. 그래서 실무에서는 이 자동 메모리 관리가 주는 편리함을 활용하면서도, 멈춤 시간을 줄이기 위해 GC 방식이나 힙 크기를 튜닝하는 작업이 중요해집니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q13. 스레드(Thread)와 프로세스(Process)의 차이점은?</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
  <div class="accordion-content">
    <p>스레드와 프로세스의 차이는 보통 독립성이랑 자원 공유 범위로 나눠서 이야기할 수 있을 것 같습니다.</p>
    <p>먼저 프로세스는 운영체제 입장에서 보면 “실행 중인 프로그램 하나”이고, 각각 독립된 메모리 공간을 가진 실행 단위입니다. 서로 다른 프로세스들은 기본적으로 메모리를 직접 공유하지 않기 때문에 한 프로세스가 죽어도 다른 프로세스에 바로 영향을 주지는 않지만, 대신 서로 데이터를 주고받으려면 IPC 같은 별도의 방법이 필요하고 전환 비용도 상대적으로 큰 편입니다.</p>
    <p>반대로 스레드는 하나의 프로세스 안에서 돌아가는 더 작은 실행 흐름 단위입니다. 같은 프로세스에 속한 스레드들은 힙이나 데이터 영역 같은 메모리를 서로 공유하고, 각자 스택만 따로 가지고 있어서 생성·전환 비용이 더 가볍습니다. 그래서 한 프로그램 안에서 여러 작업을 동시에 처리할 때 많이 쓰지만, 공유 자원을 잘못 다루면 경쟁 조건이나 데드락 같은 문제가 생길 수 있고, 한 스레드가 치명적인 오류를 내면 프로세스 전체에 영향을 줄 수 있다는 단점도 있습니다.</p>
    <p>정리해서 말하면, 프로세스는 서로 격리된 무거운 실행 단위, 스레드는 한 프로세스 안에서 자원을 공유하면서 병렬로 일하는 가벼운 실행 단위라고 이해하고 있습니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q14. synchronized 키워드의 역할과 사용법은?</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
  <div class="accordion-content">
    <p>synchronized 키워드는 멀티스레드 환경에서 공유 자원에 대한 동시 접근을 제어하기 위해 사용하는 키워드라고 이해하고 있습니다. 즉, 한 번에 하나의 스레드만 특정 코드 블록을 실행하도록 막아서 원자성 보장과 메모리 일관성을 확보하는 역할을 합니다.</p>
    <p>조금 더 구체적으로 보면, synchronized는 모니터 락(내부 락, intrinsic lock) 을 사용합니다. 어떤 객체에 대해 synchronized가 걸리면, 해당 객체의 락을 먼저 획득한 스레드만 그 블록을 실행할 수 있고, 다른 스레드는 락이 풀릴 때까지 대기하게 됩니다. 이 과정에서 단순히 “한 번에 하나만 들어간다”는 상호 배제뿐 아니라, 락을 획득·해제하는 시점에 메모리 가시성(visibility) 도 보장되어, 한 스레드가 변경한 값을 다른 스레드가 제대로 볼 수 있게 해줍니다.</p>
    <p>사용법은 크게 두 가지로 정리할 수 있습니다.</p>
    <p>첫째, 메서드 전체에 synchronized를 붙이는 방법입니다.</p>
    <ul>
      <li>public synchronized void method() 형태로 선언하면, 해당 인스턴스(this)에 대한 락을 기준으로 메서드 전체가 임계 구역이 됩니다.</li>
      <li>static synchronized 메서드의 경우에는 클래스 객체(Class)에 대한 락을 사용합니다.</li>
    </ul>
    <p>둘째, synchronized 블록을 사용하는 방법입니다.</p>
    <ul>
      <li>synchronized(lockObject) { ... } 형태로, 임계 구역을 감싸고 싶은 부분만 선택적으로 잠글 수 있습니다.</li>
      <li>이 방식은 락으로 사용할 객체를 명시적으로 고를 수 있고, 필요한 최소한의 범위에만 락을 걸 수 있어서 성능과 설계 측면에서 더 유연합니다.</li>
    </ul>
    <p>정리하면, synchronized는 멀티스레드 환경에서 공유 자원을 안전하게 보호하기 위한 가장 기본적인 동기화 메커니즘이고, 메서드나 블록에 적용해서 한 시점에 하나의 스레드만 접근하도록 보장합니다. 다만, 과도한 사용은 락 경합이나 데드락 같은 문제를 유발할 수 있기 때문에, 상황에 따라 java.util.concurrent 패키지의 Lock, 동시 컬렉션 등과 함께 적절히 선택하는 것이 중요하다고 생각합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q15. final, finally, finalize의 차이점은?</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
  <div class="accordion-content">
    <p>final, finally, finalize는 이름은 비슷하지만 역할과 쓰이는 위치가 완전히 다른 세 가지라고 이해하고 있습니다.</p>
    <p>먼저 final은 키워드이고, 변수·메서드·클래스에 붙여서 변경을 제한할 때 사용합니다.</p>
    <ul>
      <li>final 변수는 한 번 초기화되면 다시 다른 값으로 재할당할 수 없고,</li>
      <li>final 메서드는 상속받은 클래스에서 오버라이딩할 수 없으며,</li>
      <li>final 클래스는 다른 클래스가 상속(extends)할 수 없습니다.</li>
    </ul>
    <p>즉, final은 “이건 더 이상 바뀌면 안 된다”는 수정 금지 의도를 명확히 하는 키워드라고 생각합니다.</p>
    <p>finally는 예외 처리에서 사용하는 블록입니다. try-catch-finally 구조에서 finally 블록은 예외가 발생하든 안 하든, 그리고 예외를 잡았든 못 잡았든 거의 항상 실행되는 영역입니다. 주로 파일 닫기, 소켓 종료, DB 커넥션 반납 같은 자원 정리 코드를 넣는 용도로 사용합니다. (강제 종료 같은 특수한 경우를 제외하면 실행된다고 이해하고 있습니다.)</p>
    <p>마지막으로 finalize()는 Object 클래스에 정의된 메서드로, 가비지 컬렉터가 객체를 실제로 회수하기 전에 한 번 호출될 수 있는 훅(hook)입니다. 다만 호출 시점이 언제, 실제로 호출될지조차 보장되지 않기 때문에 자원 정리 용도로 사용하는 것은 권장되지 않고, 최근 자바에서는 사실상 사용이 deprecated된 개념입니다. 실제 코드에서는 finalize() 대신 try-with-resources나 명시적인 close() 호출로 자원을 정리하는 것이 일반적입니다.</p>
    <p>정리하면,</p>
    <ul>
      <li>final은 수정/확장을 막는 키워드,</li>
      <li>finally는 예외 처리에서 항상 실행되는 정리용 블록,</li>
      <li>finalize()는 GC 직전에 호출될 수 있는 메서드지만, 현재는 거의 사용하지 않는 방식이라고 정리할 수 있습니다.</li>
    </ul>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q16. static 키워드의 특징과 사용 용도는?</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
  <div class="accordion-content">
    <p>static 키워드는 “인스턴스가 아니라 클래스 자체에 속하는 멤버”를 정의할 때 사용하는 키워드라고 이해하고 있습니다. 즉, 객체를 여러 개 만들어도 각 객체가 따로 가지는 것이 아니라 클래스 차원에서 하나만 공유되는 멤버를 만들 때 사용합니다.</p>
    <p>먼저 특징부터 말씀드리면,</p>
    <ul>
      <li>static으로 선언된 변수와 메서드는 클래스 로딩 시점에 함께 메모리에 올라가고, 인스턴스를 생성하지 않아도 클래스이름.변수, 클래스이름.메서드() 형태로 바로 접근할 수 있습니다.</li>
      <li>모든 인스턴스가 하나의 static 변수 값을 공유하기 때문에, 공용 카운터나 설정 값처럼 객체들 사이에서 공통으로 사용하는 상태를 표현할 때 적합합니다.</li>
      <li>반대로 인스턴스에 종속되지 않기 때문에, static 메서드 안에서는 인스턴스 필드나 인스턴스 메서드에 바로 접근할 수 없고, this 키워드도 사용할 수 없습니다.</li>
    </ul>
    <p>사용 용도로는 크게 세 가지 정도로 정리합니다. 첫째, 상수와 공용 변수입니다. 예를 들어 public static final로 선언된 상수처럼, 모든 곳에서 공유하며 변하지 않는 값을 정의할 때 사용합니다.</p>
    <p>둘째, 유틸리티성 메서드입니다. 특정 객체 상태와 상관없이 입력만 주어지면 항상 같은 작업을 하는 함수들은 굳이 인스턴스를 만들 필요가 없기 때문에 static 메서드로 두는 편입니다. 대표적으로 Math.random(), Collections.sort() 같은 형태가 있습니다. 자바의 main 메서드도 프로그램 시작을 위해 인스턴스 없이 호출해야 해서 static으로 선언됩니다.</p>
    <p>셋째, 클래스 단위의 공용 기능입니다. 예를 들어 생성된 인스턴스 개수를 세는 카운터나, 싱글톤에서 getInstance() 같은 메서드처럼 클래스 전체에서 하나만 관리해야 하는 데이터나 로직을 표현할 때 사용합니다.</p>
    <p>정리하면, static은 “객체가 아니라 클래스 수준에서 하나만 존재해야 하는 값이나 메서드”를 정의할 때 사용하는 키워드이고, 인스턴스와 무관한 공용 상태나 공용 기능에 한정해서 사용하는 것이 바람직하다고 생각합니다.</p>
  </div>
</details>

  </div>
</details>

<details>
  <summary><span class="accordion-title">💡 추가 예상 질문 Q&A</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">
<details>
  <summary style="font-size:1rem;"><b>Q17. 자바의 메모리 구조를 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p>JVM 메모리는 크게 &lt;b&gt;메서드 영역&lt;/b&gt;, &lt;b&gt;힙 영역&lt;/b&gt;, &lt;b&gt;스택 영역&lt;/b&gt;으로 구성됩니다. 메서드 영역은 클래스 정보, static 변수, 상수 풀을 저장합니다. 힙 영역은 객체와 인스턴스 변수를 저장하며 가비지 컬렉션의 대상입니다. 스택 영역은 메서드 호출 시마다 프레임을 생성하여 지역 변수와 매개변수를 저장합니다. PC 레지스터는 현재 실행 중인 명령어의 주소를, 네이티브 메서드 스택은 JNI로 호출하는 네이티브 메서드를 위한 공간입니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q18. equals()와 hashCode()의 관계는?</b></summary>
  <div class="accordion-content">
    <p>equals()와 hashCode()는 객체의 동등성을 판단하는 메서드로 함께 재정의해야 합니다. &lt;b&gt;equals() 계약&lt;/b&gt;: 반사적(reflexive), 대칭적(symmetric), 이행적(transitive), 일관적(consistent), null과 비교 시 false를 만족해야 합니다. &lt;b&gt;hashCode() 계약&lt;/b&gt;: equals()가 true인 객체들은 같은 hashCode 값을 가져야 하며, equals()가 false인 객체들도 가능한 다른 hashCode 값을 가져야 합니다. HashMap 등에서 성능에 직접적인 영향을 미칩니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q19. 자바 8의 주요 특징들을 설명해주세요.</b></summary>
  <div class="accordion-content">
    <b>람다 표현식</b>: 함수형 프로그래밍을 지원하여 코드를 더 간결하게 작성할 수 있습니다. <b>스트림 API</b>: 컬렉션 데이터를 함수형으로 처리할 수 있는 API를 제공합니다. <b>메서드 참조</b>: 기존 메서드를 람다 표현식처럼 사용할 수 있습니다. <b>디폴트 메서드</b>: 인터페이스에 구현체가 있는 메서드를 추가할 수 있어 하위 호환성을 유지합니다. <b>Optional</b>: null 처리를 더 안전하게 할 수 있는 컨테이너 클래스입니다. <b>새로운 날짜/시간 API</b>: LocalDate, LocalTime 등으로 기존 Date/Calendar의 문제점을 해결했습니다.
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q20. 직렬화(Serialization)란 무엇인가요?</b></summary>
  <div class="accordion-content">
    <p>직렬화는 자바 객체를 바이트 스트림으로 변환하는 과정이고, 역직렬화는 그 반대 과정입니다. Serializable 인터페이스를 구현하면 ObjectOutputStream/ObjectInputStream을 통해 직렬화할 수 있습니다. &lt;b&gt;serialVersionUID&lt;/b&gt;: 클래스의 버전을 나타내는 값으로, 역직렬화 시 호환성을 확인합니다. &lt;b&gt;transient&lt;/b&gt;: 직렬화에서 제외할 필드에 사용하는 키워드입니다. 네트워크 전송, 파일 저장, 캐싱 등에 활용되지만, 보안과 성능 측면에서 주의가 필요합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q21. 리플렉션(Reflection)이란 무엇인가요?</b></summary>
  <div class="accordion-content">
    <p>리플렉션은 런타임에 클래스의 정보를 동적으로 가져오거나 조작할 수 있는 기능입니다. Class.forName(), getClass() 등으로 클래스 정보를 얻을 수 있고, getDeclaredFields(), getDeclaredMethods() 등으로 필드와 메서드 정보를 조회할 수 있습니다. private 멤버에도 접근 가능하며, 동적으로 객체를 생성하거나 메서드를 호출할 수 있습니다. 프레임워크에서 많이 사용되지만, 성능 저하와 보안 문제가 있을 수 있습니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q22. 자바의 제네릭(Generics)을 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p>제네릭은 클래스나 메서드에서 사용할 타입을 컴파일 시점에 미리 지정하는 기능입니다. &lt;b&gt;타입 안전성&lt;/b&gt;: 컴파일 시점에 타입 검사를 수행하여 ClassCastException을 방지합니다. &lt;b&gt;형변환 제거&lt;/b&gt;: 명시적인 형변환이 불필요합니다. &lt;b&gt;코드 재사용&lt;/b&gt;: 하나의 코드로 여러 타입에 대응할 수 있습니다. &lt;b&gt;와일드카드&lt;/b&gt;: `&lt;?&gt;`, `&lt;? extends T&gt;`, `&lt;? super T&gt;`를 통해 유연성을 제공합니다. &lt;b&gt;타입 소거&lt;/b&gt;: 런타임에는 제네릭 타입 정보가 제거되어 하위 호환성을 유지합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q23. 어노테이션(Annotation)의 개념과 활용법은?</b></summary>
  <div class="accordion-content">
    <p>어노테이션은 소스코드에 메타데이터를 추가하는 방법으로, 컴파일러에게 정보를 제공하거나 런타임에 특별한 처리를 할 수 있게 합니다. &lt;b&gt;빌트인 어노테이션&lt;/b&gt;: @Override, @Deprecated, @SuppressWarnings 등이 있습니다. &lt;b&gt;메타 어노테이션&lt;/b&gt;: @Retention, @Target, @Documented, @Inherited 등으로 사용자 정의 어노테이션을 만들 수 있습니다. 스프링의 @Controller, @Service, JPA의 @Entity 등 프레임워크에서 광범위하게 활용됩니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q24. 멀티스레딩에서 발생할 수 있는 문제들과 해결방법은?</b></summary>
  <div class="accordion-content">
    <b>Race Condition</b>: 여러 스레드가 공유 자원에 동시 접근할 때 발생하며, synchronized나 Lock을 사용하여 해결합니다. <b>Deadlock</b>: 두 개 이상의 스레드가 서로의 락을 기다리며 무한 대기하는 상황으로, 락 순서를 정하거나 타임아웃을 설정하여 방지합니다. <b>Starvation</b>: 특정 스레드가 계속 자원을 할당받지 못하는 상황으로, 공정한 스케줄링을 사용합니다. <b>Live Lock</b>: 스레드들이 서로를 의식하여 계속 상태를 바꾸며 진전이 없는 상황입니다.
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q25. 자바의 입출력 스트림을 설명해주세요.</b></summary>
  <div class="accordion-content">
    <p>자바의 I/O는 스트림 기반으로 동작하며, &lt;b&gt;바이트 스트림&lt;/b&gt;(InputStream/OutputStream)과 &lt;b&gt;문자 스트림&lt;/b&gt;(Reader/Writer)으로 구분됩니다. &lt;b&gt;Buffer 클래스&lt;/b&gt;: BufferedInputStream, BufferedReader 등은 내부 버퍼를 사용하여 성능을 향상시킵니다. &lt;b&gt;Data 클래스&lt;/b&gt;: DataInputStream, DataOutputStream은 기본 타입 데이터를 읽고 쓸 수 있습니다. &lt;b&gt;Object 클래스&lt;/b&gt;: ObjectInputStream, ObjectOutputStream은 객체 직렬화/역직렬화를 지원합니다. &lt;b&gt;NIO&lt;/b&gt;: New I/O는 채널과 버퍼 기반으로 더 효율적인 I/O를 제공합니다.</p>
  </div>
</details>

  </div>
</details>

<details>
  <summary><span class="accordion-title">📚 자바 개념 요약 노트</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">
    <h3>🏗 기본 개념</h3>
    <h4>자바 플랫폼</h4>
    <ul>
    <li><b>JVM</b>: 바이트코드 실행 환경</li>
    <li><b>JRE</b>: JVM + 실행 라이브러리</li>
    <li><b>JDK</b>: JRE + 개발 도구</li>
    </ul>
    <h4>데이터 타입</h4>
    <ul>
    <li><b>기본 타입</b>: byte, short, int, long, float, double, char, boolean</li>
    <li><b>참조 타입</b>: 배열, 클래스, 인터페이스, 열거형</li>
    </ul>
    <h4>메모리 구조</h4>
    <ul>
    <li><b>메서드 영역</b>: 클래스 정보, static 변수</li>
    <li><b>힙 영역</b>: 객체, 인스턴스 변수</li>
    <li><b>스택 영역</b>: 지역 변수, 메서드 매개변수</li>
    <li><b>PC 레지스터</b>: 현재 실행 명령어 주소</li>
    <li><b>네이티브 메서드 스택</b>: JNI 메서드</li>
    </ul>
    <h3>⚙️ 객체지향</h3>
    <h4>4대 특징</h4>
    <ul>
    <li><b>캡슐화</b>: 데이터 은닉, 접근 제한자</li>
    <li><b>상속</b>: extends, 코드 재사용</li>
    <li><b>다형성</b>: 오버로딩/오버라이딩, 업캐스팅</li>
    <li><b>추상화</b>: abstract, interface</li>
    </ul>
    <h4>접근 제한자</h4>
    <ul>
    <li><b>private</b>: 클래스 내부만</li>
    <li><b>default</b>: 패키지 내부만  </li>
    <li><b>protected</b>: 패키지 + 상속 관계</li>
    <li><b>public</b>: 모든 곳</li>
    </ul>
    <h4>클래스 관계</h4>
    <ul>
    <li><b>상속</b>: IS-A 관계 (extends)</li>
    <li><b>구현</b>: 인터페이스 구현 (implements)</li>
    <li><b>포함</b>: HAS-A 관계 (멤버 변수)</li>
    </ul>
    <h3>📦 컬렉션 프레임워크</h3>
    <h4>계층 구조</h4>
    <pre><code>Collection
    ├── List (순서O, 중복O)
    │   ├── ArrayList (배열 기반)
    │   ├── LinkedList (노드 기반)
    │   └── Vector (동기화)
    ├── Set (순서X, 중복X)
    │   ├── HashSet (해시 테이블)
    │   ├── TreeSet (정렬)
    │   └── LinkedHashSet (입력 순서)
    └── Queue (FIFO)
        ├── LinkedList
        └── PriorityQueue (우선순위)
    </pre></code>
    <pre><code>Map (키-값 쌍)
    ├── HashMap (해시 테이블)
    ├── TreeMap (정렬)
    ├── LinkedHashMap (입력 순서)
    └── Hashtable (동기화)
    </pre></code>
    <h4>성능 비교</h4>
    <table>
    <thead><tr><th>구분</th><th>검색</th><th>삽입/삭제</th><th>정렬</th><th>동기화</th></tr></thead>
    <tbody>
    <tr><td>ArrayList</td><td>O(1)</td><td>O(n)</td><td>수동</td><td>X</td></tr>
    <tr><td>LinkedList</td><td>O(n)</td><td>O(1)</td><td>수동</td><td>X</td></tr>
    <tr><td>HashMap</td><td>O(1)</td><td>O(1)</td><td>X</td><td>X</td></tr>
    <tr><td>TreeMap</td><td>O(log n)</td><td>O(log n)</td><td>O</td><td>X</td></tr>
    </tbody>
    </table>
    <h3>🧵 동시성</h3>
    <h4>스레드 생성</h4>
    <ul>
    <li><b>Thread 상속</b>: class MyThread extends Thread</li>
    <li><b>Runnable 구현</b>: class MyTask implements Runnable</li>
    <li><b>람다 표현식</b>: new Thread(() -&gt; {...}).start()</li>
    </ul>
    <h4>동기화 방법</h4>
    <ul>
    <li><b>synchronized</b>: 메서드/블록 동기화</li>
    <li><b>volatile</b>: 가시성 보장</li>
    <li><b>Lock</b>: 명시적 락 제어</li>
    <li><b>Atomic</b>: 원자적 연산</li>
    </ul>
    <h4>스레드 상태</h4>
    <ul>
    <li>NEW → RUNNABLE → WAITING/BLOCKED → TERMINATED</li>
    </ul>
    <h3>💾 메모리 관리</h3>
    <h4>가비지 컬렉션</h4>
    <ul>
    <li><b>Young Generation</b>: Eden, Survivor0, Survivor1</li>
    <li><b>Old Generation</b>: Tenured</li>
    <li><b>Permanent</b>: 클래스 메타데이터 (Java 8+에서 Metaspace)</li>
    </ul>
    <h4>GC 종류</h4>
    <ul>
    <li><b>Minor GC</b>: Young Generation 대상</li>
    <li><b>Major GC</b>: Old Generation 대상  </li>
    <li><b>Full GC</b>: 전체 힙 대상</li>
    </ul>
    <h3>📝 예외 처리</h3>
    <h4>예외 계층</h4>
    <pre><code>Throwable
    ├── Error (시스템 오류)
    └── Exception
        ├── Checked Exception (컴파일 시 확인)
        └── RuntimeException (실행 시 발생)
    </code></pre>
    <h4>처리 방법</h4>
    <ul>
    <li><b>try-catch</b>: 예외 처리</li>
    <li><b>throws</b>: 예외 전파</li>
    <li><b>finally</b>: 정리 코드</li>
    <li><b>try-with-resources</b>: 자동 자원 해제</li>
    </ul>
    <h3>🔧 자바 8+ 특징</h3>
    <h4>함수형 프로그래밍</h4>
    <ul>
    <li><b>람다</b>: (parameter) -&gt; expression</li>
    <li><b>메서드 참조</b>: Class::method</li>
    <li><b>함수형 인터페이스</b>: @FunctionalInterface</li>
    </ul>
    <h4>스트림 API</h4>
    <pre><code class="language-java">list.stream()
        .filter(x -&gt; x &gt; 10)
        .map(x -&gt; x * 2)
        .collect(Collectors.toList());
    </code></pre>
    <h4>Optional</h4>
    <ul>
    <li><b>생성</b>: Optional.of(), Optional.empty()</li>
    <li><b>확인</b>: isPresent(), isEmpty()</li>
    <li><b>처리</b>: orElse(), orElseThrow()</li>
    </ul>
    <h3>🎯 성능 최적화</h3>
    <h4>문자열 처리</h4>
    <ul>
    <li>단순 연결: String</li>
    <li>동기화 필요: StringBuffer</li>
    <li>단일 스레드: StringBuilder</li>
    </ul>
    <h4>컬렉션 선택</h4>
    <ul>
    <li>빠른 검색: HashMap</li>
    <li>정렬 필요: TreeMap  </li>
    <li>순서 유지: LinkedHashMap</li>
    <li>스레드 안전: ConcurrentHashMap</li>
    </ul>
    <h4>메모리 최적화</h4>
    <ul>
    <li><b>불변 객체</b>: 캐시 활용 가능</li>
    <li><b>지연 초기화</b>: 필요 시점에 생성</li>
    <li><b>약한 참조</b>: WeakReference 사용</li>
    <li><b>풀링</b>: 객체 재사용</li>
    </ul>
    <h3>💡 면접 팁</h3>
    <ol>
    <li><b>기본기 탄탄히</b>: OOP 4원칙과 자바 기본 문법 완벽 숙지</li>
    <li><b>예시 코드</b>: 설명과 함께 간단한 코드 작성 능력 보여주기</li>
    <li><b>실무 경험</b>: 프로젝트에서 사용한 라이브러리나 패턴 언급</li>
    <li><b>성능 고려</b>: 시간복잡도와 메모리 사용량 분석</li>
    <li><b>최신 동향</b>: 자바 8+ 특징과 스프링 생태계 이해</li>
    <li><b>트러블슈팅</b>: 실제 겪은 문제와 해결 과정 준비</li>
    </ol>
  </div>
</details>
