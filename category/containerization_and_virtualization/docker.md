---
layout: default
title: "Containerization vs Virtualization"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>Docker</h2>
  <p><b>도커(Docker)</b>는 경량의 이식 가능한 <b>컨테이너</b>를 사용하여 애플리케이션의 배포, 확장, 관리를 자동화하는 오픈소스 플랫폼이다. 컨테이너는 애플리케이션 실행에 필요한 <b>모든 의존성, 라이브러리, 설정 파일</b>을 포함한 독립적인 실행 단위로, 다양한 환경에서 일관된 애플리케이션 실행을 가능하게 한다.</p>

  <h3 style="color: #0366d6;">컨테이너란?</h3>
  <p><b>컨테이너(Containers)</b>는 경량이고 이식 가능하며 격리된 소프트웨어 환경으로, 애플리케이션을 그 <b>의존성들과 함께 패키징</b>하여 다양한 플랫폼에서 일관되게 실행될 수 있도록 한다. 컨테이너는 개발, 배포, 관리 과정을 단순화하며, <b>기반 인프라와 상관없이 안정적으로 애플리케이션이 실행</b>되도록 보장한다.</p>

  <h3 style="color: #0366d6;">컨테이너의 필요성</h3>
  <p>컨테이너는 <b>실행 환경을 표준화</b>하여 팀 작업 시 발생하는 환경 불일치 문제를 해결한다. 컨테이너가 등장하기 전에는 팀원이 공유한 프로젝트를 실행하기 위해 로컬 환경을 설정하는 데 많은 시간이 소요되었고, 이로 인해 흔히 <b>"내 컴퓨터에서는 잘 되는데(works on my machine)"</b>라는 문제가 발생하곤 했다.</p>

  <h3 style="color: #0366d6;">Bare Metal vs VMS vs Containers</h3>
  <p><b>베어 메탈(Bare Metal)</b>은 애플리케이션을 <b>하드웨어 위에서 직접 실행</b>하여 최고의 성능을 제공하지만, 유연성이 제한된다. <b>가상 머신(VM)</b>은 하이퍼바이저를 사용해 여러 운영체제 인스턴스를 실행하며, 강력한 격리를 제공하지만 오버헤드가 크다. <b>컨테이너(Container)</b>는 호스트 운영체제 커널을 공유하여 VM보다 가볍고 효율적인 격리를 제공하면서도 이식성을 유지한다.</p>

  <h3 style="color: #0366d6;">Docker와 OCI</h3>
  <p><b>OCI(Open Container Initiative)</b>는 리눅스 재단이 주도하는 프로젝트로, <b>컨테이너 포맷과 런타임에 대한 업계 표준</b>을 만드는 것을 목표로 한다. 그 주된 목적은 정의된 기술 사양을 통해 컨테이너 환경의 <b>호환성과 상호운용성</b>을 보장하는 것이다.</p>
</section>

<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Underlying Technologies</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>도커 컨테이너는 <b>리눅스 커널 기술</b>을 활용하여 격리와 자원 관리를 수행한다.</p>
  <ul>
    <li><strong>네임스페이스(Namespaces):</strong> 프로세스를 격리한다.</li>
    <li><strong>cgroups(Control Groups):</strong> 자원 사용 한계를 설정한다.</li>
    <li><strong>Union 파일시스템(Union Filesystems):</strong> 효율적인 계층형 스토리지를 제공한다.</li>
  </ul>
  <p>이러한 기술 덕분에 도커 컨테이너는 <b>호스트 커널을 공유하면서도 경량, 이식성, 보안성</b>을 갖춘 환경을 제공한다.</p>

  <hr>
  <h3>네임스페이스란?</h3>
  <p>도커 네임스페이스(Docker Namespaces)는 <b>리눅스 커널 기능</b>으로, 전역 시스템 자원의 분리된 인스턴스를 제공하여 컨테이너를 위한 격리된 환경을 만든다. 도커는 <b>PID, NET, MNT, UTS, IPC, USER 네임스페이스</b>를 활용해 각 컨테이너가 자신만의 고유한 자원을 가지고 있다고 인식하도록 하여, <b>경량·이식 가능·보안성 있는 컨테이너화</b>를 가능하게 한다.</p>

  <hr>
  <h3>cgroups(Control Groups)</h3>
  <p><b>cgroups</b>는 리눅스 커널 기능으로, 프로세스 그룹에 대해 <b>CPU, 메모리, I/O 같은 시스템 자원을 제한하고 관리</b>한다. 도커는 cgroups를 사용하여 컨테이너의 자원 사용을 제약함으로써 <b>예측 가능한 성능을 보장</b>하고, 컨테이너가 과도한 시스템 자원을 소모하지 않도록 한다.</p>

  <hr>
  <h3>Union Filesystems</h3>
  <p><b>Union 파일시스템(UnionFS)</b>은 여러 디렉토리를 원본을 수정하지 않고 <b>겹쳐서(overlay) 하나의 가상 계층형 파일 구조</b>를 만드는 기술이다. 도커는 이를 활용해 디렉토리 내용을 분리된 상태로 유지하면서도 하나로 마운트하여, <b>중복을 최소화하고 이미지 크기를 줄이는 계층형 파일시스템 방식</b>으로 스토리지를 효율적으로 관리한다.</p>

