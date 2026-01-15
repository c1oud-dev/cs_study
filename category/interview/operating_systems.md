---
layout: default
title: "운영체제 면접 대비"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>운영체제 면접 대비</h2>
</section>

<!-- ① 기본 면접 Q&A -->
<details open>
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
  <details>
    <summary style="font-size:1rem;"><b>💡 예상 꼬리질문</b></summary>
    <div class="accordion-content">
      <details>
        <summary style="font-size:1rem;"><b>Q1. 스레드가 프로세스보다 컨텍스트 스위칭 비용이 적은 이유는 무엇인가요?</b></summary>
        <div class="accordion-content">
          <p></p>
        </div>
      </details>
    </div>
  </details>

  </div>
</details>
