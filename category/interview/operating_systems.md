---
layout: default
title: "운영체제 면접 대비"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>운영체제 면접 대비</h2>
</section>

<!-- ① 기본 면접 Q&A -->
<details open class="section-box">
  <summary><span class="accordion-title">1️⃣ 프로세스와 스레드</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <details>
    <summary style="font-size:1rem;"><b>Q1. 운영체제란 무엇이며 주요 기능은 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p>운영체제는 컴퓨터 하드웨어와 소프트웨어 사이의 중간 역할을 하는 시스템 소프트웨어입니다. 주요 기능으로는 프로세스 관리, 메모리 관리, 파일 시스템 관리, 입출력 관리, 네트워크 관리가 있습니다. 또한 하드웨어 자원을 효율적으로 분배하고, 사용자와 응용 프로그램에게 편리한 인터페이스를 제공하며, 시스템의 보안과 안정성을 보장하는 역할을 합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q2. 프로세스와 스레드의 차이점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>프로세스는 실행 중인 프로그램으로, 독립적인 메모리 공간을 가지며 다른 프로세스와 완전히 분리되어 있습니다. 각 프로세스는 고유한 PID를 가지고 있으며, 프로세스 간 통신을 위해서는 IPC 메커니즘이 필요합니다. 반면 스레드는 프로세스 내부의 실행 단위로, 같은 프로세스의 스레드들은 코드, 데이터, 힙 영역을 공유하고 스택 영역만 개별적으로 가집니다. 스레드는 생성과 컨텍스트 스위칭 비용이 프로세스보다 적어 효율적입니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q3. 멀티 프로세스와 멀티 스레드의 차이점은 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q4. PCB(Process Control Block)란 무엇이며, 어떤 정보를 담고 있나요?</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <!--꼬리 질문-->
  <details class="tail-question">
    <summary style="font-size:1rem;"><b>💡 예상 꼬리질문</b></summary>
    <div class="accordion-content">
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q1. 스레드가 프로세스보다 컨텍스트 스위칭 비용이 적은 이유는 무엇인가요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q2. 멀티 스레드 환경에서 발생할 수 있는 문제점은 무엇인가요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q3. 프로세스 간 통신(IPC) 방법에는 어떤 것들이 있나요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q4. 스레드는 어떤 자원을 공유하고, 어떤 자원을 독립적으로 가지나요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q5. 컨텍스트 스위칭이 발생하는 상황은 언제인가요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    </div>
  </details>

  </div>
</details>


<!-- ① 기본 면접 Q&A -->
<details class="section-box">
  <summary><span class="accordion-title">2️⃣ CPU 스케줄링</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <details>
    <summary style="font-size:1rem;"><b>Q1. CPU 스케줄링이 필요한 이유는 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q2. 선점형 스케줄링과 비선점형 스케줄링의 차이점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q3. 알고 있는 CPU 스케줄링 알고리즘을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <!--꼬리 질문-->
  <details class="tail-question">
    <summary style="font-size:1rem;"><b>💡 예상 꼬리질문</b></summary>
    <div class="accordion-content">
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q1. Round Robin 스케줄링에서 Time Quantum이 너무 크거나 작으면 어떤 문제가 발생하나요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q2. Starvation(기아 현상)이란 무엇이며, 어떻게 해결할 수 있나요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q3. Priority Scheduling의 단점은 무엇인가요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q4. FCFS, SJF, Round Robin 각각의 장단점을 비교해주세요.</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    </div>
  </details>

  </div>
</details>


