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
      <p>멀티 프로세스는 여러 개의 독립적인 프로세스를 실행하는 방식이고, 멀티 스레드는 하나의 프로세스 안에서 여러 스레드를 실행하는 방식입니다.</p>
      <p>가장 큰 차이점은 메모리 공유 여부입니다. 멀티 프로세스는 각 프로세스가 독립된 메모리 공간을 가지므로 하나가 죽어도 다른 프로세스에 영향이 없어 안정적입니다. 반면 멀티 스레드는 힙, 데이터 영역을 공유하기 때문에 메모리 효율이 좋고 통신이 빠르지만, 하나의 스레드에 문제가 생기면 전체 프로세스가 영향을 받을 수 있습니다.</p>
      <p>또한 멀티 스레드는 컨텍스트 스위칭 비용이 적어 성능상 유리하지만, 공유 자원 접근 시 동기화 문제를 신경 써야 합니다.</p>
      <table>
      <thead>
        <tr>
          <th>구분</th>
          <th>멀티 프로세스</th>
          <th>멀티 스레드</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>메모리</td>
          <td>독립적</td>
          <td>공유</td>
        </tr>
        <tr>
          <td>안정성</td>
          <td>높음</td>
          <td>낮음</td>
        </tr>
        <tr>
          <td>자원 효율</td>
          <td>낮음</td>
          <td>높음</td>
        </tr>
        <tr>
          <td>통신</td>
          <td>IPC 필요</td>
          <td>직접 공유</td>
        </tr>
        <tr>
          <td>컨텍스트 스위칭</td>
          <td>비용 큼</td>
          <td>비용 적음</td>
        </tr>
      </tbody>
    </table>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q4. 컨텍스트 스위칭(Context Switching)이란 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p>CPU가 현재 실행 중인 프로세스(또는 스레드)를 멈추고, 다른 프로세스로 전환하는 작업입니다.</p>
      <h4>동작 과정</h4>
      <ol>
        <li>현재 프로세스의 상태(레지스터, PC 등)를 PCB에 저장</li>
        <li>다음 실행할 프로세스의 상태를 PCB에서 불러옴</li>
        <li>CPU가 새로운 프로세스를 실행</li>
      </ol>
      <h4>발생 시점</h4>
      <ul>
        <li>타임 슬라이스(할당 시간) 만료</li>
        <li>I/O 요청 등으로 프로세스가 대기 상태로 전환될 때</li>
        <li>인터럽트 발생 시</li>
      </ul>
      <h4>특징</h4>
      <p>컨텍스트 스위칭 중에는 CPU가 실제 작업을 수행하지 못하므로 오버헤드가 발생합니다. 따라서 너무 자주 발생하면 시스템 성능이 저하됩니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q5. PCB(Process Control Block)란 무엇이며, 어떤 정보를 담고 있나요?</b></summary>
    <div class="accordion-content">
      <p>PCB는 운영체제가 각 프로세스를 관리하기 위해 해당 프로세스의 정보를 저장하는 자료구조입니다. 프로세스가 생성될 때 만들어지고, 종료되면 삭제됩니다.</p>
      <h4>담고 있는 정보</h4>
      <ul>
        <li><b>프로세스 ID(PID):</b> 프로세스 고유 식별 번호</li>
        <li><b>프로세스 상태:</b> 실행, 준비, 대기 등 현재 상태</li>
        <li><b>프로그램 카운터(PC):</b> 다음에 실행할 명령어 주소</li>
        <li><b>CPU 레지스터 값:</b> 컨텍스트 스위칭 시 저장/복원할 레지스터 정보</li>
        <li><b>CPU 스케줄링 정보:</b> 우선순위, 스케줄링 큐 포인터</li>
        <li><b>메모리 관리 정보:</b> 페이지 테이블, 세그먼트 테이블 등</li>
        <li><b>입출력 상태 정보:</b> 할당된 I/O 장치, 열린 파일 목록</li>
      </ul>
      <h4>핵심 포인트</h4>
      <p>PCB는 컨텍스트 스위칭의 핵심입니다. CPU가 다른 프로세스로 전환될 때, 현재 프로세스 상태를 PCB에 저장하고, 다음 프로세스의 PCB에서 정보를 불러와서 실행을 이어갑니다.</p>
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
          <p>스레드는 같은 프로세스 내에서 코드, 데이터, 힙 영역을 공유하기 때문입니다. 전환 시 스택과 레지스터 값만 교체하면 되므로 비용이 적습니다.</p>
          <h4>프로세스 전환 시 필요한 작업</h4>
          <ul>
            <li>메모리 주소 공간 전체 교체</li>
            <li>페이지 테이블 교체</li>
            <li>TLB(Translation Lookaside Buffer) 비우기</li>
            <li>캐시 무효화 발생 가능</li>
          </ul>
          <h4>스레드 전환 시 필요한 작업</h4>
          <ul>
            <li>스택 포인터 교체</li>
            <li>레지스터 값 교체</li>
            <li>프로그램 카운터(PC) 교체</li>
          </ul>
          <p>쉽게 말해, 프로세스 전환은 "다른 집으로 이사"하는 것과 같고, 스레드 전환은 "같은 집에서 방만 바꾸는 것"과 같습니다. 주소 공간을 공유하니까 짐을 옮길 필요가 없는 거죠.</p>
        </div>
      </details>
    <!--구분-->
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q2. 멀티 스레드 환경에서 발생할 수 있는 문제점은 무엇인가요?</b></summary>
        <div class="accordion-content">
          <p><b>1. 경쟁 상태 (Race Condition)</b> - 여러 스레드가 공유 자원에 동시에 접근하여 예상치 못한 결과가 발생하는 문제입니다. 실행 순서에 따라 결과가 달라집니다.</p>
          <p><b>2. 데드락 (Deadlock)</b> - 두 개 이상의 스레드가 서로가 가진 자원을 기다리며 무한히 대기하는 상태입니다.</p>
          <p><b>3. 기아 상태 (Starvation)</b> - 특정 스레드가 계속 자원을 할당받지 못하고 무한히 대기하는 상태입니다.</p>
          <p><b>4. 동기화 오버헤드</b> - 공유 자원 보호를 위해 락(Lock)을 사용하면 성능 저하가 발생할 수 있습니다.</p>
          <h4>해결 방법 (간단히)</h4>
          <ul>
            <li>뮤텍스, 세마포어로 임계 영역 보호</li>
            <li>락 획득 순서 통일로 데드락 방지</li>
            <li>불변 객체 사용, 스레드 로컬 변수 활용</li>
          </ul>
        </div>
      </details>
    <!--구분-->
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q3. 프로세스 간 통신(IPC) 방법에는 어떤 것들이 있나요?</b></summary>
        <div class="accordion-content">
          <p>"프로세스는 각각 독립된 메모리 공간을 가지고 있어서 서로 직접 데이터를 주고받을 수 없습니다. 그래서 운영체제가 제공하는 IPC라는 통신 방법을 사용해야 합니다.</p>
          <p>대표적인 방법으로는 먼저 파이프가 있습니다. 파이프는 단방향 통신 방식으로, 주로 부모-자식 프로세스 간에 사용됩니다. 양방향 통신이 필요하면 파이프를 두 개 만들어야 합니다.</p>
          <p>다음으로 공유 메모리가 있는데, 이건 여러 프로세스가 같은 메모리 공간을 함께 사용하는 방식입니다. 메모리를 직접 접근하기 때문에 IPC 중에서 가장 빠릅니다. 다만 동시에 접근하면 문제가 생길 수 있어서 동기화 처리를 직접 해줘야 합니다.</p>
          <p>메시지 큐는 메시지 단위로 데이터를 주고받는 방식입니다. 보내는 쪽과 받는 쪽이 동시에 동작하지 않아도 되는 비동기 통신이 가능합니다.</p>
          <p>마지막으로 소켓은 네트워크를 통해 다른 컴퓨터에 있는 프로세스와도 통신할 수 있는 방법입니다. 분산 시스템이나 서버-클라이언트 구조에서 많이 사용됩니다."</p>
        </div>
      </details>
    <!--구분-->
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q4. 스레드는 어떤 자원을 공유하고, 어떤 자원을 독립적으로 가지나요?</b></summary>
        <div class="accordion-content">
        <h4>공유하는 자원</h4>
          <ul>
            <li><b>코드 영역:</b> 실행할 프로그램 코드</li>
            <li><b>데이터 영역:</b> 전역 변수, static 변수</li>
            <li><b>힙 영역:</b> 동적으로 할당된 메모리</li>
            <li><b>파일 디스크립터:</b> 열린 파일 목록</li>
            <li><b>프로세스 ID:</b> 같은 프로세스에 속함</li>
          </ul>
          <h4>독립적으로 가지는 자원</h4>
          <ul>
            <li><b>스택 영역:</b> 지역 변수, 함수 호출 정보</li>
            <li><b>프로그램 카운터(PC):</b> 다음 실행할 명령어 주소</li>
            <li><b>레지스터 값:</b> 현재 연산 상태</li>
            <li><b>스레드 ID:</b> 스레드 고유 식별자</li>
          </ul>
          <p>각 스레드는 독립적인 실행 흐름을 가지므로 "어디까지 실행했는지(PC)", "함수 호출 상태(스택)"는 따로 관리해야 합니다. 반면 같은 작업을 협력해서 수행하므로 코드와 데이터는 공유하는 것이 효율적입니다.</p>
          <p>정리하면, 스레드는 스택, PC, 레지스터만 독립적으로 가지고, 나머지(코드, 데이터, 힙)는 공유합니다.</p>
        </div>
      </details>
    <!--구분-->
    <!--구분-->
      <details>
        <summary style="font-size:1rem;"><b>Q5. 컨텍스트 스위칭이 발생하는 상황은 언제인가요?</b></summary>
        <div class="accordion-content">
          <ol>
            <li><b>타임 슬라이스 만료</b> - CPU 할당 시간(Time Quantum)이 끝나면 다른 프로세스/스레드에게 CPU를 넘겨줍니다. (선점형 스케줄링)</li>
            <li><b>I/O 요청</b> - 파일 읽기, 네트워크 통신 등 I/O 작업 요청 시 해당 프로세스는 대기 상태로 전환되고 다른 프로세스가 실행됩니다.</li>
            <li><b>인터럽트 발생</b> - 하드웨어 인터럽트(키보드 입력, 타이머 등)가 발생하면 현재 작업을 멈추고 인터럽트를 처리합니다.</li>
            <li><b>시스템 콜 호출</b> - 프로세스가 운영체제 기능을 요청할 때 사용자 모드 → 커널 모드 전환이 일어납니다.</li>
            <li><b>우선순위 변경</b> - 더 높은 우선순위의 프로세스가 준비 상태가 되면 현재 프로세스를 중단하고 전환합니다.</li>
          </ol>
          <p>정리하면, 컨텍스트 스위칭은 타임 슬라이스 만료, I/O 요청, 인터럽트, 높은 우선순위 프로세스 등장 시 발생합니다.</p>
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
      <p>CPU는 한 번에 하나의 프로세스만 실행할 수 있기 때문입니다. 여러 프로세스가 효율적으로 CPU를 사용하려면 어떤 순서로, 얼마나 오래 실행할지 결정하는 스케줄링이 필요합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q2. 선점형 스케줄링과 비선점형 스케줄링의 차이점을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <table>
      <thead>
        <tr>
          <th>구분</th>
          <th>선점형 (Preemptive)</th>
          <th>비선점형 (Non-preemptive)</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>CPU 강제 회수</td>
          <td>가능</td>
          <td>불가능</td>
        </tr>
        <tr>
          <td>전환 시점</td>
          <td>언제든지</td>
          <td>프로세스가 스스로 반납할 때</td>
        </tr>
        <tr>
          <td>응답성</td>
          <td>빠름</td>
          <td>느림</td>
        </tr>
        <tr>
          <td>오버헤드</td>
          <td>상대적으로 높음</td>
          <td>낮음</td>
        </tr>
      </tbody>
      </table>
      <h4>선점형 스케줄링</h4>
      <p>운영체제가 실행 중인 프로세스로부터 CPU를 <b>강제로 회수</b>할 수 있습니다.</p>
      <ul>
        <li>예시: Round Robin, Priority Scheduling (선점형), SRTF</li>
        <li>장점: 응답 시간이 빠름, 한 프로세스가 CPU 독점 방지</li>
        <li>단점: 컨텍스트 스위칭 오버헤드 증가</li>
      </ul>
      <h4>비선점형 스케줄링</h4>
      <p>프로세스가 <b>자발적으로 CPU를 반납</b>(종료 또는 I/O 대기)할 때까지 기다립니다.</p>
      <ul>
        <li>예시: FCFS, SJF (비선점형)</li>
        <li>장점: 컨텍스트 스위칭 적음, 구현 단순</li>
        <li>단점: 긴 프로세스가 CPU 독점 가능 (Convoy Effect)</li>
      </ul>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q3. 알고 있는 CPU 스케줄링 알고리즘을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <h4>FCFS (First Come First Served)</h4>
      <p>가장 먼저 도착한 프로세스부터 실행합니다. 구현이 간단하지만, 긴 프로세스가 앞에 있으면 뒤의 짧은 프로세스들이 오래 기다리는 <b>Convoy Effect</b>가 발생합니다.</p>
      <h4>SJF (Shortest Job First)</h4>
      <p>실행 시간이 가장 짧은 프로세스를 먼저 실행합니다. 평균 대기 시간이 최소지만, 실행 시간을 미리 알기 어렵고 긴 프로세스는 <b>기아 상태</b>에 빠질 수 있습니다.</p>
      <h4>Round Robin</h4>
      <p>각 프로세스에 동일한 시간 할당량(Time Quantum)을 주고 돌아가며 실행합니다. 응답 시간이 빠르고 공정하며, 대화형 시스템에 적합합니다.</p>
      <h4>Priority Scheduling</h4>
      <p>우선순위가 높은 프로세스를 먼저 실행합니다. 낮은 우선순위 프로세스의 기아 문제를 <b>에이징(Aging) 기법</b>으로 해결할 수 있습니다.</p>
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
