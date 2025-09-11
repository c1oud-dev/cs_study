---
layout: default
title: "운영체제 면접 대비 — 완전 정리"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>운영체제 면접 대비 — 기본·심화 Q&A + 개념 요약</h2>
  <p>구성: 기본 면접 Q&A → 심화 면접 Q&A → 추가 예상 질문 Q&A → 운영체제 개념 요약 노트</p>
</section>

<!-- ① 기본 면접 Q&A -->
<details open>
  <summary><span class="accordion-title">📋 기본 면접 Q&A</span> <span class="indicator">펼치기</span></summary>
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
      <hr>
      <h3>PID (Process ID)</h3>
      <ul>
        <li>PID는 프로세스의 주민등록번호 같은 개념이다.</li>
        <li>운영체제가 각 프로세스에게 부여하는 고유한 번호</li>
        <li>시스템에서 실행 중인 모든 프로세스를 구별하기 위해 사용</li>
        <li>프로세스가 생성되면 자동으로 할당되고, 종료되면 해제됨</li>
      </ul>
      <h3>IPC (Inter-Process Communication)</h3>
      <ul>
        <li>IPC는 프로세스들 간의 소통 방법이다.</li>
        <li>프로세스들은 기본적으로 독립적인 공간에서 실행되기 때문에, 서로 데이터를 주고받으려면 특별한 방법이 필요하다.</li>
        <li>주요 IPC 메커니즘들</li>
        <ul>
          <li>파이프(Pipe): 물을 흘려보내듯 데이터를 한 방향으로 전달</li>
          <li>공유 메모리: 여러 프로세스가 같은 메모리 공간을 공유</li>
          <li>메시지 큐: 우편함처럼 메시지를 저장했다가 전달</li>
          <li>소켓: 네트워크를 통한 통신 (같은 컴퓨터 내에서도 사용 가능)</li>
        </ul>
      </ul>
      <p>간단히 말해, PID는 프로세스의 이름표이고, IPC는 프로세스들이 대화하는 방법이라고 생각하면 됨.</p>
      <br>
      <h3>프로세스 vs 스레드를 쉽게 비유해보면</h3>
      <ul>
        <li>프로세스 = 공장 한 동</li>
        <li>스레드 = 공장 안의 작업자</li>
      </ul>
      <p>왜 "실행 단위"라고 할까?</p>
      <ul>
        <li>프로세스 자체는 그냥 "틀"이고, 실제로 CPU에서 명령어를 실행하는 것은 스레드이다.</li>
      </ul>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q3. 프로세스의 상태 전이도를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>프로세스는 생성, 준비, 실행, 대기, 종료의 5가지 상태를 가집니다. 새로 생성된 프로세스는 생성 상태에서 준비 상태로 이동합니다. 준비 상태의 프로세스는 CPU를 할당받으면 실행 상태가 되고, 시간 할당량이 끝나거나 높은 우선순위 프로세스가 오면 다시 준비 상태로 돌아갑니다. 실행 중 I/O 작업이나 자원 대기가 필요하면 대기 상태로 이동하고, 대기 조건이 해결되면 준비 상태로 돌아갑니다. 작업을 완료하면 종료 상태가 됩니다.</p>
      <hr>
      <figure style="margin:12px 0; text-align:center;">
      <img
        src="https://github.com/user-attachments/assets/6ff556a4-56c2-433d-b15b-b5019aaeff4d"
        alt="프로세스 상태 전이도(생성-준비-실행-대기-종료)"
        width="900" height="437" loading="lazy"
        style="max-width:100%; height:auto; display:inline-block;"
      />
      <figcaption style="font-size:.9rem; color:#666;"></figcaption>
      </figure>
      <ul>
        <li><b>Dispatch:</b> 스케줄러가 준비(Ready) → 실행(Run) 으로 올려보내는 동작. 준비 큐에서 하나를 뽑아 CPU에 얹고(컨텍스트 스위치) 실행을 시작합니다.</li>
        <li><b>Wake Up:</b> I/O 완료·자원 확보 같은 이벤트로 대기(Wait) → 준비(Ready) 로 깨우는 신호. 대기 중이던 프로세스가 다시 준비 큐로 돌아옵니다.</li>
        <li><b>Timer Runout:</b> 시간 할당량(타임 슬라이스) 끝을 알리는 타이머 인터럽트로 실행(Run) → 준비(Ready) 로 선점(preemption)됨.</li>
      </ul>
      <p>유사하게 더 높은 우선순위 프로세스가 도착해도 실행 중이던 프로세스가 선점되어 Run → Ready로 내려갑니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q4. 메모리 관리에서 가상 메모리란 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p>가상 메모리는 물리 메모리의 크기 제약을 극복하기 위한 기법으로, 프로세스가 실제 물리 메모리보다 큰 주소 공간을 사용할 수 있게 해줍니다. 각 프로세스는 독립적인 가상 주소 공간을 가지며, MMU(Memory Management Unit)가 가상 주소를 물리 주소로 변환합니다. 당장 필요하지 않은 페이지는 보조 저장장치에 저장하고, 필요할 때 메모리로 로드하는 페이징 기법을 사용합니다. 이를 통해 멀티태스킹과 메모리 보호, 공유를 효율적으로 구현할 수 있습니다.</p>
      <hr>
      <h3>MMU(Memory Management Unit)</h3>
      <p>가상 주소와 실제 주소를 변환해주는 하드웨어이다. 쉽게 말해, 메모리 번역기이다.</p>
      <ul>
        <li>프로그램이 사용하는 "가짜 주소"를 실제 RAM의 "진짜 주소"로 바꿔주는 역할을 한다.</li>
        <li><b>왜 필요할까?</b></li>
        <ul>
          <li>주소 충돌 방지: MMU가 각각 다른 실제 위치로 매핑해줘서, 여러 프로그램이 모두 "주소 0번부터 시작"이라고 해도 충돌되지 않는다.</li>
          <li>보안: 프로그램 A가 프로그램 B의 메모리에 접근하려고 하면 MMU가 차단</li>
          <li>메모리 효율성: 실제로는 연속되지 않은 메모리 조각들을 마치 연속된 것처럼 보이게 해줌</li>
        </ul>
      </ul>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q5. 페이징과 세그멘테이션의 차이점은 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p>페이징은 고정된 크기의 페이지 단위로 메모리를 관리하는 방식입니다. 내부 단편화는 발생할 수 있지만 외부 단편화는 발생하지 않으며, 하드웨어의 지원을 받아 효율적으로 구현됩니다. 세그멘테이션은 논리적 의미를 가진 가변 크기의 세그먼트로 메모리를 분할하는 방식입니다. 코드, 데이터, 스택 등으로 논리적으로 분할되어 보호와 공유가 용이하지만, 외부 단편화 문제가 발생할 수 있습니다. 현대의 많은 시스템에서는 두 기법을 결합한 세그먼트-페이지 방식을 사용합니다.</p>
    </div>
    <hr>
    <h3>하드웨어의 지원을 받아 구현된다는 건 무슨 의미일까?</h3>
    <p>페이징은 CPU 안의 전용 하드웨어(MMU·TLB)가 주소 변환을 대신 해줘서 빠르고 자동으로 돌아간다는 뜻</p>
    <ul>
      <li><b>MMU:</b> 프로그램이 쓰는 가상주소 → 실제 물리주소로 매 접근마다 자동 변환</li>
      <li><b>TLB:</b> 최근 변환 결과를 캐시해서 더 빠르게 접근</li>
      <li><b>페이지 폴트 신호:</b> 해당 페이지가 없으면 하드웨어가 예외를 띄워 OS가 불러오게 해줌</li>
    </ul>
    <p>즉, 소프트웨어가 일일이 계산하지 않아도 하드웨어가 뒷단에서 번역·캐시·예외 처리를 맡아줘서 페이징이 눈에 띄는 오버헤드 없이 동작한다는 의미</p>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q6. CPU 스케줄링 알고리즘들을 비교해주세요.</b></summary>
    <div class="accordion-content">
      <p>FCFS(First Come First Served)는 도착 순서대로 처리하는 가장 간단한 방식이지만, 평균 대기 시간이 길고 convoy effect가 발생할 수 있습니다. SJF(Shortest Job First)는 실행 시간이 짧은 작업부터 처리하여 평균 대기 시간을 최소화하지만, 실행 시간 예측이 어렵고 starvation 문제가 있습니다. Round Robin은 시간 할당량을 두고 순환하며 처리하는 방식으로 응답 시간이 좋지만, 시간 할당량 설정이 중요합니다. Priority Scheduling은 우선순위가 높은 작업부터 처리하지만 낮은 우선순위 작업의 starvation을 방지하기 위해 aging 기법을 사용합니다.</p>
      <hr>
      <h3>convoy effect</h3>
      <p>FCFS에서 맨 앞에 있는 ‘아주 긴 작업’ 때문에 뒤의 ‘짧은 작업들’이 줄줄이 묶여 느려지는 현상</p>
      <ul>
        <li><b>왜 생기나?</b> FCFS는 선착순·비선점이라, 긴 CPU-bound 작업이 먼저 오면 끝날 때까지 뒤의 I/O-bound(짧게 CPU 쓰고 I/O 하러 가는) 작업들이 시작도 못 함 → 그 사이에 I/O 장치는 놀고, 평균 대기시간·응답시간이 확 늘어남.</li>
        <li><b>피하는 법:</b> SJF/SRTF(짧은 작업 우선), Round Robin(선점), MLFQ처럼 I/O-bound에 유리한 선점형 스케줄링을 쓰면 완화됩니다.</li>
      </ul>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q7. 교착상태(Deadlock)란 무엇이며 발생 조건은?</b></summary>
    <div class="accordion-content">
      <p>교착상태는 두 개 이상의 프로세스가 서로가 점유하고 있는 자원을 기다리며 무한정 대기하는 상황입니다. 발생 조건으로는 상호 배제(자원을 한 번에 한 프로세스만 사용), 점유와 대기(자원을 보유한 채 다른 자원을 기다림), 비선점(다른 프로세스가 자원을 강제로 빼앗을 수 없음), 순환 대기(프로세스들이 원형으로 자원을 기다림)의 4가지 조건이 모두 성립해야 합니다. 이 중 하나라도 성립하지 않으면 교착상태를 방지할 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q8. 뮤텍스(Mutex)와 세마포어(Semaphore)의 차이점은?</b></summary>
    <div class="accordion-content">
      <p>뮤텍스는 mutual exclusion의 줄임말로, 한 번에 하나의 스레드만 임계 영역에 접근할 수 있도록 하는 동기화 객체입니다. 이진 값(0 또는 1)만 가지며, 락을 획득한 스레드만이 락을 해제할 수 있습니다. 세마포어는 정수 값을 가지는 동기화 객체로, 지정된 개수만큼의 스레드가 동시에 자원에 접근할 수 있습니다. wait(P)와 signal(V) 연산을 통해 값을 조작하며, 어떤 스레드든 세마포어 값을 증가시킬 수 있습니다. 뮤텍스는 소유권 개념이 있지만 세마포어는 없습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q9. 컨텍스트 스위칭(Context Switching)이란 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p>컨텍스트 스위칭은 현재 실행 중인 프로세스나 스레드를 중단하고 다른 프로세스나 스레드를 실행하는 과정입니다. 현재 실행 상태를 PCB(Process Control Block)에 저장하고, 실행할 프로세스의 상태를 PCB에서 복원합니다. 이 과정에서 CPU 레지스터, 프로그램 카운터, 메모리 관리 정보 등이 저장되고 복원됩니다. 컨텍스트 스위칭은 오버헤드가 발생하므로 너무 자주 발생하면 시스템 성능이 저하될 수 있습니다.</p>
      <hr>
      <p>PCB (Process Control Block) = 프로세스 정보를 담은 카드(프로세스의 신분증)</p>
      <ul>
        <li>무엇을 저장하나요?</li>
        <ul>
          <li>PID: 프로세스 번호</li>
          <li>레지스터 값들: CPU가 어디까지 실행했는지</li>
          <li>메모리 정보: 어떤 메모리를 사용 중인지</li>
          <li>상태: 실행 중/대기 중/종료 등</li>
        </ul>
        <li>언제 사용하나요?</li>
        <ul>
          <li>컨텍스트 스위칭 시</li>
          <ol>
            <li>현재 프로세스 정보를 PCB에 저장 (백업)</li>
            <li>다음 프로세스의 PCB 정보를 CPU에 복원</li>
          </ol>
        </ul>
      </ul>
      <p>PCB 덕분에 여러 프로그램이 번갈아 실행되면서도 각자 중단된 지점부터 정확히 이어갈 수 있다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q10. 파일 시스템의 역할과 구조를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>파일 시스템은 저장 장치에 파일을 저장하고 관리하는 시스템입니다. 파일의 생성, 삭제, 읽기, 쓰기 등의 기본 연산을 제공하고, 디렉토리 구조를 통해 파일을 계층적으로 조직화합니다. 파일 시스템은 일반적으로 부트 블록, 슈퍼 블록, 아이노드 테이블, 데이터 블록으로 구성됩니다. 슈퍼 블록은 파일 시스템의 전체 정보를 담고, 아이노드는 파일의 메타데이터를 저장하며, 데이터 블록은 실제 파일 내용을 저장합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q11. 시스템 콜(System Call)이란 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p>시스템 콜은 사용자 프로그램이 운영체제의 서비스를 요청하는 인터페이스입니다. 사용자 모드에서 실행되는 프로그램이 커널 모드의 기능을 사용하려면 시스템 콜을 통해야 합니다. 파일 조작(open, read, write), 프로세스 제어(fork, exec, exit), 정보 관리(getpid, alarm), 통신(pipe, socket) 등의 기능을 제공합니다. 시스템 콜 발생 시 인터럽트가 발생하고, 사용자 모드에서 커널 모드로 전환되어 요청된 서비스가 실행됩니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q12. 인터럽트(Interrupt)의 동작 원리를 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>인터럽트는 CPU가 현재 실행 중인 작업을 중단하고 다른 작업을 처리하게 하는 신호입니다. 하드웨어 인터럽트와 소프트웨어 인터럽트로 구분됩니다. 인터럽트 발생 시 현재 실행 중인 명령어를 완료하고, 현재 상태를 스택에 저장한 후 인터럽트 벡터를 통해 해당 인터럽트 핸들러로 분기합니다. 인터럽트 처리가 완료되면 저장된 상태를 복원하고 원래 작업을 계속 수행합니다. 이를 통해 I/O 처리, 시분할 시스템, 예외 처리 등이 가능합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q13. 메모리 계층구조와 캐시의 역할은 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p>메모리 계층구조는 속도가 빠르고 비싼 메모리에서 속도가 느리고 저렴한 메모리로 구성됩니다. CPU 레지스터, L1/L2/L3 캐시, 주기억장치(RAM), 보조기억장치(HDD/SSD) 순으로 배열됩니다. 캐시는 자주 사용되는 데이터를 빠른 메모리에 저장하여 평균 접근 시간을 줄이는 역할을 합니다. 지역성 원리(시간적, 공간적 지역성)에 기반하여 동작하며, 캐시 적중률이 높을수록 시스템 성능이 향상됩니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q14. 프로세스 간 통신(IPC) 방법들을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>파이프는 부모-자식 프로세스 간 단방향 통신을 제공하며, 명명된 파이프(FIFO)는 관련 없는 프로세스 간에도 사용할 수 있습니다. 공유 메모리는 여러 프로세스가 같은 메모리 영역을 공유하여 빠른 데이터 교환을 가능하게 하지만 동기화가 필요합니다. 메시지 큐는 메시지 단위로 데이터를 전송하며, 순서가 보장되고 동기화 문제가 적습니다. 소켓은 네트워크를 통한 프로세스 간 통신을 제공하며, 시그널은 간단한 이벤트 통지에 사용됩니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q15. 가상화(Virtualization)의 개념과 장점은 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p>가상화는 물리적 자원을 논리적으로 분할하여 여러 개의 가상 환경을 만드는 기술입니다. 하나의 물리적 서버에서 여러 개의 가상 머신을 실행할 수 있어 하드웨어 활용률을 높일 수 있습니다. 자원 격리를 통해 안정성을 보장하고, 스냅샷과 마이그레이션 기능으로 관리 편의성을 제공합니다. 또한 서로 다른 운영체제를 동시에 실행할 수 있어 개발과 테스트 환경 구축에 유리하며, 클라우드 컴퓨팅의 기반 기술입니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q16. 메모리 할당 방식인 연속 할당과 비연속 할당을 비교해주세요.</b></summary>
    <div class="accordion-content">
      <p>연속 할당은 프로세스를 물리 메모리의 연속된 공간에 배치하는 방식입니다. First Fit, Best Fit, Worst Fit 등의 전략이 있으며, 구현이 간단하고 주소 변환이 빠르지만 외부 단편화 문제가 발생합니다. 비연속 할당은 프로세스를 여러 개의 블록으로 나누어 메모리의 여러 위치에 배치하는 방식입니다. 페이징과 세그멘테이션이 대표적이며, 외부 단편화 문제를 해결하고 메모리 활용률을 높이지만, 주소 변환을 위한 추가 하드웨어와 오버헤드가 필요합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q17. 페이지 교체 알고리즘들을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>FIFO는 가장 먼저 들어온 페이지를 교체하는 간단한 방식이지만, Belady's Anomaly가 발생할 수 있습니다. LRU(Least Recently Used)는 가장 오랫동안 사용되지 않은 페이지를 교체하며, 지역성 원리에 기반하여 좋은 성능을 보입니다. LFU(Least Frequently Used)는 가장 적게 사용된 페이지를 교체하고, MFU(Most Frequently Used)는 그 반대입니다. Optimal은 가장 먼 미래에 사용될 페이지를 교체하는 이론적 최적 알고리즘이지만 실제로는 구현 불가능합니다. Clock 알고리즘은 LRU의 근사치로 하드웨어 구현이 용이합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q18. 입출력(I/O) 관리 방식들을 비교해주세요.</b></summary>
    <div class="accordion-content">
      <p>폴링(Polling)은 CPU가 주기적으로 I/O 장치의 상태를 확인하는 방식으로 구현이 간단하지만 CPU 자원을 낭비합니다. 인터럽트 방식은 I/O 작업 완료 시 인터럽트를 발생시켜 CPU에 알리므로 효율적이지만, 대량의 데이터 전송 시 인터럽트 오버헤드가 큽니다. DMA(Direct Memory Access)는 CPU의 개입 없이 I/O 장치가 직접 메모리와 데이터를 주고받는 방식으로, 대용량 데이터 전송에 효율적입니다. 비동기 I/O는 I/O 요청 후 다른 작업을 계속 수행하다가 완료 통지를 받는 방식입니다.</p>
    </div>
  </details>

  </div>
