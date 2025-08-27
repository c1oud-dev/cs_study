---
layout: default
title: "Kubernetes"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>Kubernetes</h2>
  <p>Kubernetes는 <b>오픈 소스 컨테이너 오케스트레이션 플랫폼</b>으로, <b>컨테이너화된 애플리케이션의 배포, 확장, 관리</b>를 자동화한다. 이는 <b>기반 인프라를 추상화</b>하고, 대규모로 애플리케이션을 관리할 수 있는 방법을 제공하며, 동시에 <b>유연성, 이식성, 풍부한 기능 세트</b>를 제공한다. Kubernetes는 <b>광범위한 채택, 활발한 커뮤니티, 복잡한 다계층 애플리케이션을 처리할 수 있는 능력</b> 덕분에 컨테이너 오케스트레이션의 <b>사실상 표준(de facto standard)</b>이 되었다.</p>

  <h3 style="color: #0366d6;">개요</h3>
  <p>Kubernetes는 <b>컨테이너화된 워크로드와 서비스를 관리하기 위한 이식 가능하고 확장 가능한 오픈 소스 플랫폼</b>으로, <b>선언적 구성(declarative configuration)</b>과 <b>자동화</b>를 모두 지원한다. 이는 <b>빠르게 성장하는 대규모 생태계</b>를 보유하고 있으며, Kubernetes 관련 서비스, 지원, 도구들이 널리 제공되고 있다.</p>
  <p>“Kubernetes”라는 이름은 <b>그리스어에서 ‘키잡이(helmsman)’ 또는 ‘조종사(pilot)’</b>를 뜻한다. 약어 <b>“K8s”</b>는 “K”와 “s” 사이에 있는 여덟 글자를 세어 만든 것이다. Google은 2014년에 Kubernetes 프로젝트를 오픈 소스로 공개했으며, 이는 <b>Google이 15년 이상 대규모 운영 환경에서 실제 워크로드를 관리해 온 경험과, 커뮤니티에서 나온 최고 수준의 아이디어와 관행</b>을 결합한 것이다.</p>

  <h3 style="color: #0366d6;">Kubernetes의 필요성</h3>
  <p>Kubernetes(k8s)가 필요한 이유는, <b>대규모 컨테이너화된 애플리케이션을 배포하고 관리할 수 있는 강력하고 유연한 플랫폼</b>을 제공하기 때문이다. 이를 통해 다음을 가능하게 한다.
    <ul>
        <li>손쉬운 확장성(Scalability)</li>
        <li>높은 복원력(Resilience)</li>
        <li>애플리케이션 이식성(Portability)</li>
        <li>다양한 작업의 자동화(Automation)</li>
        <li>컨테이너 플랫폼의 표준화(Standardization)</li>
    </ul>
    또한 k8s는 운영팀의 <b>복잡성과 업무 부담을 줄여주어</b>, 그들이 <b>더 전략적인 업무에 집중할 수 있도록</b> 도와준다.</p>

  <h3 style="color: #0366d6;">핵심 개념과 용어</h3>
  <p>Kubernetes는 <b>컨테이너화된 애플리케이션의 배포, 확장, 관리</b>를 자동화하는 오픈 소스 컨테이너 오케스트레이션 플랫폼이다. 다음은 Kubernetes에서 중요한 개념과 용어들이다.
    <ul>
        <li><strong>클러스터 아키텍처 (Cluster Architecture):</strong> Kubernetes의 아키텍처 개념.</li>
        <li><strong>컨테이너 (Containers):</strong> 애플리케이션과 런타임 의존성을 함께 패키징하는 기술.</li>
        <li><strong>워크로드 (Workloads):</strong> Kubernetes에서 배포 가능한 최소 단위인 <b>파드(Pod)</b>와, 이를 실행하도록 돕는 상위 수준의 추상화 개념.</li>
        <li><strong>서비스, 로드 밸런싱, 네트워킹 (Services, Load Balancing, and Networking):</strong> Kubernetes 네트워킹 관련 개념 및 리소스.</li>
        <li><strong>스토리지 (Storage):</strong> 클러스터의 파드에 <b>영구적/임시적 스토리지</b>를 제공하는 방법.</li>
        <li><strong>구성 (Configuration):</strong> 파드(Pod)를 구성하기 위해 Kubernetes가 제공하는 리소스.</li>
        <li><strong>클러스터 관리 (Cluster Administration):</strong> Kubernetes 클러스터를 생성하거나 관리할 때 필요한 하위 수준의 세부 내용.</li>
    </ul>
  </p>

  <h3 style="color: #0366d6;">Alternatives</h3>
  <p>Kubernetes는 컨테이너화된 애플리케이션을 관리·배포하기 위해 널리 사용되는 <b>오픈 소스 컨테이너 오케스트레이션 도구</b>이다. 이와 같은 기능을 제공하는 다른 도구들도 있으며, 대표적으로 <b>Docker Swarm, Mesos, Nomad</b> 등이 있다. 하지만 Kubernetes와 이들 도구 간에는 몇 가지 주요 차이가 있다.
    <ul>
        <li><strong>아키텍처 (Architecture):</strong> Kubernetes는 <b>API 서버, kubelet, kube-proxy, etcd</b> 등 여러 컴포넌트가 함께 작동하는 <b>모듈형 시스템</b>으로 설계되었다.</li>
        <li><strong>확장성 (Scalability):</strong> Kubernetes는 <b>대규모 배포를 처리</b>할 수 있도록 설계되었으며, 수요에 따라 애플리케이션을 <b>자동으로 확장/축소</b>할 수 있다.</li>
        <li><strong>유연성 (Flexibility):</strong> Kubernetes는 <b>높은 수준의 설정 가능성</b>을 제공해 특정 요구사항에 맞게 커스터마이징할 수 있는 반면, 다른 도구들은 상대적으로 제한적일 수 있다.</li>
        <li><strong>이식성 (Portability):</strong> Kubernetes는 <b>클라우드에 종속되지 않도록(cloud-agnostic)</b> 설계되어, 퍼블릭/프라이빗 클라우드뿐만 아니라 <b>온프레미스 환경</b>에서도 실행할 수 있다.</li>
        <li><strong>커뮤니티 (Community):</strong> Kubernetes는 <b>대규모·활발한 개발자 및 사용자 커뮤니티</b>를 보유하고 있어, 지속적인 개발 기여와 풍부한 지원을 받을 수 있다.</li>
    </ul>
  </p>