<!-- ① 기본 면접 Q&A -->
<details class="section-box">
  <summary><span class="accordion-title">3️⃣ 동기화</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <details>
    <summary style="font-size:1rem;"><b>Q1. 경쟁 상태(Race Condition)란 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q2. 임계 영역(Critical Section)이란 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q3. 뮤텍스(Mutex)와 세마포어(Semaphore)의 차이점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q4. 데드락(Deadlock)이란 무엇이며, 발생 조건 4가지를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <!--꼬리 질문-->
  <details class="tail-question">
    <summary style="font-size:1rem;"><b>💡 예상 꼬리질문</b></summary>
    <div class="accordion-content">
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q1. 데드락을 예방, 회피, 탐지, 복구하는 방법을 각각 설명해주세요.</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q2. 은행원 알고리즘(Banker's Algorithm)이란 무엇인가요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q3. 스핀락(Spinlock)이란 무엇이며, 언제 사용하면 좋나요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q4. 뮤텍스와 이진 세마포어는 같은 건가요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q5. Java에서 동기화를 구현하는 방법에는 어떤 것들이 있나요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    </div>
  </details>

  </div>
</details>


<!-- ① 기본 면접 Q&A -->
<details class="section-box">
  <summary><span class="accordion-title">4️⃣ 메모리 관리</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <details>
    <summary style="font-size:1rem;"><b>Q1. 가상 메모리(Virtual Memory)란 무엇이며, 왜 사용하나요?</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q2. 페이징(Paging)과 세그멘테이션(Segmentation)의 차이점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q3. 페이지 폴트(Page Fault)란 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q4. 내부 단편화와 외부 단편화의 차이점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <!--꼬리 질문-->
  <details class="tail-question">
    <summary style="font-size:1rem;"><b>💡 예상 꼬리질문</b></summary>
    <div class="accordion-content">
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q1. 페이지 교체 알고리즘에는 어떤 것들이 있나요? (LRU, FIFO, LFU 등)</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q2. TLB(Translation Lookaside Buffer)란 무엇인가요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q3. 스레싱(Thrashing)이란 무엇이며, 어떻게 해결하나요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q4. 워킹셋(Working Set)이란 무엇인가요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q5. 페이징에서 내부 단편화가 발생하는 이유는 무엇인가요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    </div>
  </details>

  </div>
</details>

<!-- ① 기본 면접 Q&A -->
<details class="section-box">
  <summary><span class="accordion-title">5️⃣ 프로세스 메모리 구조</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <details>
    <summary style="font-size:1rem;"><b>Q1. 프로세스의 메모리 구조(Code, Data, Heap, Stack)를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q2. 힙(Heap) 영역과 스택(Stack) 영역의 차이점은 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q3. 스택 오버플로우(Stack Overflow)는 왜 발생하나요?</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <!--꼬리 질문-->
  <details class="tail-question">
    <summary style="font-size:1rem;"><b>💡 예상 꼬리질문</b></summary>
    <div class="accordion-content">
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q1. 지역 변수와 전역 변수는 각각 어느 영역에 저장되나요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q2. 힙 영역은 왜 낮은 주소에서 높은 주소로 할당되나요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q3. Java에서 객체는 어느 메모리 영역에 저장되나요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q4. 메모리 누수(Memory Leak)는 왜 발생하나요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    </div>
  </details>

  </div>
</details>

<!-- ① 기본 면접 Q&A -->
<details class="section-box">
  <summary><span class="accordion-title">6️⃣ 시스템 콜과 인터럽트</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <details>
    <summary style="font-size:1rem;"><b>Q1. 시스템 콜(System Call)이란 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q2. 인터럽트(Interrupt)란 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q3. 사용자 모드(User Mode)와 커널 모드(Kernel Mode)의 차이점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <!--꼬리 질문-->
  <details class="tail-question">
    <summary style="font-size:1rem;"><b>💡 예상 꼬리질문</b></summary>
    <div class="accordion-content">
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q1. 시스템 콜의 종류에는 어떤 것들이 있나요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q2. 하드웨어 인터럽트와 소프트웨어 인터럽트의 차이점은 무엇인가요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q3. 모드 전환이 필요한 이유는 무엇인가요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q4. 트랩(Trap)이란 무엇인가요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    </div>
  </details>

  </div>
</details>


<!-- ① 기본 면접 Q&A -->
<details class="section-box">
  <summary><span class="accordion-title">7️⃣ 파일 시스템</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <details>
    <summary style="font-size:1rem;"><b>Q1. 파일 시스템이란 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q2. 아이노드(inode)란 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <!--꼬리 질문-->
  <details class="tail-question">
    <summary style="font-size:1rem;"><b>💡 예상 꼬리질문</b></summary>
    <div class="accordion-content">
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q1. 하드 링크와 심볼릭 링크(소프트 링크)의 차이점은 무엇인가요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q2. 파일 디스크립터(File Descriptor)란 무엇인가요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    </div>
  </details>

  </div>
</details>


<!-- ① 기본 면접 Q&A -->
<details class="section-box">
  <summary><span class="accordion-title">8️⃣ 캐시와 지역성</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <details>
    <summary style="font-size:1rem;"><b>Q1. 캐시 메모리란 무엇이며, 왜 사용하나요?</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q2. 지역성(Locality)의 원리를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <!--꼬리 질문-->
  <details class="tail-question">
    <summary style="font-size:1rem;"><b>💡 예상 꼬리질문</b></summary>
    <div class="accordion-content">
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q1. 시간 지역성과 공간 지역성의 차이점은 무엇인가요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q2. 캐시 히트와 캐시 미스란 무엇인가요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q3. 캐시의 지역성 원리를 활용한 코드 최적화 예시를 들어주세요.</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    </div>
  </details>

  </div>
</details>



<!-- ① 기본 면접 Q&A -->
<details class="section-box">
  <summary><span class="accordion-title">9️⃣ 백엔드 연관 심화 질문</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <details>
    <summary style="font-size:1rem;"><b>Q1. 동기(Synchronous)와 비동기(Asynchronous)의 차이점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q2. 블로킹(Blocking)과 논블로킹(Non-blocking)의 차이점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p></p>
    </div>
  </details>

  <!--꼬리 질문-->
  <details class="tail-question">
    <summary style="font-size:1rem;"><b>💡 예상 꼬리질문</b></summary>
    <div class="accordion-content">
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q1. 동기/비동기와 블로킹/논블로킹의 조합 4가지를 설명해주세요.</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q2. Node.js가 싱글 스레드인데도 동시성을 지원하는 이유는 무엇인가요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q3. I/O 멀티플렉싱이란 무엇인가요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    <!--구분-->
    </div>
  </details>

  </div>
</details>
