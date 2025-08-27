---
layout: default
title: "Containerization vs Virtualization"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>Containerization vs Virtualization</h2>
  <p>컨테이너화(Containerization)와 가상화(Virtualization)는 <b>모두 공유된 하드웨어 위에서 여러 애플리케이션을 격리해 실행</b>하는 기술이지만, 접근 방식과 자원 사용 면에서 큰 차이가 있다.</p>
  <p><b>가상화(Virtualization)</b>는 하이퍼바이저 위에서 각자 독립된 운영체제를 가진 <b>가상 머신(VM)</b>을 생성한다. 이는 강력한 격리를 제공하지만 자원을 더 많이 소비한다.</p>
  <p><b>컨테이너화(Containerization)</b>는 Docker로 대표되며, <b>공유 운영체제 커널</b>을 사용하여 애플리케이션을 위한 격리된 환경(컨테이너)을 만든다. 컨테이너는 VM보다 더 가볍고, 더 빨리 시작되며, 더 적은 자원을 사용한다. 따라서 마이크로서비스 아키텍처나 빠른 배포에 이상적이다.</p>
  <p>가상화는 더 강력한 보안 격리를 제공하고, 하나의 하드웨어에서 <b>다른 운영체제</b>를 실행할 수 있다는 장점이 있다. 반면 컨테이너화는 더 높은 효율성과 확장성을 제공하며, 특히 <b>클라우드 네이티브 애플리케이션</b>에 적합하다.</p>
  <p>따라서 선택은 <b>특정 사용 사례, 보안 요구사항, 인프라 필요</b>에 따라 달라진다.</p>
  <p><strong>정리: 가상화는 VM으로 강력한 격리, 컨테이너화는 공유 커널로 효율성과 확장성 제공한다.</strong></p>
</section>

<details open>
  <summary>
    <span class="accordion-title">Docker</span> 
    <a href="./docker.html" style="margin-left: 8px; font-size: 0.5em; color: #0366d6;">이동하기 →</a>
  </summary>
</details>

<details open>
  <summary><span class="accordion-title">Kubernetes</span>
  <a href="./kubernetes.html" style="margin-left: 8px; font-size: 0.5em; color: #0366d6;">이동하기 →</a> 
  </summary>
</details>

<!-- 설명 -->
<details open>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">LXC(Linux Containers)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>LXC</b>는 하나의 리눅스 커널을 통해 제어된 호스트 위에서 여러 개의 리눅스 시스템을 가상으로 실행하기 위해 사용되는 <b>운영체제 수준의 가상화 기술</b>이다.</p>
  <p>LXC는 리눅스 커널의 격리(containment) 기능을 활용하는 <b>사용자 공간 인터페이스(userspace interface)</b>로, 강력한 API와 간단한 도구를 제공하여 리눅스 사용자가 시스템 컨테이너나 애플리케이션 컨테이너를 손쉽게 생성하고 관리할 수 있도록 한다.</p>
  <p><strong>정리: LXC는 단일 커널 위에서 여러 리눅스 컨테이너를 실행·관리하는 OS 수준 가상화 기술이다.</strong></p>
  <!-- 가로선 추가 -->
  <hr>
  <ul>
    <li><strong>리눅스 커널 (Linux Kernel):</strong> 리눅스 운영체제의 핵심으로, 하드웨어와 소프트웨어를 연결하는 중간 계층 역할을 하며 프로세스 관리, 메모리 관리, 파일 시스템, 네트워크, 보안 등을 담당한다.</li>
    <li><strong>격리 기능 (Containment / Isolation Features):</strong> 하나의 운영체제 안에서 프로세스, 네트워크, 파일 시스템 등을 서로 분리하여 독립된 환경처럼 동작하게 만드는 기능.</li>
    <ul><li>예: 네임스페이스, cgroups</li></ul>
    <li><strong>사용자 공간 인터페이스 (Userspace Interface):</strong> 커널과 직접 상호작용하지 않고, 일반 사용자가 애플리케이션을 통해 커널 기능을 쉽게 사용할 수 있도록 제공되는 인터페이스.</li>
    <ul><li>예: LXC 도구, 시스템 콜을 추상화한 API</li></ul>
  </ul>
</div>
</details>