</section>

<!-- 설명 -->
<details>
<summary><span class="accordion-title">Containers(컨테이너) </span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
    <p>Kubernetes는 <b>컨테이너를 기반</b>으로 구축되었으므로, Kubernetes를 학습하기 전에 <b>컨테이너를 직접 실행하고 빌드할 수 있는 능숙함</b>을 갖추는 것이 필요하다.</p>
</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Setting up Kubernetes</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <h3>Deploying your First Application</h3>
  <p>Kubernetes에서 첫 번째 애플리케이션을 배포하려면, 먼저 <b>배포(Deployment)와 서비스(Service) 매니페스트를 YAML 파일</b>로 작성해야 한다. 그 다음, <u>kubectl apply</u> 명령어를 사용해 이 매니페스트를 <b>Kubernetes 클러스터에 적용</b>한다. 이후 <u>kubectl get pods</u> 명령어로 애플리케이션의 <b>파드(Pod)가 정상 실행 중인지 확인</b>하고, <u>kubectl get services</u> 명령어를 통해 서비스를 확인한 뒤, <b>웹 브라우저나 cURL 같은 도구</b>로 서비스에 접근해 테스트할 수 있다. 또한 <b>Helm 차트(Helm charts)</b>나 <b>Kubernetes 오퍼레이터(operators)</b>와 같은 다양한 도구 및 플랫폼을 활용하면 애플리케이션 배포 과정을 더욱 간소화할 수 있다.</p>

  <hr>
  <h3>Choosing a Managed Provider</h3>
  <p>관리형 제공자(Managed Provider)란 클라우드 기반 서비스로, 관리형 Kubernetes 환경을 제공한다. 이는 제공자가 서버, 스토리지, 네트워킹 같은 기반 인프라뿐만 아니라, Kubernetes 클러스터의 설치, 설정, 유지 관리까지 모두 담당한다는 의미이다. 관리형 Kubernetes 제공자를 선택할 때 고려해야 할 요소는 다음과 같다.
    <ul>
        <li>사용 중인 <b>클라우드 제공자</b></li>
        <li>제공되는 <b>기능 및 역량</b></li>
        <li><b>가격과 과금 방식</b></li>
        <li><b>지원(서포트)</b> 수준</li>
        <li><b>보안 및 규정 준수(Compliance)</b></li>
        <li>제공자의 <b>평판과 리뷰</b></li>
    </ul>
    이러한 요소들을 종합적으로 검토하면, <b>조직의 요구사항을 충족하면서 최고의 가치를 제공하는 제공자</b>를 선택할 수 있다.
  </p>

  <hr>
  <h3>Installing a Local Cluster</h3>
  <p>CentOS 7 또는 Ubuntu에 Kubernetes 클러스터를 설치·구성하려면, 먼저 <b>클러스터 설치에 필요한 사전 준비와 요구 사항</b>을 설정해야 한다. 그 후 <b>Kubeadm, Kubelet, Kubectl</b>과 같은 Kubernetes 구성 요소들을 설치한다. 이후에는 <b>마스터 노드와 워커 노드를 연결</b>해야 하며, 연결이 성공적으로 이루어지면 <b>클러스터에 애플리케이션을 배포하여 정상 동작 여부를 확인</b>할 수 있다.</p>