</div>
</details>


<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Installation/Setup</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>도커(Docker)는 설치와 설정을 쉽게 하고 <b>GUI 기능</b>을 제공하는 데스크톱 애플리케이션인 <b>Docker Desktop</b>을 제공한다. 대안으로, 그래픽 인터페이스 구성 요소 없이 <b>명령줄 전용 기능</b>만을 제공하는 <b>Docker Engine</b>을 설치할 수도 있다.</p>

  <hr>
  <h3>Docker Desktop(Win/Mac/Linux)</h3>
  <p><b>Docker Desktop</b>은 Windows, macOS, Linux에서 사용할 수 있는 <b>GUI 기반 종합 개발 환경</b>이다. 이 환경에는 <b>Docker Engine, CLI, Buildx, Extensions, Compose, Kubernetes, 자격 증명 헬퍼(credentials helper)</b> 등이 포함되어 있어, 데스크톱 플랫폼에서 컨테이너 개발에 필요한 모든 것을 제공한다.</p>

  <hr>
  <h3>Docker Engine(Linux)</h3>
  <p><b>Docker Engine</b>은 컨테이너를 생성·관리하고 이미지를 빌드하며, <b>Docker API</b>를 제공하는 <b>오픈소스 컨테이너 런타임의 핵심</b>이다. 이 엔진은 Linux, Windows, macOS에서 실행되며, <b>Docker Desktop의 기반</b>이자 서버에서 독립적으로 설치해 사용할 수 있는 도커 환경을 제공한다.</p>
</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Docker Basics</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>도커(Docker)</b>는 경량의 이식 가능한 <b>컨테이너</b> 안에서 애플리케이션을 빌드, 패키징, 배포하는 과정을 단순화하는 플랫폼이다. 주요 구성 요소로는 <b>Dockerfile(빌드 지침), 이미지(스냅샷), 컨테이너(실행 인스턴스)</b>가 있으며, 기본 명령어로는 이미지 다운로드, Dockerfile 빌드, 포트 매핑을 통한 컨테이너 실행, 컨테이너 및 이미지 관리 등이 있다.</p>

  <h3>컨테이너란?</h3>
  <p>컨테이너는 애플리케이션 실행에 필요한 <b>모든 의존성(라이브러리, 바이너리, 설정 파일)</b>을 포함한 <b>경량·독립·실행 가능한 소프트웨어 패키지</b>다. 컨테이너는 애플리케이션을 환경으로부터 격리하여, 다양한 시스템에서 일관되게 동작하도록 보장한다.</p>

  <h3>도커 구성 요소</h3>
  <ul>
    <li><strong>Dockerfile:</strong> Docker 이미지를 빌드하기 위한 명령어를 담은 텍스트 파일</li>
    <li><strong>Docker Image:</strong> Dockerfile로부터 생성된 컨테이너 스냅샷. Docker Hub 같은 레지스트리에 저장·다운로드 가능</li>
    <li><strong>Docker Container:</strong> 이미지를 기반으로 실행되는 컨테이너 인스턴스</li>
  </ul>