</details>

<!-- ② 심화 면접 Q&A -->
<details>
  <summary><span class="accordion-title">🚀 심화 면접 Q&A</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <details>
    <summary style="font-size:1rem;"><b>Q19. 메모리 보호(Memory Protection) 기법들을 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>메모리 보호는 프로세스가 자신에게 할당되지 않은 메모리에 접근하는 것을 방지하는 기법입니다. 기준 레지스터와 한계 레지스터를 사용하는 방법, 페이징에서 페이지 테이블의 보호 비트를 활용하는 방법, 세그멘테이션에서 세그먼트별 접근 권한을 설정하는 방법이 있습니다. 또한 사용자 모드와 커널 모드를 구분하여 특권 명령어의 실행을 제한하고, MMU에서 주소 변환 과정에서 접근 권한을 검사합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q20. Copy-on-Write(COW) 기법의 동작 원리는?</b></summary>
    <div class="accordion-content">
      <p>Copy-on-Write는 fork() 시스템 콜의 성능을 향상시키기 위한 기법입니다. 프로세스가 fork될 때 즉시 메모리를 복사하지 않고, 부모와 자식이 같은 물리 메모리를 공유하되 읽기 전용으로 설정합니다. 어느 한 프로세스가 메모리에 쓰기를 시도할 때만 실제로 복사가 일어납니다. 이를 통해 fork의 시간과 메모리 사용량을 크게 줄일 수 있으며, exec() 호출로 새로운 프로그램을 실행하는 경우 불필요한 복사를 피할 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q21. NUMA(Non-Uniform Memory Access) 아키텍처란?</b></summary>
    <div class="accordion-content">
      <p>NUMA는 멀티프로세서 시스템에서 각 프로세서가 로컬 메모리와 원격 메모리에 대해 서로 다른 접근 시간을 가지는 아키텍처입니다. 프로세서는 자신의 로컬 메모리에는 빠르게 접근하지만, 다른 프로세서의 로컬 메모리에는 상대적으로 느리게 접근합니다. 운영체제는 프로세스를 특정 NUMA 노드에 바인딩하고, 해당 노드의 로컬 메모리를 우선적으로 할당하여 성능을 최적화해야 합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q22. 실시간 시스템(Real-time System)의 스케줄링은 어떻게 다른가요?</b></summary>
    <div class="accordion-content">
      <p>실시간 시스템은 작업이 정해진 데드라인 내에 완료되어야 하는 시스템입니다. 경성 실시간 시스템은 데드라인을 절대 놓치면 안 되고, 연성 실시간 시스템은 가끔 놓쳐도 괜찮습니다. Rate Monotonic 스케줄링은 주기가 짧은 태스크에 높은 우선순위를 부여하고, Earliest Deadline First(EDF)는 데드라인이 가장 가까운 태스크를 먼저 실행합니다. 스케줄러빌리티 분석을 통해 주어진 태스크 집합이 모든 데드라인을 만족할 수 있는지 미리 검증해야 합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q23. 마이크로커널과 모놀리식 커널의 장단점은?</b></summary>
    <div class="accordion-content">
      <p>모놀리식 커널은 운영체제의 모든 기능이 커널 공간에서 실행되는 구조입니다. 시스템 콜 오버헤드가 적고 성능이 좋지만, 한 부분에서 오류가 발생하면 전체 시스템이 다운될 수 있고 유지보수가 어렵습니다. 마이크로커널은 최소한의 기능만 커널에 두고 나머지는 사용자 공간의 서버로 구현합니다. 안정성과 확장성이 좋고 다양한 하드웨어에 포팅이 용이하지만, 서버 간 통신 오버헤드로 인해 성능이 저하될 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q24. 메모리 압축(Memory Compression) 기술은 어떻게 동작하나요?</b></summary>
    <div class="accordion-content">
      <p>메모리 압축은 물리 메모리 부족 시 일부 페이지를 디스크로 스왑하는 대신 메모리 내에서 압축하여 저장하는 기술입니다. 디스크 I/O보다 압축/해제가 빠르기 때문에 성능 향상을 기대할 수 있습니다. 압축률이 좋은 페이지들을 선별하여 압축하고, 접근 빈도가 낮은 페이지를 우선적으로 대상으로 합니다. 최근 모바일 기기나 가상화 환경에서 메모리 효율성을 높이기 위해 활용되고 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q25. 컨테이너와 가상머신의 차이점은 무엇인가요?</b></summary>
    <div class="accordion-content">
      <p>가상머신은 하이퍼바이저 위에서 완전한 운영체제를 실행하는 방식으로, 강력한 격리를 제공하지만 오버헤드가 큽니다. 컨테이너는 호스트 운영체제의 커널을 공유하면서 애플리케이션 레벨에서 격리를 제공합니다. 컨테이너는 시작 시간이 빠르고 리소스 사용량이 적으며 이미지 크기가 작습니다. 하지만 보안 격리가 상대적으로 약하고 같은 커널을 공유하므로 운영체제 레벨의 버그에 취약할 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q26. 메모리 맵 파일(Memory-Mapped File)의 장점은?</b></summary>
    <div class="accordion-content">
      <p>메모리 맵 파일은 파일의 내용을 프로세스의 가상 주소 공간에 매핑하여, 파일 I/O를 메모리 접근처럼 처리할 수 있게 하는 기법입니다. 일반적인 read/write 시스템 콜보다 오버헤드가 적고, 여러 프로세스가 같은 파일을 공유할 때 효율적입니다. 또한 운영체제의 페이지 캐시를 직접 활용할 수 있어 중복 버퍼링을 피할 수 있습니다. 대용량 파일 처리나 데이터베이스 시스템에서 주로 사용됩니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q27. 버퍼 오버플로우와 스택 스매싱 보호 기법은?</b></summary>
    <div class="accordion-content">
      <p>버퍼 오버플로우는 배열의 경계를 넘어서 데이터를 쓰는 보안 취약점으로, 스택의 반환 주소를 변조하여 악의적인 코드를 실행시킬 수 있습니다. 보호 기법으로는 스택 카나리(Stack Canary)를 사용하여 오버플로우 발생을 탐지하고, ASLR(Address Space Layout Randomization)로 메모리 주소를 무작위화하며, DEP(Data Execution Prevention)로 데이터 영역의 코드 실행을 차단합니다. 또한 컴파일러 수준에서 스택 보호 옵션을 제공합니다.</p>
    </div>
  </details>

  </div>