</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Running Application</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <h3>Deployments</h3>
  <p><b>Deployment</b>는 <b>선언적 구성(declarative configuration)</b>을 통해 <b>파드(Pods)와 레플리카셋(ReplicaSets)</b>을 관리하는 리소스 객체이다. 배포는 애플리케이션 워크로드의 <b>수명 주기, 파드 개수, 배포 전략, 컨테이너 이미지</b> 등을 정의하는 <b>원하는 상태(Desired State)</b>를 기술한다. 그리고 <b>Deployment Controller</b>는 실제 상태가 원하는 상태와 일치하도록 보장하며, 예를 들어 <b>실패한 파드를 교체</b>한다. 기본적으로 디플로이먼트는 <b>Recreate(다시 생성)</b>와 <b>Rolling Update</b>(순차 업데이트) 같은 배포 전략을 지원하며, <b>Blue/Green 배포나 카나리 배포(Canary Deployment)</b> 같은 더 고급 배포 전략으로도 커스터마이징할 수 있다.</p>

  <hr>
  <h3>Pods</h3>
  <p>Kubernetes에서 <b>파드(Pod)</b>는 클러스터 내에서 실행되는 프로세스의 단일 인스턴스를 나타내는 <b>가장 작은 배포 단위</b>이다. 파드에는 하나 이상의 <b>컨테이너</b>가 포함될 수 있으며, 이 컨테이너들은 <b>동일한 네트워크 네임스페이스</b>를 공유하고, 동일한 <b>스토리지 볼륨</b>에도 접근할 수 있다. 파드는 Kubernetes에 의해 <b>생성 및 관리</b>되며, 클러스터 내의 <b>노드(Node)</b> 중 하나에 스케줄링되어 실행된다. 또한 파드는 경량적이고 유연한 <b>추상화 계층</b>을 제공하여, Kubernetes가 <b>컨테이너화된 애플리케이션의 배포, 확장, 네트워킹</b>을 관리할 수 있게 한다. 더불어 파드는 <b>동일한 파드 내에서 실행되는 컨테이너 간의 통신 및 데이터 교환</b>을 가능하게 한다.
  </p>

  <hr>
  <h3>ReplicaSets</h3>
  <p><b>ReplicaSet</b>은 클러스터 내에서 <b>지정된 수의 파드 복제본(identical copies)</b>이 항상 실행되도록 보장하는 컨트롤러이다. 레플리카셋은 <b>높은 가용성(High Availability)</b>과 <b>확장성(Scalability)</b>을 보장하는데, 이는 수요 변화나 하드웨어 장애가 발생했을 때 <b>자동으로 파드 복제본의 수를 늘리거나 줄여주기 때문</b>이다. 레플리카셋은 <b>YAML 파일</b>로 정의되며, 이 안에는 <b>원하는 복제본 수, 사용할 파드 템플릿, 기타 설정</b>이 포함된다. 레플리카셋은 파드 상태를 지속적으로 모니터링하며, <b>원하는 상태(Desired State)</b>를 만족시키기 위해 필요 시 <b>파드 복제본을 생성하거나 삭제</b>한다.</p>

  <hr>
  <h3>StatefulSets</h3>
  <p><b>스테이트풀셋(StatefulSet)</b>은 <b>안정적인 네트워크 ID와 안정적인 스토리지 볼륨</b>이 필요한 상태 저장 파드(Stateful Pods) 집합의 배포와 스케일링을 관리하는 컨트롤러이다. StatefulSets는 <b>데이터베이스와 같이 상태를 가지는 애플리케이션</b> 실행에 사용되며, 이 경우 각 파드의 <b>순서(order)</b>와 <b>고유성(uniqueness)</b>이 중요하다. StatefulSets는 각 파드에 <b>고유하고 안정적인 네트워크 ID와 스토리지 볼륨</b>을 제공하여, 애플리케이션이 <b>스케일 업·다운되거나, 노드가 장애/교체</b>되더라도 데이터 일관성을 유지할 수 있게 한다. StatefulSets는 <b>파드 템플릿, 파드에 접근하기 위한 서비스(Service), 기타 설정</b>을 포함하는 <b>YAML 파일</b>로 정의된다.</p>

  <hr>
  <h3>Jobs</h3>
  <p>Jobs는 <b>유한한 작업(finite task)이나 배치 작업(batch job)의 실행을 관리하는 컨트롤러</b>이다. 잡은 <b>배치 처리, 데이터 분석, 백업</b>과 같이 <b>종료 조건이 명확한 단기 실행 작업</b>을 수행하는 데 사용되며, 작업이 완료되면 종료된다. 잡은 작업을 실행하기 위해 <b>하나 이상의 파드(Pod)</b>를 생성하고, 각 파드의 <b>완료 상태를 모니터링</b>한다. 만약 파드가 실패하거나 중단되면, 잡은 자동으로 <b>대체 파드(replacement pod)</b>를 생성하여 작업이 성공적으로 완료되도록 보장한다. 잡은 <b>파드 템플릿, 완료 조건, 기타 설정</b>을 포함한 <b>YAML 파일</b>로 정의된다.</p>