</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Data Persistence</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>도커(Docker)는 애플리케이션과 그 의존성을 포함한 코드를 <b>호스트 운영체제로부터 분리된 격리된 컨테이너</b>로 실행할 수 있게 해준다. 컨테이너는 기본적으로 <b>휘발성(ephemeral)</b>이므로, 컨테이너가 종료되면 그 안에 저장된 데이터는 모두 사라진다. 이 문제를 해결하고 컨테이너의 라이프사이클 전반에서 데이터를 보존하기 위해, 도커는 다양한 <b>데이터 영속성(persistence) 방법</b>을 제공한다.</p>

  <hr>
  <h3>Ephemeral Container Filesystem</h3>
  <p>기본적으로 도커 컨테이너 내부의 스토리지는 <b>휘발성(ephemeral)</b>이다. 즉, 컨테이너 안에서 발생한 데이터 변경이나 수정은 컨테이너가 실행되는 동안만 유지되며, 컨테이너가 중지되고 제거되면 모든 관련 데이터가 사라진다. 이는 도커 컨테이너가 본질적으로 <b>무상태(stateless)</b>로 설계되었기 때문이다. 이러한 일시적·단기 저장소는 <b>"휘발성 컨테이너 파일 시스템(ephemeral container file system)"</b>이라 불린다. 이 기능은 도커의 중요한 특징으로, 컨테이너 상태에 신경 쓰지 않고도 애플리케이션을 <b>빠르고 일관되게 다양한 환경에 배포</b>할 수 있도록 한다.</p>

  <hr>
  <h3>Volume Mounts(볼륨 마운트)</h3>
  <p><b>Volume Mounts</b>는 호스트 시스템의 폴더나 파일을 컨테이너 내부의 폴더나 파일에 <b>매핑</b>하는 방식이다. 이를 통해 컨테이너가 제거되더라도 데이터가 <b>컨테이너 외부에 보존</b>될 수 있다. 또한 여러 컨테이너가 동일한 볼륨을 공유할 수 있어, 컨테이너 간 <b>데이터 공유</b>를 쉽게 할 수 있다.</p>

  <hr>
  <h3>Bind Mounts(바인드 마운트)</h3>
  <p><b>바인드 마운트(Bind Mounts)</b>는 볼륨에 비해 기능이 제한적이다. 바인드 마운트를 사용할 때는 <b>호스트 머신의 파일이나 디렉토리</b>가 컨테이너 안에 마운트되며, 이 파일이나 디렉토리는 호스트 머신의 <b>절대 경로</b>로 참조된다. 반대로 <b>볼륨(Volume)</b>을 사용할 때는 호스트 머신의 <b>도커 전용 스토리지 디렉토리</b> 안에 새로운 디렉토리가 생성되고, 해당 디렉토리의 내용은 도커가 직접 관리한다.</p>

</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Using 3rd Party Images</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>서드파티 이미지(Third-party Images)</b>는 <b>Docker Hub</b> 또는 다른 컨테이너 레지스트리에서 제공되는 <b>사전 빌드된 도커 컨테이너 이미지</b>다. 이 이미지는 개인이나 조직이 생성·관리하며, 사용자는 이를 기반으로 자신의 컨테이너화된 애플리케이션을 시작할 수 있다.</p>

  <hr>
  <h3>Using Databases</h3>
  <p>데이터베이스를 도커 컨테이너에서 실행하면 <b>개발 과정을 간소화</b>하고 <b>배포를 쉽게</b> 할 수 있다.Docker Hub에는 MySQL, PostgreSQL, MongoDB와 같은 인기 있는 데이터베이스를 위한 <b>미리 만들어진 이미지</b>가 다수 제공된다.</p>

  <hr>
  <h3>Command Line Utilities</h3>
  <p>도커 이미지는 <b>명령줄 유틸리티</b>나 <b>독립 실행형 애플리케이션</b>을 포함할 수 있으며, 이를 컨테이너 내부에서 실행할 수 있다.</p>
</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Building Container Images</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>컨테이너 이미지는 애플리케이션 실행에 필요한 <b>코드, 런타임, 시스템 도구, 라이브러리, 설정</b>을 모두 포함한 <b>실행 가능한 패키지</b>다. 커스텀 이미지를 빌드하면, 모든 의존성을 포함한 애플리케이션을 Docker가 지원하는 어떤 플랫폼에서든 원활하게 배포할 수 있다. 컨테이너 이미지를 빌드하는 핵심 요소는 <b>Dockerfile</b>이다. Dockerfile은 도커 이미지를 어떻게 구성할지에 대한 <b>명령어가 담긴 스크립트</b>로, 각 명령어는 이미지 안에서 <b>새로운 레이어(layer)</b>를 생성한다. 이를 통해 변경 사항 추적이 쉬워지고 이미지 크기를 최소화할 수 있다.</p>

  <hr>
  <h3>Dockerfile</h3>
  <p><b>Dockerfile</b>은 도커 엔진이 이미지를 빌드할 때 사용하는 <b>명령어 목록을 담은 텍스트 문서</b>다. Dockerfile의 각 명령어는 이미지에 <b>새로운 레이어(layer)</b>를 추가하며, 도커는 이 명령어들을 기반으로 이미지를 빌드한다. 그 후, 빌드된 이미지를 이용해 컨테이너를 실행할 수 있다.</p>

  <hr>
  <h3>Efficient Layer Caching</h3>
  <p>컨테이너 이미지를 빌드할 때 도커는 새로 생성된 <b>레이어(layer)</b>를 캐시한다. 이후 다른 이미지를 빌드할 때 이 레이어들을 재사용할 수 있어, 빌드 시간을 줄이고 대역폭 사용을 최소화할 수 있다. 이 캐싱 메커니즘을 최대한 활용하려면, 레이어 캐싱을 효율적으로 사용하는 방법을 이해하는 것이 중요하다. 도커는 Dockerfile의 각 명령어(RUN, COPY, ADD 등)에 대해 새로운 레이어를 생성하며, <b>명령어가 이전 빌드 이후 변경되지 않았다면 기존 레이어를 재사용</b>한다.</p>

  <hr>
  <h3>Reducing Image Size</h3>
  <p>도커 이미지 크기를 줄이는 것은 <b>스토리지 최적화, 전송 속도 향상, 배포 시간 단축</b>을 위해 매우 중요하다. 주요 전략은 다음과 같다.</p>
  <ul>
    <li><b>Alpine Linux</b>와 같은 최소한의 베이스 이미지를 사용한다.</li>
    <li><b>멀티 스테이지 빌드(Multi-stage Build)</b>를 활용해 불필요한 빌드 도구를 제외한다.</li>
    <li>필요 없는 파일과 패키지를 제거한다.</li>
    <li>명령어를 결합해 레이어 수를 최소화한다.</li>
  </ul>
