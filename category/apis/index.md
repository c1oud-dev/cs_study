---
layout: default
title: "APIs"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>APIs</h2>
  <p>
    API(애플리케이션 프로그래밍 인터페이스)는 서로 다른 소프트웨어 애플리케이션이 서로 통신하고 상호작용할 수 있도록 하는 정의된 규칙과 프로토콜의 집합입니다. 개발자가 서비스, 애플리케이션 또는 플랫폼의 내부 작동 방식을 이해하지 않고도 해당 기능이나 데이터에 접근하고 조작할 수 있는 표준화된 방법을 제공합니다. API는 공개 또는 비공개로 제공되며, 일반적으로 서로 다른 시스템을 통합하고, 타사 개발을 용이하게 하며, 애플리케이션 간 상호 운용성을 지원하는 데 사용됩니다. 일반적으로 API에는 엔드포인트, 요청 메서드(GET, POST, PUT 등), 그리고 상호작용할 데이터 형식(JSON 또는 XML 등)이 포함됩니다.
  </p>
</section>

<details open>
<summary><a href="category/repo_hosting_services/github.html">GitHub</a> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
    <p>GitHub는 Git을 활용한 버전 관리 및 협업을 위한 웹 기반 플랫폼이다. Microsoft가 소유한 GitHub는 SW 개발을 위한
    호스팅을 제공하고 기본적인 Git 기능 외의 다양한 기능을 제공한다. GitHub에는 프로젝트 관리, 코드 검토, 소셜 코딩
    도구가 포함되어 있다. 주요 기능으로는 코드 저장을 위한 저장소, 변경 사항 제안 및 검토를 위한 풀 리퀘스트, 버그 작업
    및 작업 추적을 위한 이슈, 워크플로 자동화를 위한 액션 등이 있다. 공개 및 비공개 저장소를 모두 지원하여 오픈소스
    프로젝트와 비공개 개발에 널리 사용된다. 저장소 포킹 및 인라인 코드 주석과 같은 GitHub의 협업 기능은 팀 개발
    및 커뮤니티 기여를 용이하게 한다. 광범위한 통합 기능과 광범위한 사용자 기반을 바탕으로 GitHub는 개발자를 위한 중심
    *허브로 자리 잡았으며, 모든 규모의 SW 프로젝트를 위한 포트폴리오, 협업 플랫폼, 배포 도구 역할을 한다.
</p>

<ul>
    <li><strong>허브(hub):</strong> ‘중심 거점’이라는 의미로, 여러 개발자와 도구·프로젝트가 모여 서로 연결되고 교류하는 핵심 플랫폼을</li>
    <ul>
    <li>즉, GitHub가 개발 생태계의 중심축 역할을 한다는 비유적 표현</li>
    </ul>
    <li><strong>롤백(Rollback):</strong> 잘못된 커밋이나 배포 후 문제 발생 시, 이전 안정 상태로 변경 이력을 되돌리는 작업 </li>
    <li><strong>브랜칭(Branching):</strong> 주요 코드베이스에서 분기된 독립된 작업 공간을 만들어 기능 개발·버그 수정 등을 병행할 수 있게 하는 Git 기능</li>
    <li><strong>스테이징 영역(Staging Area):</strong> <em>git add</em> 명령으로 커밋 전 변경 파일을 임시로 모아 두는 공간으로, 어떤 변경을 커밋할지 선택할 수 있게 해 준다.</li>
    <li><strong>풀 리퀘스트(Pull Request):</strong> 분기된 브랜치에서 작업한 내용을 메인 브랜치에 병합해 달라고 요청하는 절차로, 코드 리뷰와 자동 테스트를 거쳐 안전하게 통합한다.</li>
</ul>

</div>
</details>

<details>
<summary><a href="category/repo_hosting_services/gitlab.html">GitLab</a> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
    <p>GitLab은 SW 개발 라이프사이클을 위한 완벽한 솔루션을 제공하는 웹 기반 *DevOps 플랫폼이다. 소스 코드 관리, 
    *지속적 통합/지속적 배포(CI/CD), 이슈 추적 등 다양한 기능을 *단일 애플리케이션에 통합하여 제공한다. GitLab은 Git 
    저장소를 지원하며, GitHub의 풀 리퀘스트와 유사한 병합 요청, 위키 페이지, 이슈 보드 등의 기능을 제공합니다. DevOps 
    실행 방식을 강조하여 *CI/CD 파이프라인, *컨테이너 레지스트리, *쿠버네티스 통합 기능을 기본 제공한다. GitLab은 *클라우드 
    호스팅 및 *셀프 호스팅 옵션을 모두 제공하여 기업의 배포 유연성을 높인다. GitLab의 *올인원 접근 방식은 다른 생태계에서는 
    여러 도구가 필요할 수 있는 기능을 포함하고 있어 경쟁사와 차별화된다. GitLab은 계획부터 모니터링까지 DevOps 라이프사이클 
    전체에 중점을 두고 있어 개발 워크플로우를 위한 통합 플랫폼을 찾는 기업과 팀에게 인기가 높다.
</p>

<ul>
    <li><strong>DevOps:</strong> 개발(Development)과 운영(Operations)의 경계를 허물어 협업·자동화를 통해 빠르고 안정적인 SW 제공을 실현하는 문화·방법론</li>
    <li><strong>CI/CD:</strong> 코드 통합(CI)과 지속적 배포/전달(CD)을 자동화해 빌드→테스트→배포 전 과정을 효율화하는 기법</li>
    <li><strong>단일 애플리케이션(모놀리식):</strong> 기능들을 하나의 배포 단위로 묶어 운영하는 구조로, 구현이 단순하지만 서비스 확장·유연성에 제약이 있음</li>
    <li><strong>CI/CD 파이프라인:</strong> 코드 커밋부터 프로덕션 배포까지 빌드·테스트·배포 단계를 연속적으로 실행하는 자동화된 워크플로우</li>
    <li><strong>컨테이너 레지스트리:</strong> Docker 이미지 등의 컨테이너 패키지를 저장·버전 관리·배포할 수 있는 중앙 저장소 서비스(예: Docker Hub)</li>
    <li><strong>쿠버네티스 통합 기능:</strong> CI/CD 도구가 Kubernetes 클러스터와 연동되어 컨테이너 배포·스케일링·롤백 등을 자동으로 수행하도록 지원하는 기능</li>
    <li><strong>클라우드 호스팅 및 셀프 호스팅:</strong> AWS·GCP 같은 외부 클라우드에 인프라를 맡기거나, 자체 서버에 소프트웨어를 설치해 운영하는 두 가지 방식</li>
    <li><strong>올인원 접근 방식:</strong> 빌드·테스트·배포·모니터링 등 개발·운영에 필요한 모든 기능을 하나의 플랫폼이나 도구에서 통합 제공하는 방식</li>
</ul>
</div>
</details>