</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Services and Networking</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <h3>Networking and Pod to Pod Communication(네트워킹과 파드 간 통신)</h3>
  <p>네트워킹은 Kubernetes 클러스터 내에서 <b>파드와 리소스 간 통신</b>을 위해 매우 중요하다. 각 파드에는 <b>고유한 IP 주소</b>가 부여되며, 이를 통해 다른 파드와 <b>직접 통신</b>할 수 있다. Kubernetes는 <b>CNI(Container Networking Interface) 플러그인</b>을 사용하여 파드 네트워크 인터페이스를 구성하고, 파드 간 격리(isolation)를 제공한다. 또한 Kubernetes는 <b>로드 밸런싱, 서비스 디스커버리(service discovery), 인그레스(ingress)</b>와 같은 네트워킹 서비스를 제공하여, <b>외부 트래픽이 파드 및 서비스에 접근</b>할 수 있도록 한다. 이러한 서비스들은 <b>Service, Ingress, NetworkPolicy</b>와 같은 Kubernetes 오브젝트로 구현된다. 네트워킹과 파드 간 통신은 <b>확장성, 신뢰성, 유연성</b>을 보장하는 데 필수적이다.</p>

  <hr>
  <h3>서비스의 외부 접근 (External Access to Services)</h3>
  <p>Kubernetes(k8s) 서비스에 대한 <b>외부 접근</b>은 클러스터 내에서 실행 중인 <b>파드와 서비스에 외부 클라이언트가 접속</b>할 수 있도록 해준다. k8s에서 서비스에 외부 접근을 가능하게 하는 방법에는 <b>NodePort, LoadBalancer, Ingress</b> 등이 있다. 특히 <b>Ingress</b>는 Kubernetes 오브젝트로, <b>URL이나 호스트 기반의 트래픽 라우팅</b>을 통해 외부 접근을 유연하게 관리할 수 있다. 외부 접근은 <b>Kubernetes 배포의 확장성과 신뢰성</b>을 보장하기 위해 필수적이다.</p>

  <hr>
  <h3>로드 밸런싱 (Load Balancing)</h3>
  <p>Kubernetes에서 로드 밸런싱은 Service 오브젝트를 사용하여 네트워크 트래픽을 여러 파드나 노드에 분산하는 것을 의미한다. Service는 여러 파드 집합에 대해 안정적인 네트워크 엔드포인트를 제공하며, 이를 통해 다른 파드나 외부 클라이언트가 단일 IP 주소와 DNS 이름으로 접근할 수 있게 한다. Kubernetes는 Service를 위한 세 가지 로드 밸런싱 알고리즘을 제공한다.
    <ul>
        <li><b>라운드 로빈 (Round-Robin):</b> 요청을 순차적으로 분배</li>
        <li><b>최소 연결 (Least Connections):</b> 현재 연결이 가장 적은 파드로 분배</li>
        <li><b>IP 해시 (IP Hash):</b> 클라이언트 IP 기반으로 요청을 특정 파드에 매핑</li>
    </ul>
    로드 밸런싱은 Kubernetes 네트워킹의 핵심 요소로, 클러스터 전반에 걸쳐 효율적이고 신뢰성 있는 트래픽 분산을 보장한다.
  </p>
</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Configuration Management</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <h3>시크릿 (Secrets)</h3>
  <p>Kubernetes <b>Secret</b>은 <b>비밀번호, 토큰, API 키</b>와 같은 <b>민감한 데이터</b>를 안전하게 저장하는 데 사용된다. 시크릿은 <b>수동 또는 자동으로 생성</b>할 수 있으며, <b>etcd</b>에 저장된다. 또한 시크릿은 파드 내에서 <b>파일 또는 환경 변수</b>로 마운트될 수 있으며, 접근 권한은 <b>Kubernetes RBAC(Role-Based Access Control)</b>으로 관리할 수 있다. 하지만 시크릿에는 몇 가지 제한 사항이 있다. 예를 들어 <b>크기 제한</b>이 있으며, <b>한 번 생성되면 업데이트할 수 없다</b>는 점이다. 따라서 Kubernetes에서 <b>보안 애플리케이션을 구축하기 위해 시크릿을 이해하는 것은 매우 중요하다.</b></p>

  <hr>
  <h3>컨피그맵 (ConfigMaps)</h3>
  <p><b>ConfigMap</b>은 Kubernetes 클러스터에서 실행되는 애플리케이션이 사용할 <b>설정 데이터를 저장</b>하는 방법이다. ConfigMap은 <b>키-값(Key-Value) 저장소</b> 형태로, 데이터베이스 URL, 자격 증명(Credentials), API 키, 그 외 애플리케이션에서 사용하는 다양한 설정 데이터를 담을 수 있다.</p>