</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Container Registries</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>컨테이너 레지스트리(Container Registry)</b>는 도커 컨테이너 이미지를 위한 <b>중앙 집중식 저장소이자 배포 시스템</b>이다. 이를 통해 개발자는 애플리케이션을 이미지 형태로 손쉽게 공유하고 배포할 수 있다. 컨테이너 레지스트리는 다양한 운영 환경에 걸쳐 컨테이너 이미지를 <b>빠르고, 신뢰성 있게, 안전하게 배포</b>할 수 있게 해주므로, 컨테이너화된 애플리케이션의 배포에서 핵심적인 역할을 한다.</p>

  <hr>
  <h3>DockerHub</h3>
  <p><b>Docker Hub</b>은 클라우드 기반의 레지스트리 서비스로, 도커 컨테이너 이미지를 위한 <b>주요 공개 저장소</b> 역할을 한다. 사용자는 도커 허브를 통해 이미지를 <b>저장, 공유, 배포</b>할 수 있으며, 무료 공개 저장소와 유료 비공개 저장소 모두 제공된다. 또한 Docker CLI와 매끄럽게 통합되어 이미지를 쉽게 <b>푸시(push)·풀(pull)</b> 할 수 있다. Docker Hub에는 소프트웨어 공급업체가 관리하는 <b>공식 이미지</b>, 소스 코드 저장소와 연결된 <b>자동 빌드</b>, 그리고 저장소 이벤트에 따라 동작을 트리거할 수 있는 <b>웹훅(webhook)</b> 기능이 포함되어 있다.</p>

  <hr>
  <h3>DockerHub Alternatives</h3>
  <p>컨테이너 이미지는 <b>Docker Hub뿐만 아니라 다양한 레지스트리</b>에 저장될 수 있다. 현재 대부분의 주요 클라우드 플랫폼은 자체 컨테이너 레지스트리를 제공한다. 예를 들어,</p>
  <ul>
    <li><b>Google Cloud Platform</b> → Artifact Registry</li>
    <li><b>AWS</b> → Elastic Container Registry (ECR)</li>
    <li><b>Microsoft Azure</b> → Azure Container Registry (ACR)</li>
  </ul>
  <p>또한 <b>GitHub</b>도 자체 레지스트리를 제공하며, 이는 컨테이너 빌드를 <b>GitHub Actions 워크플로우와 통합</b>할 때 유용하다.</p>

  <hr>
  <h3>Image Tagging Best Practices</h3>
  <p>도커 이미지 태깅(Docker Image Tagging) 모범 사례는 <b>명확하고 일관성 있으며 유용한 라벨</b>을 만드는 데 초점을 맞춘다.</p>
  <ul>
    <li>릴리스를 위해 <b>시맨틱 버전(semantic versioning)</b>을 채택한다.</li>
    <li>프로덕션 환경에서는 모호한 <b>latest 태그 사용을 피한다.</b></li>
    <li>빌드 날짜나 Git 커밋 해시 같은 <b>관련 메타데이터</b>를 포함한다.</li>
    <li>환경별(개발, 스테이징, 운영 등)로 구분하는 전략을 사용한다.</li>
    <li>변형(variants)에 대해 <b>설명적인 태그</b>를 사용한다.</li>
    <li>CI/CD 파이프라인에서 태깅을 자동화한다.</li>
    <li>오래된 태그는 주기적으로 정리하고, 팀 전체가 따를 수 있도록 <b>규칙을 문서화</b>한다.</li>
  </ul>
  <p>이러한 모범 사례를 따르면 효율적인 이미지 관리가 가능해지고, 조직 내 협업이 더욱 원활해진다.</p>