</details>

<!-- ③ 추가 예상 질문 Q&A -->
<details>
  <summary><span class="accordion-title">💡 추가 예상 질문 Q&A</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <details>
    <summary style="font-size:1rem;"><b>Q28. 멀티코어 시스템에서 캐시 일관성(Cache Coherence) 문제는?</b></summary>
    <div class="accordion-content">
      <p>멀티코어 시스템에서 각 코어가 개별 캐시를 가질 때, 같은 메모리 위치의 데이터가 여러 캐시에 다른 값으로 저장될 수 있습니다. MESI 프로토콜은 Modified, Exclusive, Shared, Invalid 상태로 캐시 라인을 관리하여 일관성을 유지합니다. 한 코어가 데이터를 수정하면 다른 코어의 캐시에 있는 해당 데이터를 무효화하거나 업데이트합니다. 이러한 프로토콜은 하드웨어 수준에서 자동으로 처리되지만 성능에 영향을 줄 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q29. 운영체제의 부팅 과정을 단계별로 설명해주세요.</b></summary>
    <div class="accordion-content">
      <p>전원이 켜지면 BIOS/UEFI가 실행되어 하드웨어를 초기화하고 POST(Power-On Self Test)를 수행합니다. 부트 로더를 찾아 실행하면, 부트 로더는 커널 이미지를 메모리에 로드하고 커널로 제어를 넘깁니다. 커널은 하드웨어를 감지하고 드라이버를 로드하며, 루트 파일 시스템을 마운트합니다. 그 다음 init 프로세스(또는 systemd)가 시작되어 시스템 서비스들을 차례로 시작하고, 마지막으로 로그인 프롬프트나 그래픽 인터페이스가 나타납니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q30. 커널 스레드와 사용자 스레드의 차이점은?</b></summary>
    <div class="accordion-content">
      <p>사용자 스레드는 사용자 공간에서 라이브러리에 의해 관리되는 스레드로, 커널이 존재를 모릅니다. 생성과 컨텍스트 스위칭이 빠르지만, 하나의 스레드가 블록되면 전체 프로세스가 블록됩니다. 커널 스레드는 커널에 의해 직접 관리되는 스레드로, 한 스레드가 블록되어도 다른 스레드는 계속 실행될 수 있습니다. 하지만 생성과 관리 비용이 높습니다. 하이브리드 모델은 사용자 스레드를 커널 스레드에 매핑하여 두 방식의 장점을 결합합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q31. 파일 시스템의 저널링(Journaling) 기능이란?</b></summary>
    <div class="accordion-content">
      <p>저널링은 파일 시스템의 일관성을 보장하기 위해 변경 사항을 미리 로그에 기록하는 기법입니다. 시스템 크래시 발생 시 저널을 통해 미완료된 작업을 롤백하거나 재실행할 수 있어 파일 시스템 복구 시간을 단축시킵니다. 메타데이터만 저널링하는 방식과 데이터도 함께 저널링하는 방식이 있으며, 후자가 더 안전하지만 성능 오버헤드가 큽니다. ext3, ext4, NTFS 등의 현대 파일 시스템에서 지원됩니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q32. 로드 밸런싱과 프로세서 친화도(Processor Affinity)란?</b></summary>
    <div class="accordion-content">
      <p>로드 밸런싱은 멀티프로세서 시스템에서 작업을 여러 CPU에 균등하게 분배하여 전체 시스템 성능을 최적화하는 기법입니다. 프로세서 친화도는 프로세스나 스레드를 특정 CPU에 고정하여 실행하는 것으로, 캐시 지역성을 향상시키고 메모리 접근 패턴을 최적화할 수 있습니다. 소프트 친화도는 가능한 한 같은 CPU를 사용하려 하지만 필요시 이동이 가능하고, 하드 친화도는 특정 CPU에 강제로 고정합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q33. 메모리 디프래그멘테이션(Defragmentation) 기법들은?</b></summary>
    <div class="accordion-content">
      <p>압축(Compaction)은 사용 중인 메모리 블록들을 한쪽으로 모아 큰 연속 공간을 만드는 기법입니다. 모든 포인터를 업데이트해야 하므로 비용이 크지만 외부 단편화를 완전히 해결할 수 있습니다. 버디 시스템은 2의 거듭제곱 크기로 메모리를 관리하여 단편화를 줄이는 방법이고, 슬랩 할당자는 자주 사용되는 크기의 객체를 미리 할당해두어 효율성을 높입니다. 가비지 컬렉터는 사용하지 않는 메모리를 자동으로 회수하여 단편화를 방지합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q34. 분산 시스템에서의 일관성(Consistency) 모델들은?</b></summary>
    <div class="accordion-content">
      <p>강한 일관성은 모든 노드가 동시에 같은 값을 보는 모델이지만 성능과 가용성에 제약이 있습니다. 약한 일관성은 일정 시간 후에 일관성이 보장되는 모델로, 최종 일관성이 대표적입니다. 순차 일관성은 모든 연산이 어떤 순서로 실행되든 결과가 같아야 한다는 조건이고, 인과 일관성은 인과 관계가 있는 연산들의 순서만 보장합니다. CAP 정리에 따르면 분산 시스템에서는 일관성, 가용성, 분할 내성 중 두 가지만 동시에 만족할 수 있습니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q35. 컨테이너 오케스트레이션의 핵심 개념들은?</b></summary>
    <div class="accordion-content">
      <p>컨테이너 오케스트레이션은 대규모 컨테이너 환경을 자동으로 배포, 관리, 확장하는 기술입니다. 쿠버네티스는 파드(Pod) 단위로 컨테이너를 그룹화하고, 서비스 디스커버리를 통해 동적으로 연결합니다. 리플리카셋은 원하는 수의 파드 인스턴스를 유지하고, 롤링 업데이트로 무중단 배포를 지원합니다. 리소스 쿼터와 네임스페이스를 통해 멀티테넌시를 지원하며, 헬스체크와 셀프힐링 기능으로 안정성을 보장합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q36. 시스템 모니터링과 성능 튜닝 지표들은?</b></summary>
    <div class="accordion-content">
      <p>CPU 사용률은 시스템의 처리 능력을 나타내며, 메모리 사용률과 스왑 사용량은 메모리 부족 상황을 파악하는 데 중요합니다. 디스크 I/O는 IOPS, 처리량, 지연 시간으로 측정하며, 네트워크는 대역폭 사용률과 패킷 손실률을 모니터링합니다. 로드 애버리지는 시스템의 전반적인 부하를 나타내고, 컨텍스트 스위치 횟수는 스케줄링 오버헤드를 측정합니다. 이러한 지표들을 종합적으로 분석하여 병목 지점을 찾고 성능을 최적화해야 합니다.</p>
    </div>
  </details>

  <details>
    <summary style="font-size:1rem;"><b>Q37. 보안 운영체제(Security-Enhanced OS)의 특징은?</b></summary>
    <div class="accordion-content">
      <p>보안 운영체제는 일반 운영체제에 추가적인 보안 기능을 제공합니다. 강제 접근 제어(MAC)는 관리자가 정의한 보안 정책에 따라 접근을 제한하고, 다단계 보안은 기밀성 수준에 따라 정보를 분류합니다. 감사(Audit) 기능은 모든 보안 관련 이벤트를 기록하고, 침입 탐지 시스템은 비정상적인 활동을 감지합니다. SELinux는 리눅스에 MAC를 추가한 대표적인 예시로, 세밀한 권한 제어와 프로세스 격리를 제공합니다.</p>
    </div>
  </details>

  </div>