</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Resource Management</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <h3>리소스 사용 모니터링 및 최적화 (Monitoring and Optimizing Resource Usage)</h3>
  <p>Kubernetes(k8s)에서 리소스 사용을 모니터링하고 최적화하는 것은 리소스를 효율적이고 효과적으로 활용하기 위해 매우 중요하다.
    <ul>
        <li><b>리소스 모니터링:</b> k8s는 Metrics Server를 제공하며, Prometheus를 k8s에 통합해 사용할 수도 있다. 또한 <b>CRI(Container Runtime Interface)</b>를 통해 컨테이너 단위의 리소스 사용 데이터를 모니터링할 수 있다.</li>
        <li><b>리소스 최적화:</b> </li>
        <ul>
            <li>적절한 <b>Requests와 Limits 설정</b> </li>
            <li><b>Horizontal Pod Autoscaling(HPA)</b> 활용</li>
            <li><b>파드 친화도/반친화도(Pod Affinity/Anti-Affinity) 규칙 적용</b> </li>
            <li><b>노드 선택(Node Selection) 제어</b> </li>
        </ul>
        이러한 방법들을 통해 리소스 경쟁(Resource Contention)을 줄이고, 리소스 활용률(Resource Utilization)을 개선할 수 있다.
    </ul>
    결과적으로, 리소스 사용을 모니터링하고 최적화함으로써 k8s는 애플리케이션이 효율적으로 실행되고, 리소스가 효과적으로 사용되도록 보장할 수 있다.
  </p>

  <hr>
  <h3>리소스 요청과 제한 설정 (Setting Resource Requests and Limits)</h3>
  <p>Kubernetes에서 **리소스 요청(requests)**과 **제한(limits)**은 컨테이너가 실행되기 위해 필요한 최소 및 최대 CPU와 메모리 양을 지정한다.
    <ul>
        <li><b>리소스 요청(Requests):</b> 스케줄러가 컨테이너를 충분한 리소스를 가진 노드에 배치할 수 있도록 보장한다.</li>
        <li><b>리소스 제한(Limits):</b> 컨테이너가 지나치게 많은 리소스를 사용하는 것을 방지하고, 리소스 할당량을 강제한다.</li>
    </ul>
    이 설정은 YAML의 resources 필드를 사용하여 파드(Pod) 또는 컨테이너 수준에서 구성할 수 있다. 리소스 요청과 제한을 올바르게 설정하는 것은 클러스터의 리소스를 최적화된 방식으로 활용하기 위해 매우 중요하다.
  </p>

  <hr>
  <h3>네임스페이스에 할당량 지정 (Assigning Quotas to Namespaces)</h3>
  <p>Kubernetes에서 네임스페이스에 **쿼터(Quota)**를 할당하는 것은 특정 리소스 그룹의 리소스 사용량을 제한하는 방법이다. 쿼터는 CPU, 메모리 같은 리소스뿐만 아니라, 네임스페이스 내 오브젝트 개수에도 설정할 수 있다. 이를 통해 클러스터 내에서 서로 다른 팀이나 프로젝트 간에 공정한 리소스 분배를 보장할 수 있다. 쿼터는 개별 네임스페이스 단위로도, 클러스터 전체 단위로도 적용할 수 있다. Kubernetes는 두 가지 유형의 쿼터를 지원한다.
    <ul>
        <li><b>하드 쿼터(Hard Quotas):</b> 엄격한 리소스 제한을 강제</li>
        <li><b>소프트 쿼터(Soft Quotas):</b> 일정 한도까지 초과 사용 허용</li>
    </ul>
    쿼터는 Kubernetes API 또는 YAML 설정 파일을 통해 관리할 수 있다.
  </p>

</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Monitoring and Logging</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <h3>가시성 엔진 (Observability Engines)</h3>
  <p>Kubernetes(k8s)에서 Observability(가시성)는 클러스터, 애플리케이션, 그리고 그 위에서 실행되는 서비스들의 내부 동작을 파악할 수 있는 능력을 의미한다. k8s에서 Observability Engine은 k8s 환경 내의 다양한 소스로부터 데이터를 수집, 분석, 시각화하는 것을 가능하게 해주는 도구나 플랫폼이다. k8s에서 잘 알려진 Observability Engine에는 Prometheus, Grafana, Jaeger, Elastic Stack(ELK) 등이 있다.</p>

  <hr>
  <h3>Logs</h3>
  <p>로그는 클러스터 내 노드에서 실행 중인 컨테이너화된 애플리케이션에 의해 생성된다. 이 로그들은 <u>kubectl logs</u> 명령어 뒤에 파드의 이름을 입력하여 접근할 수 있다. 기본적으로 이 명령어는 파드 내에서 가장 최근에 실행된 컨테이너의 로그를 보여주지만, 명령어에 컨테이너 이름을 추가하면 특정 컨테이너의 로그를 지정해서 볼 수 있다. 명령어에 <u>-f</u> 플래그를 추가하면 로그를 실시간으로 따라가며 확인할 수 있다. 또한 Kubernetes에는 <b>EFK 스택이나 Prometheus 스택</b>과 같은 서드파티 로깅 솔루션도 제공되며, 이를 통해 대규모 애플리케이션에 대한 더 발전된 로깅 기능과 확장성을 지원할 수 있다.</p>

  <hr>
  <h3>Metrics</h3>
  <p>모니터링해야 할 메트릭에는 CPU 사용량, 메모리 사용량, 네트워크 사용량, 디스크 사용량, API 서버 메트릭, 파드 및 컨테이너 메트릭, 클러스터 수준 메트릭이 포함된다. 이러한 메트릭들은 클러스터, 노드, 그리고 클러스터에서 실행 중인 애플리케이션의 성능과 상태에 대한 통찰을 제공한다. Kubernetes는 Prometheus, Grafana, Kubernetes Dashboard와 같은 도구를 제공하여 이러한 메트릭들을 수집하고 분석할 수 있도록 한다. 이 메트릭들을 모니터링함으로써 관리자는 성능 문제를 식별하고, 클러스터를 더 나은 성능과 확장성을 위해 최적화할 수 있다.</p>

  <hr>
  <h3>Traces</h3>
  <p>Kubernetes에서 트레이싱(Tracing)은 Jaeger나 Zipkin과 같은 도구를 사용하여 시스템의 다양한 컴포넌트를 거치는 요청의 흐름을 모니터링하는 것을 의미한다. OpenTracing과 OpenCensus는 클러스터에서 실행되는 다양한 컴포넌트와 애플리케이션 전반에 걸쳐 일관된 방식으로 트레이스를 수집할 수 있도록 한다. 트레이싱은 성능 병목 현상을 식별하고, 문제를 디버깅하며, 시스템을 더 나은 성능과 확장성을 위해 최적화하는 데 도움이 된다. Kubernetes에서 트레이스를 모니터링함으로써 관리자는 문제를 식별하고 교정 조치를 취해 효율적인 시스템 성능을 보장할 수 있다.</p>

  <hr>
  <h3>Resource Health</h3>
  <p>Kubernetes에서 리소스 상태(Resource Health) 모니터링은 파드, 노드, 컨테이너와 같은 리소스의 상태와 가용성을 모니터링하는 것을 의미한다. 이를 통해 관리자는 Kubernetes Dashboard, Prometheus, Grafana와 같은 도구를 사용하여 시스템의 성능과 가용성에 영향을 줄 수 있는 문제를 식별하고 해결할 수 있다. 리소스 상태 모니터링은 또한 시스템이 장애에 대해 탄력성을 가지도록 하고, 장애 발생 시 빠르게 복구할 수 있도록 돕는다. 이는 Kubernetes 클러스터를 관리하는 데 중요한 부분이며, 시스템의 신뢰성, 가용성, 확장성을 보장한다.</p>

