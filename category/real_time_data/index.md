---
layout: default
title: "Real Time Data"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>Real Time Data</h2>
  <p>실시간 데이터(Real-time data)는 정보가 지연 없이 즉시 처리되고 제공되어, 사용자나 시스템이 현재 상황에 신속하게 대응할 수 있도록 하는 데이터를 의미합니다. 이러한 유형의 데이터는 금융 거래 플랫폼, 온라인 게임, 실시간 분석, 모니터링 시스템처럼 즉각적인 업데이트와 반응이 필요한 애플리케이션에서 필수적입니다. 실시간 데이터 처리는 데이터가 생성되는 즉시 이를 수집·분석·전달하는 과정을 포함하며, 보통 <b>스트림 처리 프레임워크(Apache Kafka, Apache Flink 등) 와 저지연(low-latency) 데이터베이스</b> 같은 기술을 활용합니다. 효과적인 실시간 데이터 시스템은 초고속 데이터 흐름을 처리할 수 있어야 하며, 이를 통해 <b>정확하고 시기적절한 의사결정</b>이 가능해집니다.</p>
</section>

<!-- 설명 -->
<details open>
<summary><span class="accordion-title">서버 전송 이벤트(Server-Sent Events, SSE)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>서버 전송 이벤트(Server-Sent Events, SSE)는 <b>하나의 지속적인 HTTP 연결을 통해 서버가 웹 클라이언트로 실시간 업데이트를 전송</b>할 수 있게 해주는 기술입니다. 이 방식은 서버가 클라이언트에 효율적으로 데이터를 푸시할 수 있도록 하며, 연결이 끊어지면 자동으로 재연결됩니다. SSE는 <b>일방향 통신</b>이 필요한 애플리케이션(예: 실시간 알림, 데이터 피드)에 적합하며, 이벤트 데이터를 <b>단순한 텍스트 기반 형식</b>으로 전송합니다. 클라이언트 측에서는 <b>JavaScript의 EventSource API</b>를 사용해 손쉽게 처리할 수 있습니다.</p>
</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title">웹소켓(WebSockets)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>웹소켓(WebSockets)은 <b>클라이언트(보통 웹 브라우저)와 서버 간에 양방향(full-duplex) 실시간 통신</b>을 가능하게 하는 프로토콜입니다. 기존 HTTP가 데이터를 주고받기 위해 여러 번의 요청-응답 사이클을 거쳐야 하는 것과 달리, 웹소켓은 <b>하나의 지속적인 연결</b>을 유지하여 양쪽에서 자유롭게 데이터를 주고받을 수 있습니다. 이 덕분에 <b>실시간 상호작용</b>(예: 라이브 채팅, 온라인 게임, 웹페이지 실시간 업데이트)을 효율적으로 구현할 수 있습니다. 웹소켓 연결은 <b>HTTP 핸드셰이크</b>로 시작한 뒤 <b>WebSocket 프로토콜로 업그레이드</b>되며, HTTP 폴링이나 롱 폴링보다 <b>지연 시간이 적고 오버헤드가 줄어듭니다.</b></p>
</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title">롱 폴링(Long Polling)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>롱 폴링(Long Polling)은 <b>클라이언트가 서버에 새 데이터를 요청할 때, 서버에 아직 데이터가 없으면 빈 응답을 보내지 않고 일정 시간 동안 요청을 보류</b>하는 방식입니다.
  <ul>
    <li>서버에 새 데이터가 그 시간 동안 생기면 → 서버가 즉시 응답을 보내고 요청이 완료됩니다.</li>
    <li>만약 지정된 타임아웃 시간까지도 데이터가 없으면 → 서버가 “데이터 없음” 응답을 보내고 연결을 종료합니다.</li>
    <li>이후 클라이언트는 다시 서버에 요청을 보내면서 <b>새로운 요청-응답 사이클</b>을 반복합니다.</li>
    즉, 롱 폴링은 <b>실시간에 가까운 통신을 흉내내는 방법</b>으로, WebSocket이나 SSE보다 효율성은 떨어지지만, <b>HTTP 표준만으로도 구현할 수 있다는 장점</b>이 있습니다.
  </ul>
  </p>
</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title">쇼트 폴링(Short Polling)</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>쇼트 폴링(Short Polling)은 <b>클라이언트가 일정한 주기로 서버에 요청을 보내 업데이트나 새로운 데이터를 확인하는 방식</b>입니다.
  <ul>
    <li>서버는 매번 요청을 받을 때마다 현재 상태나 마지막 요청 이후의 변경 사항을 응답합니다.</li>
    <li>구현이 단순하고 대부분의 HTTP 인프라와 호환되지만, <b>불필요하게 많은 네트워크 요청</b>이 발생할 수 있고, <b>실시간성 전달에는 지연(latency)</b>이 생길 수 있습니다.</li>
    <li>따라서 <b>롱 폴링(Long Polling)이나 WebSocket 같은 실시간 통신 방식</b>보다 비효율적이지만, <b>실시간 요구가 크지 않고 구현의 단순함이 중요한 경우</b>에 주로 사용됩니다.</li>
  </ul>
  </p>
</div>
</details>