</details>

<!-- ④ 운영체제 개념 요약 노트 -->
<details>
  <summary><span class="accordion-title">📚 운영체제 개념 요약 노트</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

  <h3>🏗 운영체제 구조</h3>
  <p><b>시스템 구성요소</b><br/>
  커널: 핵심 기능 (프로세스, 메모리, I/O 관리)<br/>
  시스템 콜: 사용자-커널 인터페이스<br/>
  디바이스 드라이버: 하드웨어 추상화<br/>
  셸: 사용자 인터페이스</p>

  <p><b>실행 모드</b><br/>
  사용자 모드: 제한된 권한<br/>
  커널 모드: 전체 시스템 접근 가능<br/>
  모드 전환: 시스템 콜, 인터럽트, 예외 시 발생</p>

  <h3>⚙ 프로세스 관리</h3>
  <p><b>프로세스 상태</b><br/>
  생성(New) → 준비(Ready) → 실행(Running)<br/>
  대기(Waiting) → 준비(Ready)<br/>
  실행(Running) → 종료(Terminated)</p>

  <p><b>스케줄링 알고리즘 비교</b><br/>
  FCFS: 간단하지만 convoy effect<br/>
  SJF: 평균 대기시간 최소, starvation 문제<br/>
  Round Robin: 공평하지만 time quantum 중요<br/>
  Priority: 우선순위 기반, aging으로 starvation 방지</p>

  <p><b>스레드 vs 프로세스</b><br/>
  생성 비용: 스레드 &lt; 프로세스<br/>
  메모리 공유: 스레드 O, 프로세스 X<br/>
  컨텍스트 스위칭: 스레드 &lt; 프로세스</p>

  <h3>💾 메모리 관리</h3>
  <p><b>메모리 계층</b></p>

  <p><b>페이징 vs 세그멘테이션</b><br/>
  구분 페이징 세그멘테이션<br/>
  크기 고정 가변<br/>
  내부 단편화 있음 없음<br/>
  외부 단편화 없음 있음<br/>
  주소 변환 단순 복잡</p>

  <h3>🔄 동기화</h3>
  <p><b>동기화 도구</b><br/>
  뮤텍스: 상호배제, 소유권 있음<br/>
  세마포어: 카운팅, 소유권 없음<br/>
  모니터: 고수준 동기화<br/>
  조건 변수: wait/signal 기반</p>

  <p><b>교착상태 조건</b><br/>
  1. 상호배제 (Mutual Exclusion)<br/>
  2. 점유와 대기 (Hold and Wait)<br/>
  3. 비선점 (No Preemption)<br/>
  4. 순환 대기 (Circular Wait)</p>

  <h3>📁 파일 시스템</h3>
  <p><b>파일 시스템 구조</b><br/>
  부트 블록: 부팅 정보<br/>
  슈퍼 블록: 파일 시스템 메타데이터<br/>
  아이노드 테이블: 파일 정보<br/>
  데이터 블록: 실제 파일 내용</p>

  <p><b>메모리 계층 (cycles)</b><br/>
  레지스터 (1 cycle)<br/>
  ↓<br/>
  L1 캐시 (1-2 cycles)<br/>
  ↓<br/>
  L2 캐시 (3-10 cycles)<br/>
  ↓<br/>
  L3 캐시 (10-20 cycles)<br/>
  ↓<br/>
  주기억장치 (100-300 cycles)<br/>
  ↓<br/>
  보조기억장치 (10,000,000+ cycles)</p>

  <h3>🔌 입출력 시스템</h3>
  <p><b>I/O 방식</b><br/>
  프로그램 제어 I/O: CPU가 직접 제어<br/>
  인터럽트 기반 I/O: 완료 시 인터럽트<br/>
  DMA: CPU 개입 없이 메모리 직접 접근</p>

  <p><b>버퍼링 종류</b><br/>
  단일 버퍼: 간단, 효율성 낮음<br/>
  이중 버퍼: 동시 읽기/쓰기 가능<br/>
  원형 버퍼: 연속적인 데이터 스트림</p>

  <h3>🛡 보안과 보호</h3>
  <p><b>접근 제어</b><br/>
  DAC (임의 접근 제어): 소유자가 권한 결정<br/>
  MAC (강제 접근 제어): 시스템 정책 기반<br/>
  RBAC (역할 기반): 역할에 따른 접근</p>

  <p><b>보안 위협</b><br/>
  버퍼 오버플로우: 스택 카나리로 방지<br/>
  코드 인젝션: ASLR, DEP로 완화<br/>
  권한 상승: 최소 권한 원칙</p>

  <h3>⚡ 성능 메트릭</h3>
  <p><b>CPU 메트릭</b><br/>
  사용률 (%): 100% - idle time<br/>
  로드 애버리지: 실행 대기 중인 프로세스 수<br/>
  컨텍스트 스위치: 프로세스/스레드 전환 횟수</p>

  <p><b>메모리 메트릭</b><br/>
  사용률 (%): (사용 중 메모리 / 전체 메모리) × 100<br/>
  페이지 폴트 비율: 메모리 접근 실패 횟수<br/>
  스왑 사용량: 가상 메모리 사용 정도</p>

  <p><b>I/O 메트릭</b><br/>
  IOPS: 초당 입출력 연산 수<br/>
  처리량 (Throughput): 단위 시간당 처리 데이터량<br/>
  지연시간 (Latency): 요청부터 응답까지 시간</p>

  <h3>🎯 시스템 최적화 전략</h3>
  <p><b>CPU 최적화</b><br/>
  프로세서 친화도 설정<br/>
  적절한 스케줄링 알고리즘 선택<br/>
  멀티스레드 프로그래밍 활용</p>

  <p><b>메모리 최적화</b><br/>
  지역성 원리 활용<br/>
  메모리 풀 사용<br/>
  가비지 컬렉션 튜닝</p>

  <p><b>I/O 최적화</b><br/>
  비동기 I/O 활용<br/>
  버퍼링과 캐싱<br/>
  SSD 특성에 맞는 최적화</p>

  <h3>💭 면접 팁</h3>
  <p>1. 기본 개념을 정확히 이해하고 실무 예시로 설명<br/>
  2. 장단점을 균형있게 제시하고 상황에 따른 선택 기준 언급<br/>
  3. 시스템 전체적인 관점에서 연관성 설명<br/>
  4. 최신 기술 동향과 전통적 방법의 비교<br/>
  5. 성능 메트릭과 최적화 경험 구체적으로 언급<br/>
  6. 보안과 안정성 측면도 함께 고려한 답변</p>

  </div>
</details>