</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Running Containers</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>docker run</b> 명령은 지정된 이미지로부터 새로운 컨테이너를 생성하고 시작한다. 이 명령은 <b>docker create</b>와 <b>docker start</b> 작업을 결합한 것으로, 컨테이너의 런타임 환경을 커스터마이즈할 수 있는 다양한 옵션을 제공한다. 사용자는 환경 변수를 설정하고, 포트와 볼륨을 매핑하며, 네트워크 연결을 정의하고, 리소스 제한을 지정할 수 있다. 이 명령은 백그라운드 실행을 위한 detached 모드, 셸 접근을 위한 interactive 모드, 그리고 이미지에 정의된 기본 명령을 재정의할 수 있는 기능을 지원한다. 일반적인 플래그에는 <b>-d</b> (detached 모드), <b>-p</b> (포트 매핑), <b>-v</b> (볼륨 마운트), <b>--name</b> (사용자 지정 컨테이너 이름 할당)이 포함된다. <b>docker run</b>을 이해하는 것은 도커 컨테이너를 효과적으로 배포하고 관리하는 데 기본적이다.</p>

  <hr>
  <h3>Running Containers</h3>
  <p>데이터베이스를 도커 컨테이너에서 실행하면 <b>개발 과정을 간소화</b>하고 <b>배포를 쉽게</b> 할 수 있다.Docker Hub에는 MySQL, PostgreSQL, MongoDB와 같은 인기 있는 데이터베이스를 위한 <b>미리 만들어진 이미지</b>가 다수 제공된다.</p>

  <hr>
  <h3>Docker Compose</h3>
  <p><b>Docker Compose</b>는 <b>docker-compose.yml</b>이라는 <b>YAML 파일</b>을 사용해 <b>멀티 컨테이너 애플리케이션</b>을 정의하고 실행하는 도구다. 이 파일에는 애플리케이션의 서비스, 네트워크, 볼륨이 정의되며, 단일 명령어로 전체 컨테이너화된 애플리케이션을 생성·관리·실행할 수 있어 오케스트레이션을 단순화한다.</p>

  <hr>
  <h3>Runtime Configuration Options</h3>
  <p>도커의 <b>런타임 구성 옵션(runtime configuration options)</b>은 컨테이너 환경을 강력하게 제어할 수 있게 해준다. 리소스 제한, 네트워크 설정, 보안 프로필, 로깅 드라이버 등을 조정해 성능을 최적화하고 보안을 강화할 수 있다. 또한 환경 변수 설정, 볼륨 마운트, 기본 동작 재정의 같은 옵션도 제공되어, 컨테이너를 <b>특정 요구사항에 맞게 조정</b>할 수 있다. 고급 사용자라면 <b>커널 기능(capabilities) 조정이나 재시작 정책(restart policies) 설정</b> 같은 기능도 활용할 수 있다. 명령줄 플래그나 Docker Compose 파일을 통해 이러한 옵션들을 지정할 수 있으며, 이를 통해 컨테이너가 <b>어디서 실행되든 안정적이고 일관되게 동작</b>하도록 보장할 수 있다.</p>
</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Container Security</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>컨테이너 보안(Container Security)은 컨테이너화된 애플리케이션을 <b>개발부터 배포, 실행 시점까지 보호</b>하기 위한 광범위한 관행과 도구들을 포함한다. 이는 컨테이너 이미지를 보호하고, 신뢰할 수 있으며 취약하지 않은 코드만 사용하도록 보장하며, 컨테이너 환경에 대한 강력한 접근 제어를 구현하고, 컨테이너가 <b>최소 권한 원칙</b>을 따르도록 구성하는 것을 포함한다. 또한 예상치 못한 동작을 모니터링하고, 컨테이너 간 통신을 보호하며, 호스트 환경의 보안을 유지하는 것도 포함된다. 효과적인 컨테이너 보안은 <b>DevSecOps 워크플로우에 자연스럽게 통합</b>되어, 개발 속도나 민첩성을 저해하지 않으면서도 컨테이너 라이프사이클 전반에 걸쳐 지속적인 가시성과 보호를 제공한다.</p>

  <hr>
  <h3>Image Security</h3>
  <p>이미지 보안(Image Security)은 도커 컨테이너를 환경에 배포할 때 매우 중요한 요소다. 사용하는 이미지가 <b>안전하고, 최신 상태이며, 취약점이 없는지</b>를 보장하는 것은 필수적이다. 이 섹션에서는 도커 이미지를 보호하고 관리하기 위한 <b>모범 사례와 도구</b>를 살펴본다. 공개 레지스트리에서 이미지를 가져올 때는 항상 신뢰할 수 있는 <b>공식 이미지(official images)</b>를 컨테이너화된 애플리케이션의 출발점으로 사용해야 한다. 공식 이미지는 도커에 의해 검증되며, 정기적으로 <b>보안 패치가 적용된 최신 상태</b>로 업데이트된다. 이러한 이미지는 <b>Docker Hub</b> 또는 다른 신뢰할 수 있는 레지스트리에서 찾을 수 있다.</p>

  <hr>
  <h3>Runtime Security</h3>
  <p>도커에서의 <b>런타임 보안(Runtime Security)</b>은 컨테이너 실행 중 안전성과 무결성을 보장하고, 컨테이너화된 애플리케이션이 실행될 때 발생할 수 있는 취약점이나 악의적 활동으로부터 보호하는 데 초점을 맞춘다. 이는 컨테이너 동작을 모니터링하여 이상 징후를 탐지하고, 권한을 제한하기 위한 접근 제어를 구현하며, 의심스러운 활동을 실시간으로 탐지하고 대응할 수 있는 도구를 사용하는 것을 포함한다. 효과적인 런타임 보안은 <b>검증된 이미지만 배포되도록 보장</b>하고, 시스템을 지속적으로 감사(audit)하여 규정 준수를 유지한다. 이를 통해 취약점 악용을 방지하고, 컨테이너 라이프사이클 전반에 걸쳐 원하는 보안 수준(Security Posture)을 유지하는 강력한 방어 계층을 제공한다.</p>