</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Autoscaling</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <h3>클러스터 오토스케일링(Cluster Autoscaling)</h3>
  <p>Kubernetes에서 오토스케일링(Autoscaling)은 수요에 따라 디플로이먼트나 파드 집합에 할당된 리소스를 조정하는 것을 의미한다. 여기에는 <b>수평 파드 오토스케일링(Horizontal Pod Autoscaling, HPA)</b>과 <b>수직 파드 오토스케일링(Vertical Pod Autoscaling, VPA)</b>이 포함되며, 각각 파드 복제본 수를 늘리거나 줄이고, 리소스 요청과 제한을 조정한다. 오토스케일링은 <b>클러스터 오토스케일링(Cluster Autoscaling)</b>과 함께 사용되어 리소스를 효율적으로 할당하고 애플리케이션의 응답성을 보장할 수 있다. 이는 <b>변동이 심한 워크로드나 트래픽 급증</b>을 처리하는 데 유용하다.</p>

  <hr>
  <h3>Horizontal Pod Autoscaler(HPA)</h3>
  <p>Horizontal Pod Autoscaler(HPA)는 Kubernetes의 기능으로, 실행 중인 워크로드의 현재 수요에 따라 파드의 복제본(replica) 수를 자동으로 조정한다. HPA 컨트롤러는 파드의 CPU 사용량이나 다른 메트릭을 모니터링하고, 지정된 목표를 충족하기 위해 파드 복제본 수를 조정한다. 이를 통해 워크로드가 트래픽과 수요 증가를 처리하면서도 클러스터 리소스가 과부하되지 않도록 보장할 수 있다.</p>

  <hr>
  <h3>Vertical Pod Autoscaler(VPA)</h3>
  <p>Vertical Pod Autoscaler(VPA)는 Kubernetes의 기능으로, 파드 내 컨테이너들의 리소스 제한을 자동으로 조정하는 과정을 담당한다. HPA(Horizontal Pod Autoscaler)가 파드의 복제본(replica) 수를 조정하는 것과 달리, VPA는 파드 컨테이너에 할당된 리소스를 조정한다. 즉, 각 컨테이너의 실제 사용량에 따라 <b>리소스 요청(requests)과 리소스 제한(limits)</b>을 자동으로 조정한다.</p>

