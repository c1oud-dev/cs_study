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
    <p>자바는 객체지향 프로그래밍 언어로, 플랫폼 독립성, 메모리 관리 자동화, 멀티스레딩 지원이 주요 특징입니다. &quot;Write Once, Run Anywhere&quot;의 철학으로 JVM을 통해 어떤 운영체제에서든 실행 가능합니다. 가비지 컬렉터가 자동으로 메모리를 관리하며, 강력한 타입 검사와 예외 처리 메커니즘을 제공합니다. 풍부한 API와 라이브러리, 대규모 커뮤니티 지원도 큰 장점입니다.</p>
  </div>
</details>
<details>

  <summary style="font-size:1rem;"><b>Q2. JVM, JRE, JDK의 차이점을 설명해주세요.</b>
    <span style="float:right;">🟩🟩🟩🟩🟩</span>
  </summary>
  <div class="accordion-content">
    <p>JVM(Java Virtual Machine)은 자바 바이트코드를 실행하는 실행 환경입니다. JRE(Java Runtime Environment)는 JVM + 자바 실행에 필요한 라이브러리들의 집합으로, 자바 애플리케이션을 실행만 하려면 충분합니다. JDK(Java Development Kit)는 JRE + 컴파일러(javac), 디버거 등 개발 도구들을 포함한 개발 키트입니다. 즉, JDK ⊃ JRE ⊃ JVM의 포함 관계입니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q3. 객체지향 프로그래밍의 4대 특징을 설명해주세요.</b>
    <span style="float:right;">🟩🟩🟩🟩🟩</span>
  </summary>
  <div class="accordion-content">
    <b>캡슐화(Encapsulation)</b>: 데이터와 메서드를 하나로 묶고 외부에서의 접근을 제한하는 것입니다. private, protected, public 접근 제한자를 사용합니다. <b>상속(Inheritance)</b>: 기존 클래스의 속성과 메서드를 새로운 클래스가 물려받는 것으로, extends 키워드를 사용합니다. <b>다형성(Polymorphism)</b>: 같은 이름의 메서드가 다른 클래스에서 다른 기능을 수행하는 것으로, 오버로딩과 오버라이딩으로 구현됩니다. <b>추상화(Abstraction)</b>: 복잡한 구현 내용을 숨기고 필요한 기능만 노출하는 것으로, abstract 클래스나 interface를 통해 구현합니다.
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q4. String, StringBuffer, StringBuilder의 차이점은?</b></summary>
  <div class="accordion-content">
    <b>String</b>: 불변(immutable) 객체로, 문자열 수정 시마다 새로운 객체가 생성됩니다. 메모리 낭비가 발생할 수 있습니다. <b>StringBuffer</b>: 가변(mutable) 객체로 내부 버퍼에서 문자열을 수정합니다. 동기화(synchronized)되어 있어 스레드 안전하지만 성능이 느립니다. <b>StringBuilder</b>: StringBuffer와 동일하게 가변 객체이지만 동기화되지 않아 단일 스레드 환경에서 더 빠른 성능을 제공합니다. 문자열 연산이 많은 경우 StringBuilder 사용을 권장합니다.
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q5. 접근 제한자(Access Modifier)의 종류와 특징은?</b></summary>
  <div class="accordion-content">
    <b>private</b>: 같은 클래스 내에서만 접근 가능합니다. <b>default(package-private)</b>: 같은 패키지 내에서만 접근 가능하며, 접근 제한자를 명시하지 않으면 기본값입니다. <b>protected</b>: 같은 패키지 또는 상속받은 자식 클래스에서 접근 가능합니다. <b>public</b>: 어떤 클래스에서든 접근 가능합니다. 접근 범위는 private < default < protected < public 순서입니다.
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q6. 오버로딩(Overloading)과 오버라이딩(Overriding)의 차이점은?</b></summary>
  <div class="accordion-content">
    <b>오버로딩</b>: 같은 클래스 내에서 메서드 이름은 같지만 매개변수의 타입, 개수, 순서가 다른 여러 메서드를 정의하는 것입니다. 컴파일 시간에 결정됩니다. <b>오버라이딩</b>: 상속받은 부모 클래스의 메서드를 자식 클래스에서 재정의하는 것입니다. @Override 어노테이션을 사용하며 런타임에 결정됩니다. 메서드 시그니처(이름, 매개변수)가 동일해야 합니다.
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q7. 추상 클래스(Abstract Class)와 인터페이스(Interface)의 차이점은?</b></summary>
  <div class="accordion-content">
    <b>추상 클래스</b>: abstract 키워드로 선언하며, 추상 메서드와 일반 메서드를 모두 가질 수 있습니다. 생성자와 인스턴스 변수를 가질 수 있고, 단일 상속만 가능합니다. <b>인터페이스</b>: interface 키워드로 선언하며, 기본적으로 모든 메서드가 추상 메서드입니다(Java 8+에서는 default, static 메서드 가능). 상수만 선언할 수 있고, 다중 구현이 가능합니다. 완전한 추상화를 제공합니다.
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q8. 컬렉션 프레임워크의 주요 인터페이스들을 설명해주세요.</b></summary>
  <div class="accordion-content">
    <b>List</b>: 순서가 있고 중복을 허용하는 컬렉션입니다. ArrayList, LinkedList, Vector가 대표적입니다. <b>Set</b>: 중복을 허용하지 않는 컬렉션입니다. HashSet, TreeSet, LinkedHashSet이 있습니다. <b>Map</b>: 키-값 쌍으로 데이터를 저장하는 컬렉션입니다. HashMap, TreeMap, LinkedHashMap이 있습니다. <b>Queue</b>: FIFO(First In First Out) 구조의 컬렉션입니다. LinkedList, PriorityQueue 등이 구현체입니다.
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q9. ArrayList와 LinkedList의 차이점은?</b></summary>
  <div class="accordion-content">
    <b>ArrayList</b>: 내부적으로 배열을 사용하여 데이터를 저장합니다. 인덱스를 통한 임의 접근이 빠르지만(O(1)), 중간에 데이터 삽입/삭제 시 요소들을 이동시켜야 하므로 느립니다(O(n)). 메모리를 연속적으로 사용합니다. <b>LinkedList</b>: 노드들이 링크로 연결된 구조입니다. 중간에 데이터 삽입/삭제가 빠르지만(O(1)), 특정 인덱스 접근 시 처음부터 순차 탐색해야 하므로 느립니다(O(n)). 각 노드마다 추가 메모리가 필요합니다.
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q10. HashMap과 TreeMap의 차이점은?</b></summary>
  <div class="accordion-content">
    <b>HashMap</b>: 해시 테이블을 기반으로 하며, 평균적으로 O(1)의 검색 성능을 제공합니다. 순서를 보장하지 않고 null 키와 값을 허용합니다. <b>TreeMap</b>: Red-Black 트리(균형 이진 검색 트리)를 기반으로 하며, 키를 기준으로 정렬된 순서를 유지합니다. 검색, 삽입, 삭제가 O(log n) 성능을 가지며, null 키는 허용하지 않습니다. 정렬이 필요한 경우 TreeMap을 사용합니다.
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q11. 예외 처리에서 Checked Exception과 Unchecked Exception의 차이점은?</b></summary>
  <div class="accordion-content">
    <b>Checked Exception</b>: 컴파일 시점에 예외 처리가 강제되는 예외입니다. IOException, SQLException 등이 대표적이며, 반드시 try-catch로 처리하거나 throws로 선언해야 합니다. <b>Unchecked Exception</b>: 런타임에 발생하는 예외로 처리가 강제되지 않습니다. RuntimeException을 상속받으며, NullPointerException, ArrayIndexOutOfBoundsException 등이 있습니다. 주로 프로그램의 논리적 오류로 인해 발생합니다.
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q12. 가비지 컬렉션(Garbage Collection)이란 무엇인가요?</b></summary>
  <div class="accordion-content">
    <p>가비지 컬렉션은 JVM에서 더 이상 참조되지 않는 객체들을 자동으로 메모리에서 해제하는 과정입니다. 힙 영역을 Young Generation(Eden, Survivor), Old Generation으로 나누어 관리합니다. Minor GC는 Young Generation에서, Major GC는 Old Generation에서 발생하며, Full GC는 전체 힙을 대상으로 합니다. 개발자가 직접 메모리 관리를 하지 않아도 되는 장점이 있지만, GC 동작 시 일시적으로 애플리케이션이 중단될 수 있습니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q13. 스레드(Thread)와 프로세스(Process)의 차이점은?</b></summary>
  <div class="accordion-content">
    <b>프로세스</b>: 실행 중인 프로그램으로 독립적인 메모리 공간을 가집니다. 다른 프로세스와 메모리를 공유하지 않으며, 프로세스 간 통신은 IPC를 통해 이루어집니다. <b>스레드</b>: 프로세스 내에서 실행되는 작업 단위로, 같은 프로세스의 스레드들은 힙과 메서드 영역을 공유하고 스택 영역만 개별적으로 가집니다. 생성 비용이 낮고 컨텍스트 스위칭이 빠르며, 데이터 공유가 쉽지만 동기화 문제를 고려해야 합니다.
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q14. synchronized 키워드의 역할과 사용법은?</b></summary>
  <div class="accordion-content">
    <p>synchronized는 멀티스레드 환경에서 동기화를 제공하여 스레드 안전성을 보장하는 키워드입니다. &lt;b&gt;메서드 레벨&lt;/b&gt;: 메서드 전체를 동기화하며, 인스턴스 메서드는 객체의 락을, static 메서드는 클래스 락을 사용합니다. &lt;b&gt;블록 레벨&lt;/b&gt;: 특정 코드 블록만 동기화하며, 더 세밀한 제어가 가능합니다. synchronized 영역에는 한 번에 하나의 스레드만 진입할 수 있어 race condition을 방지할 수 있지만, 성능 저하가 발생할 수 있습니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q15. final, finally, finalize의 차이점은?</b></summary>
  <div class="accordion-content">
    <b>final</b>: 변수에 사용하면 상수가 되어 값 변경이 불가능하고, 메서드에 사용하면 오버라이딩이 불가능하며, 클래스에 사용하면 상속이 불가능합니다. <b>finally</b>: try-catch문에서 예외 발생 여부와 관계없이 항상 실행되는 블록입니다. 주로 자원 정리 코드를 작성합니다. <b>finalize</b>: Object 클래스의 메서드로, 가비지 컬렉션이 객체를 수거하기 전에 호출됩니다. 하지만 호출 시점이 불확실하여 사용을 권장하지 않습니다.
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q16. static 키워드의 특징과 사용 용도는?</b></summary>
  <div class="accordion-content">
    <p>static은 클래스 레벨에서 공유되는 멤버를 정의할 때 사용합니다. &lt;b&gt;static 변수&lt;/b&gt;: 클래스가 로딩될 때 생성되고 모든 인스턴스가 공유합니다. &lt;b&gt;static 메서드&lt;/b&gt;: 인스턴스 생성 없이 호출 가능하며, 인스턴스 변수에 접근할 수 없습니다. &lt;b&gt;static 블록&lt;/b&gt;: 클래스 로딩 시 한 번만 실행되어 static 변수 초기화에 사용됩니다. 메모리에 한 번만 할당되어 메모리를 절약할 수 있지만, 프로그램 종료까지 메모리에 남아있습니다.</p>
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