</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Docker CLI</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p><b>도커 커맨드 라인 인터페이스(Docker CLI)</b>는 도커 엔진과 상호작용하는 강력한 도구로, 개발자와 운영자가 컨테이너 및 관련 리소스를 <b>빌드, 관리, 트러블슈팅</b>할 수 있게 해준다.</p>
  <p>도커 CLI는 다양한 명령어를 제공하여 도커의 모든 측면을 제어할 수 있다.</p>
  <ul>
    <li>컨테이너 생성·관리: docker run, docker stop</li>
    <li>이미지 빌드: docker build</li>
    <li>네트워크 관리: docker network</li>
    <li>스토리지 관리: docker volume</li>
    <li>시스템 상태 확인: docker ps, docker info</li>
  </ul>
  <p>직관적인 문법과 유연성을 갖춘 Docker CLI는 복잡한 워크플로우 자동화, 개발 프로세스 단순화, 컨테이너화된 애플리케이션 유지보수를 쉽게 만들어준다. 따라서 도커 관리와 오케스트레이션을 위한 <b>기본적인 핵심 유틸리티</b>라 할 수 있다.</p>

  <hr>
  <h3>Docker Images</h3>
  <p>도커 이미지(Docker Images)는 소프트웨어 실행에 필요한 <b>애플리케이션 코드, 런타임, 라이브러리, 시스템 도구</b>를 모두 포함한 <b>경량의 독립 실행 패키지</b>다. 도커 이미지는 효율적인 저장을 위해 <b>레이어(layer)</b> 구조로 빌드되며, 컨테이너의 <b>청사진(blueprint)</b> 역할을 한다. 또한 Docker Hub 같은 레지스트리를 통해 공유될 수 있어, 다양한 환경에서 일관된 배포를 가능하게 한다.</p>

  <hr>
  <h3>Containers</h3>
  <p>컨테이너(Containers)는 애플리케이션을 실행하기 위해 <b>공유 운영체제 커널</b>을 사용하는 <b>격리된 경량 환경</b>으로, 서로 다른 컴퓨팅 환경에서도 일관성과 이식성을 보장한다. 컨테이너는 애플리케이션 실행에 필요한 <b>코드, 의존성, 설정</b>을 모두 캡슐화하여, 컨테이너화된 애플리케이션을 어디서나 손쉽게 이동하고 실행할 수 있도록 한다. 도커 CLI를 사용하면 <b>docker run</b>으로 컨테이너를 생성·시작하고, <b>docker ps</b>로 실행 중인 컨테이너를 확인하며, <b>docker stop</b>으로 중지하고, <b>docker exec</b>으로 실시간 상호작용할 수 있다. CLI는 개발자가 컨테이너를 <b>빌드, 제어, 디버깅</b>할 수 있는 강력한 인터페이스를 제공하여, 개발과 운영 워크플로우를 간소화한다.</p>

  <hr>
  <h3>Docker Volumes</h3>
  <p><b>도커 볼륨(Docker Volumes)</b>은 컨테이너 파일시스템 외부에서 데이터를 관리·저장하는 <b>영속적 스토리지 솔루션</b>으로, 컨테이너가 삭제되거나 재생성되더라도 데이터가 유지된다. 볼륨은 애플리케이션 데이터, 로그, 설정 파일처럼 컨테이너 재시작이나 업데이트 이후에도 보존이 필요한 데이터를 저장하는 데 이상적이다. 도커 CLI에서는 <b>docker volume create</b>로 새로운 볼륨을 정의하고, <b>docker volume ls</b>로 모든 볼륨을 확인하며, <b>docker run -v</b>로 특정 컨테이너에 볼륨을 마운트할 수 있다. 이 방식은 <b>데이터 무결성을 유지</b>하고, 백업 과정을 단순화하며, 컨테이너 간 데이터 공유를 지원하기 때문에 <b>상태 기반(stateful) 컨테이너 애플리케이션의 핵심 요소</b>가 된다.</p>

  <hr>
  <h3>Docker Networks</h3>
  <p><b>도커 네트워크(Docker Networks)</b>는 컨테이너들이 서로 및 외부 시스템과 통신할 수 있도록 하여, 마이크로서비스 아키텍처에 필요한 연결성을 제공한다. 도커는 기본적으로 <b>bridge, host, overlay</b>와 같은 여러 네트워크 유형을 제공하며, 이는 격리된 환경, 고성능 시나리오, 멀티 호스트 간 통신 등 다양한 사용 사례에 적합하다. 도커 CLI를 사용하면 <b>docker network create</b>로 커스텀 네트워크를 정의하고, <b>docker network ls</b>로 기존 네트워크를 조회하며, <b>docker network connect</b>로 컨테이너를 네트워크에 연결할 수 있다. 이러한 유연성 덕분에 개발자는 컨테이너 간 상호작용을 제어할 수 있으며, <b>분산 애플리케이션에서 안전하고 효율적인 통신</b>을 보장할 수 있다.</p>