</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Scheduling</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>Kubernetes에서 스케줄링(Scheduling)은 워크로드를 클러스터 내 특정 노드에 할당하는 과정을 의미한다. Kubernetes 스케줄러는 <b>리소스 가용성, 노드 적합성, 워크로드 우선순위</b>와 같은 요소들을 기반으로 스케줄링 결정을 내린다. 이를 통해 클러스터 전반에 걸쳐 워크로드를 균형 있게 분산시켜 <b>효율적인 리소스 활용</b>을 보장하고, 특정 노드의 과부하를 방지한다. 스케줄링은 또한 <b>지리적 위치, 하드웨어 요구사항, 애플리케이션 특수 요구사항</b>과 같은 요소들도 고려한다.</p>

  <hr>
  <h3>Scheduling Basics</h3>
  <p>스케줄링은 리소스 가용성, 라벨(labels), 친화도/반친화도 규칙(affinity/anti-affinity rules), 테인트(taints), 톨러레이션(tolerations) 등의 기준에 따라 파드를 워커 노드에 할당하는 것을 포함한다. 파드(Pod)는 k8s에서 배포 가능한 가장 작은 단위로, 동일한 네트워크 네임스페이스를 공유하는 하나 이상의 컨테이너로 구성된다. 스케줄러는 파드를 노드에 할당하는 역할을 담당하며, 라벨은 매칭에 사용된다. 친화도/반친화도 규칙은 다른 파드나 노드와의 관계에 따라 파드가 어떻게 스케줄링될지를 결정한다. 또한 QoS(Quality of Service)는 파드의 리소스 요구 사항에 따라 스케줄링 우선순위를 지정하는 데 사용된다.</p>

  <hr>
  <h3>Taints and Tolerations</h3>
  <p>Kubernetes에서 테인트(taint)와 톨러레이션(toleration)은 라벨을 기반으로 특정 노드에 파드가 스케줄링되는 것을 제한하거나 허용하는 데 사용된다. <b>테인트(Taint)</b>는 노드에 적용되는 라벨로, 특정 제약이나 요구사항이 있음을 나타낸다. <b>톨러레이션(Toleration)</b>은 파드에 적용되는 라벨로, 해당 파드가 특정 테인트를 허용할 수 있음을 의미한다. 노드에 테인트가 설정되어 있으면, 그에 맞는 톨러레이션을 가진 파드만 해당 노드에 스케줄링될 수 있다. 이 기능은 중요한 워크로드와 비중요 워크로드를 분리하거나, 특정 작업을 위해 노드를 예약하거나, 노드의 과부하를 방지하는 등의 다양한 목적에 유용하다.</p>

  <hr>
  <h3>토폴로지 분산 제약 조건(Topology Spread Constraints)</h3>
  <p>Topology Spread Constraints은 클러스터의 토폴로지 전반에 걸쳐 파드가 고르게 분산되도록 보장한다. 이 제약 조건은 노드, 존(zones), 랙(racks)과 같은 특정 수준에서 특정 유형의 파드가 실행될 수 있는 개수에 대한 규칙을 정의한다. 또한 이러한 제약 조건은 특정 요구사항에 맞게 커스터마이징할 수 있으며, 예를 들어 중요한 워크로드가 여러 존에 분산되도록 설정할 수 있다. 이를 통해 단일 장애 지점을 방지하고, 리소스 과부하를 막으며, 워크로드의 균형 잡힌 분배를 촉진하여 애플리케이션의 복원력을 향상시킨다. 이러한 제약 조건은 Kubernetes API 또는 명령줄 인터페이스를 통해 추가할 수 있다.</p>

  <hr>
  <h3>파드 우선순위(Pod Priorities)</h3>
  <p>Kubernetes에서 파드 우선순위(Pod Priorities)는 리소스에 대한 경쟁 수요가 있을 때, 어떤 파드가 노드에 먼저 스케줄링될지를 결정한다. 각 파드에는 숫자 형태의 우선순위 값이 할당되며, 값이 높을수록 더 높은 우선순위를 가진다. 스케줄러는 노드 적합성, 테인트와 톨러레이션, 친화도 및 반친화도 규칙 등을 고려하면서, 스케줄된 파드들의 총 우선순위를 극대화하도록 동작한다. 우선순위는 비즈니스 로직이나 애플리케이션 요구사항에 따라 수동 또는 자동으로 설정할 수 있다. 이를 통해 중요한 워크로드가 필요한 리소스를 우선적으로 확보하고 먼저 스케줄링되며, 낮은 우선순위의 워크로드는 리소스가 여유 있을 때 스케줄링된다.</p>

  <hr>
  <h3>축출(Evictions)</h3>
  <p>Evictions은 리소스 제약이나 파드 실패와 같은 이유로 노드에서 실행 중인 파드를 종료하거나 삭제하는 것을 의미한다. 축출은 시스템에 의해 자동으로 발생할 수도 있고, 관리자가 API를 통해 수동으로 실행할 수도 있다. 축출은 파드가 리소스를 정리할 수 있도록 하는 <b>우아한(Graceful) 축출</b>일 수도 있고, 즉시 파드를 종료하는 <b>강제(Forceful) 축출</b>일 수도 있다. Kubernetes는 축출을 효과적으로 처리하고 서비스 중단을 최소화하기 위해 <b>선점(Preemption)과 파드 중단 예산(Pod Disruption Budgets, PDB)</b>을 제공한다. 축출은 Kubernetes 클러스터를 관리하고 유지하는 데 필요하며, Kubernetes는 이를 처리하기 위한 다양한 도구를 제공한다.</p>

</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Storage and Volumes</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <h3>CSI drivers</h3>
  <p>Kubernetes에서 CSI(Container Storage Interface) 드라이버는 스토리지 제공자가 Kubernetes와 통합하여 컨테이너화된 애플리케이션에 <b>영구 스토리지(persistent storage)</b>를 제공할 수 있는 표준 방식을 제공한다. 이 드라이버들은 개별적인 컨테이너화된 프로세스로 동작하며, 잘 정의된 API를 통해 Kubernetes와 통신한다. CSI 드라이버를 사용하면 Kubernetes는 다양한 스토리지 시스템에 접근할 수 있으며, <b>스냅샷(snapshotting) 및 복제(cloning)</b>와 같은 고급 기능도 제공할 수 있다.</p>

  <hr>
  <h3>상태 저장 애플리케이션(stateful applications)</h3>
  <p>Kubernetes에서, 스토리지는 상태 저장 애플리케이션에 있어 핵심 구성 요소이다. 이러한 애플리케이션들은 애플리케이션의 여러 복제본에 걸쳐 사용 가능한 영구 데이터 스토리지를 필요로 한다. Kubernetes는 볼륨, 퍼시스턴트 볼륨, 스토리지 클래스 등을 포함한 여러 스토리지 옵션을 제공한다. 볼륨은 Kubernetes에서 스토리지의 기본 빌딩 블록이다. 볼륨은 애플리케이션을 실행하는 컨테이너에서 접근 가능한 디렉토리이며, 호스트 디렉토리, 클라우드 제공자의 디스크, 네트워크 스토리지 시스템과 같은 다양한 스토리지 유형에 의해 지원될 수 있다. 볼륨은 Kubernetes에 의해 생성되고 관리되며, 파드 정의의 일부로 컨테이너에 마운트될 수 있다.</p>

