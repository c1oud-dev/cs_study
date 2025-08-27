---
layout: default
title: "Message Brokers"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>Message Brokers</h2>
  <p>메시지 브로커(Message Brokers)는 <b>분산 시스템이나 컴포넌트 간의 통신을 중개</b>하는 역할을 한다. 즉 메시지를 <b>수신하고, 라우팅하며, 전달</b>하는 과정을 통해 통신을 가능하게 한다.</p>
  <p>이들은 <b>비동기 메시지 전달</b>을 지원하여 <b>생산자(보내는 측)</b>와 <b>소비자(받는 측)</b>를 분리(디커플링)시킴으로써 시스템의 <b>확장성</b>과 <b>유연성</b>을 향상시킨다.</p>
  <p>메시지 브로커의 일반적인 기능에는 다음이 포함된다.</p>
  <ul>
    <li><strong>메시지 큐잉(message queuing)</strong> </li>
    <li><strong>부하 분산(load balancing)</strong> </li>
    <li><b>영속성</b>과 <b>승인</b> 같은 기능을 통한 <b>신뢰성 있는 메시지 전달 보장</b></li>
  </ul>
  <p>대표적인 메시지 브로커로는 <b>Apache Kafka, RabbitMQ, ActiveMQ</b> 등이 있으며, 각각 <b>실시간 데이터 처리, 이벤트 스트리밍, 작업 관리</b> 등 다양한 사용 사례에 맞게 특화된 기능과 역량을 제공한다.</p>
  <p><strong style="color: #555555;">📝 정리: 메시지 브로커는 분산 시스템에서 생산자와 소비자 사이의 메시지를 비동기적으로 중개하여 확장성과 신뢰성을 높여주는 시스템이다.</strong></p>
</section>

<!-- 설명 -->
<details open>
<summary><span class="accordion-title">RabbitMQ </span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
    <p>RabbitMQ는 <b>오픈 소스 메시지 브로커</b>로, <b>AMQP(Advanced Message Queuing Protocol)</b>를 사용하여 분산 시스템 간의 메시지 교환을 가능하게 한다.</p>
    <p>이것은 메시지를 <b>큐잉(queuing)</b>하고 <b>라우팅(routing)</b>하여 <b>생산자(Producer)</b>와 <b>소비자(Consumer)</b> 사이에서 <b>비동기 통신</b>을 지원하며, 애플리케이션 컴포넌트를 <b>분리(디커플링)</b>시켜 <b>확장성</b>과 <b>신뢰성</b>을 향상시킨다.</p>
    <p>RabbitMQ는 다음과 같은 기능을 제공한다.
    <ul>
        <li><strong>메시지 내구성(Message durability)</strong> </li>
        <li><strong>승인(Acknowledgment)</strong> </li>
        <li><strong>익스체인지(Exchange)와 큐(Queue)를 통한 유연한 라우팅</strong> </li></p>
    </ul>
    <p>또한 <b>높은 수준의 설정 가능성</b>을 제공하여 다음과 같은 다양한 메시징 패턴을 지원한다.</p>
    <ul>
        <li><strong>발행/구독(Publish/Subscribe)</strong> </li>
        <li><strong>요청/응답(Request/Reply)</strong> </li>
        <li><strong>지점 간(Point-to-Point) 통신</strong> </li>
    </ul>
    <p>RabbitMQ는 <b>엔터프라이즈 환경</b>에서 <b>대량 메시지 처리(high-throughput messaging)</b>와 <b>이기종 시스템 간 통합</b>을 위해 널리 사용된다.</p>
    <p><strong style="color: #555555;">📝 정리: RabbitMQ는 AMQP 기반의 오픈 소스 메시지 브로커로, 큐와 익스체인지를 통해 다양한 메시징 패턴을 지원하며 엔터프라이즈 환경에서 안정적인 메시지 전달을 제공한다.</strong></p>
    <!-- 가로선 추가 -->
    <hr>
    <ul>
        <li><strong>AMQP (Advanced Message Queuing Protocol):</strong> 메시지 브로커(예: RabbitMQ)에서 사용되는 표준 프로토콜로, 메시지를 안전하고 신뢰성 있게 전송하기 위한 규칙과 형식을 정의한다.</li>
        <li><strong>큐잉 (Queuing):</strong> 메시지를 <b>큐(Queue)</b>에 쌓아두고, 소비자가 준비되었을 때 순서대로 전달하는 방식으로 비동기 처리를 가능하게 한다.</li>
        <li><strong>라우팅 (Routing):</strong> 메시지를 특정 조건(토픽, 규칙 등)에 따라 적절한 큐나 소비자에게 전달하는 과정이다.</li>
        <li><strong>비동기 통신 (Asynchronous Communication):</strong> 송신자와 수신자가 동시에 연결되어 있을 필요 없이, 메시지를 중간에 저장했다가 나중에 전달하는 통신 방식이다.</li>
        <li><strong>분리(디커플링, Decoupling):</strong> 생산자와 소비자가 서로 직접 알 필요 없이 메시지 브로커를 통해 간접적으로 통신하게 하여, 시스템 의존성을 줄이고 유연성을 높이는 개념이다.</li>
        <li><strong>이기종 시스템 (Heterogeneous Systems):</strong> 서로 다른 기술 스택(언어, 플랫폼, 프레임워크 등)을 사용하는 시스템들을 의미하며, 메시지 브로커는 이기종 시스템 간의 통합을 쉽게 해준다.</li>
    </ul>
</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title">Kafka </span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
    <p>Apache Kafka는 <b>대규모 처리량(high-throughput)</b>과 <b>내결함성(fault-tolerant)</b>을 갖춘 <b>분산 이벤트 스트리밍 플랫폼</b>이다. Kafka는 메시지 브로커처럼 동작하여 시스템이 <b>레코드 스트림을 발행(publish)하고 구독(subscribe)</b>할 수 있게 해주며, 이는 <b>분산 커밋 로그(distributed commit log)</b>와 유사하다.</p>
    <p>Kafka는 <b>높은 확장성(scalability)</b>을 제공하고, <b>낮은 지연(latency)</b>으로 대량 데이터를 처리할 수 있어 <b>실시간 분석, 로그 수집, 데이터 통합</b> 등에 이상적이다.</p>
    <p>주요 특징으로는</p>
    <ul>
    <li><strong>토픽(Topic):</strong> 데이터 스트림을 조직화</li>
    <li><strong>파티션(Partition):</strong> 병렬 처리 지원</li>
    <li><strong>복제(Replication):</strong> 내결함성 보장</li>
    </ul>
    <p>이로써 분산 시스템 전반에서 <b>대규모 데이터 흐름을 신뢰성 있고 효율적으로 처리</b>할 수 있다.</p>
    <p><strong style="color: #555555;">📝 정리: Kafka는 대규모 데이터를 낮은 지연으로 처리하는 분산 이벤트 스트리밍 플랫폼으로, 토픽·파티션·복제를 통해 실시간 분석과 데이터 통합에 최적화된 메시지 브로커이다.</strong></p>
    <!-- 가로선 추가 -->
    <hr>
    <ul>
    <li><strong>레코드 스트림 (Record Stream):</strong> 시간 순서대로 발생하는 데이터를 지속적으로 전달·처리하는 데이터 흐름이다.</li>
    <li><strong>분산 커밋 로그 (Distributed Commit Log):</strong> 분산 환경에서 모든 이벤트를 순서대로 기록하고, 여러 소비자가 동일한 기록을 읽을 수 있도록 보장하는 로그 저장 방식이다.</li>
    </ul>
</div>
</details>