</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Developer Experience</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>도커(Docker)는 애플리케이션을 <b>빌드, 테스트, 실행</b>할 때 일관되고 격리된 환경을 제공하여, 흔히 발생하는 <b>“내 컴퓨터에서는 잘 되는데(It works on my machine)” 문제</b>를 해결함으로써 개발자 경험을 크게 향상시킨다. 개발자는 도커를 사용해 애플리케이션과 의존성을 이식 가능한 <b>컨테이너</b>로 패키징할 수 있으며, 이를 통해 로컬 개발부터 스테이징, 프로덕션에 이르기까지 환경 간 <b>일관성</b>을 보장한다. 간단한 설정과 환경 재현성은 온보딩 속도를 높이고, 충돌을 최소화하며, 개발자가 설정 문제 해결보다 <b>코딩에 집중</b>할 수 있도록 한다. 또한 Docker Compose 같은 도구는 복잡한 멀티 컨테이너 애플리케이션을 빠르게 오케스트레이션할 수 있어, <b>프로토타이핑, 반복(iteration), 협업</b>을 쉽게 만들어 전체 개발 라이프사이클을 간소화한다.</p>

  <hr>
  <h3>Hot Reloading in Docker</h3>
  <p>레이어 캐싱(layer caching)을 활성화하면 이미지 빌드 속도를 높일 수 있지만, <b>코드가 바뀔 때마다 컨테이너 이미지를 다시 빌드</b>하고 싶지는 않다. 대신, 컨테이너 안의 애플리케이션 상태가 코드 변경 사항을 즉시 반영하도록 하고 싶다. 이를 달성하기 위해서는 <b>바인드 마운트(bind mounts)</b>와 <b>핫 리로딩(hot reloading) 유틸리티</b>를 조합해 사용할 수 있다.</p>

  <hr>
  <h3>Debuggers in Docker</h3>
  <p>컨테이너 기반 개발이 로컬 개발만큼 경쟁력을 가지려면, 우리는 <b>컨테이너 내부에서 디버거를 실행하고 연결할 수 있는 기능</b>이 필요하다.</p>

  <hr>
  <h3>Tests</h3>
  <p>우리는 테스트를 프로덕션과 가능한 한 유사한 환경에서 실행하기를 원하기 때문에, 이를 컨테이너 내부에서 수행하는 것이 가장 합리적이다. 이에는 <b>단위 테스트(Unit Tests), 통합 테스트(Integration Tests), 엔드투엔드 테스트(E2E Tests)</b>가 포함될 수 있으며, 모두 도커 컨테이너 안에서 실행되어 실제 시나리오를 시뮬레이션하면서 외부 의존성의 간섭을 피할 수 있다. 도커 CLI와 Docker Compose 같은 도구를 사용하면 <b>격리된 테스트 환경</b>을 만들고, 테스트를 병렬로 실행하며, 필요한 인프라를 자동으로 <b>생성(spin up)·해제(tear down)</b>할 수 있다.</p>

  <hr>
  <h3>Continuous Integration(CI)</h3>
  <p><b>지속적 통합(Continuous Integration, CI)</b>은 코드가 버전 관리 시스템에 푸시될 때마다 빌드, 테스트 등 특정 작업을 <b>자동으로 실행</b>하는 개념이다. 컨테이너의 경우, 우리가 하고 싶은 작업들은 다음과 같다.</p>
  <ul>
    <li>컨테이너 이미지 빌드</li>
    <li>테스트 실행</li>
    <li>컨테이너 이미지 취약점 스캔</li>
    <li>유용한 메타데이터로 이미지 태깅</li>
    <li>컨테이너 레지스트리에 푸시</li>
  </ul>