</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Deployment Patterns</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <h3>Blue Green Deployments</h3>
  <p>이것은 Kubernetes에서 애플리케이션의 새로운 버전을 배포하기 위해 사용되는 배포 전략으로, 현재 버전(블루)과 새로운 버전(그린)을 각각 실행하는 두 개의 동일한 프로덕션 환경을 운영한다. 그린 환경이 완전히 테스트된 후, 트래픽은 블루 환경에서 그린 환경으로 라우팅되며, 이를 통해 사용자에게 매끄러운 전환을 제공하고 다운타임이나 서비스 중단을 피할 수 있다. Kubernetes에서 블루-그린 배포는 배포 전략, 트래픽 라우팅, 로드 밸런싱을 포함한 다양한 도구와 기법을 사용하여 구현할 수 있다.</p>

  <hr>
  <h3>CI/CD Integration</h3>
  <p>CI/CD 패턴에서 애플리케이션을 Kubernetes에 빌드, 테스트, 배포하는 과정은 완전히 자동화된다. CI 파이프라인은 컨테이너 이미지를 생성하고, 테스트를 실행하며, 그것을 레지스트리에 푸시한다. 그 후 CD 파이프라인은 Kubernetes 매니페스트나 Helm 차트를 업데이트하고, Argo CD, Flux, kubectl 같은 도구를 사용하여 클러스터에 적용한다. 이를 통해 배포는 일관적이고, 반복 가능하며, 빠르게 이루어진다.</p>

  <hr>
  <h3>GitOps</h3>
  <p>GitOps는 선언적 구성(declarative configuration)을 위한 진실의 원천(source of truth)으로 Git 저장소를 사용하여 인프라와 애플리케이션을 관리하는 일련의 방법론이다. Kubernetes에서 GitOps는 시스템의 원하는 상태(desired state)와 실제 상태(actual state) 모두에 대해 Git을 단일 진실의 원천으로 사용하고, 배포 및 관리 작업을 자동화하며, 종종 지속적 배포(Continuous Delivery, CD) 관행과 함께 사용된다. 그 결과 인프라와 애플리케이션을 관리하는 데 있어 더 일관되고, 신뢰할 수 있으며, 자동화된 접근 방식을 제공한다.</p>

  <hr>
  <h3>Helm Charts</h3>
  <p>Helm은 Kubernetes 패키지 매니저로, 재사용 가능하고 버전 관리되는 Helm 차트를 사용하여 복잡한 애플리케이션의 배포와 관리를 단순화한다. 이 차트들은 관련된 Kubernetes 리소스 집합을 기술하는 YAML 파일들로 구성되며, 값 파일(values files)과 Go 템플릿을 활용한 템플릿화를 통해 커스터마이징할 수 있다. Helm 차트는 다른 차트에 대한 의존성을 가질 수도 있고, Helm Hub와 같은 중앙 저장소에 보관되어 쉽게 공유되고 접근할 수 있다. Helm을 활용함으로써 팀은 애플리케이션 관리를 간소화하고, 중복 작업을 줄일 수 있다.</p>

  <hr>
  <h3>카나리 배포(Canary Deployments)</h3>
  <p>Canary Deployments는 Kubernetes에서 애플리케이션의 새로운 버전을 점진적으로 배포하는 기법으로, 소수의 사용자나 트래픽만 새로운 버전으로 보내고 대다수는 기존 버전을 계속 사용하도록 한다. 이 방식은 전체 업데이트를 적용하기 전에 실제 환경에서 새로운 버전을 테스트할 수 있게 해준다. Kubernetes에서 카나리 배포는 Istio, Linkerd, Nginx와 같은 도구를 사용하거나, 배포 전략 및 트래픽 라우팅과 같은 내장 기능을 통해 구현할 수 있다.</p>

  <hr>
  <h3>Kubernetes(쿠버네티스)</h3>
  <p>쿠버네티스, 줄여서 K8s라고도 불리며, 컨테이너화된 애플리케이션의 배포, 확장, 관리를 자동화하는 오픈 소스 컨테이너 오케스트레이션 플랫폼이다. 이를 통해 개발자는 코드 작성에 집중할 수 있고, Kubernetes는 그 기반 인프라를 처리한다. Kubernetes는 선언적 구성 파일을 사용하여 애플리케이션의 원하는 상태(desired state)를 지정하며, 수요에 따라 애플리케이션을 자동으로 확장하거나, 장애 조치를 처리하고, 네트워킹과 스토리지를 관리할 수 있다. 이는 마이크로서비스와 컨테이너에 기반한 프로덕션 배포를 위해 클라우드 네이티브 아키텍처에서 널리 사용된다.</p>

</div>
</details>