</div>
</details>

<!-- 설명 -->
<details>
<summary><span class="accordion-title" style="color: #000; font-weight: bold;">Deploying Containers</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>컨테이너 배포는 도커와 컨테이너화를 활용해 애플리케이션을 <b>더 효율적으로 관리하고, 손쉽게 확장하며, 환경 간 일관된 성능</b>을 보장하기 위한 핵심 단계다. 이 주제에서는 애플리케이션을 만들고 실행하기 위해 도커 컨테이너를 배포하는 방법에 대한 <b>개요</b>를 다룬다.</p>

  <hr>
  <h3>Nomad: Deploying Containers</h3>
  <p><b>Nomad</b>는 컨테이너화된 애플리케이션을 <b>배포, 관리, 확장</b>할 수 있게 해주는 <b>클러스터 관리자이자 스케줄러</b>다. Nomad는 노드 장애, 리소스 할당, 컨테이너 오케스트레이션을 자동으로 처리한다. 또한 Docker 컨테이너뿐만 아니라 다른 컨테이너 런타임과 <b>비(非)컨테이너화 애플리케이션</b>도 실행할 수 있다.</p>

  <hr>
  <h3>Docker Swarm</h3>
  <p><b>Docker Swarm</b>은 도커의 네이티브 컨테이너 오케스트레이션 도구로, 사용자가 여러 도커 호스트에 걸쳐 컨테이너를 <b>배포, 관리, 확장</b>할 수 있게 해준다. Swarm은 여러 도커 노드를 하나의 통합된 클러스터로 변환하여, 간단한 선언적 명령어를 통해 <b>고가용성, 로드 밸런싱, 자동 컨테이너 스케줄링</b>을 제공한다. 또한 <b>서비스 디스커버리, 롤링 업데이트, TLS 암호화를 통한 통합 보안</b> 같은 기능을 지원하여, 쿠버네티스(Kubernetes) 같은 더 복잡한 오케스트레이터에 비해 접근하기 쉬운 대안을 제시한다. Docker CLI와의 긴밀한 통합 및 간단한 설정 덕분에, Swarm은 <b>작은 규모에서 중간 규모의 배포</b>에 적합하며, 단순성과 직관적인 관리가 우선시되는 경우 유용하다.</p>

  <hr>
  <h3>Kubernetes</h3>
  <p>쿠버네티스(Kubernetes)**는 컨테이너화된 애플리케이션의 <b>배포, 확장, 관리</b>를 자동화하기 위해 설계된 <b>오픈소스 컨테이너 오케스트레이션 플랫폼</b>이다. 쿠버네티스는 컨테이너를 <b>파드(Pod)</b>라는 논리적 단위로 조직화하고, 선언적 설정을 통해 <b>서비스 디스커버리, 로드 밸런싱, 스케일링</b>을 관리함으로써 복잡한 컨테이너 워크로드를 처리할 수 있는 강력한 프레임워크를 제공한다. 또한, 클러스터 전반에 걸쳐 컨테이너를 배포할 수 있으며, 자동 재시작, 교체, 롤백 같은 <b>자가 치유(self-healing) 기능</b>을 통해 고가용성과 장애 허용성을 보장한다. 쿠버네티스는 방대한 생태계와 유연성을 바탕으로 <b>대규모 분산 애플리케이션 실행의 사실상 표준</b>이 되었으며, 운영을 단순화하고 컨테이너화된 워크로드의 안정성을 높여준다.</p>

  <hr>
  <h3>PaaS Options for Deploying Containers</h3>
  <p>컨테이너 배포를 위한 <b>PaaS(Platform-as-a-Service)</b> 옵션은 개발자가 <b>기반 인프라를 신경 쓰지 않고도</b> 컨테이너화된 애플리케이션을 빌드, 배포, 확장할 수 있는 간소화된 관리형 환경을 제공한다. 대표적인 PaaS 서비스로는 <b>Google Cloud Run, Azure App Service, AWS Elastic Beanstalk, Heroku</b> 등이 있으며, 이들은 컨테이너 오케스트레이션의 복잡성을 추상화하면서 <b>자동 확장, CI/CD 파이프라인 통합, 모니터링 기능</b>을 제공한다. 이러한 플랫폼은 서버 관리보다 <b>애플리케이션 로직</b>에 집중할 수 있게 하여, 팀이 빠르게 개발·배포할 수 있도록 지원하며, 최소한의 운영 부담으로 프로덕션 환경에서 컨테이너를 원활하게 실행할 수 있게 한다.</p>

</div>
</details>
