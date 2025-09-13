---
layout: default
title: "DevOps 면접 대비 — 완전 정리"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>DevOps 면접 대비 — 기본·심화 Q&A + 추가 예상 질문 Q&A + 개념 요약</h2>
  <p>구성: 기본 면접 Q&A → 심화 면접 Q&A → 추가 예상 질문 Q&A → DevOps 개념 요약 노트</p>
</section>

<!-- ① 기본 면접 Q&A -->
<details open>
  <summary><span class="accordion-title">📋 기본 면접 Q&A</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">
<details>
  <summary style="font-size:1rem;"><b>Q1. Git이란 무엇이며 다른 버전 관리 시스템과의 차이점은?</b></summary>
  <div class="accordion-content">
<p>Git은 분산 버전 관리 시스템으로, 각 개발자가 로컬에 전체 프로젝트 히스토리를 가지고 작업할 수 있습니다. SVN이나 CVS와 달리 중앙 서버 없이도 독립적으로 작업 가능하며, 브랜치 생성과 병합이 매우 빠르고 효율적입니다. 또한 데이터 무결성을 위해 SHA-1 해시를 사용하여 모든 객체를 식별하고, 스냅샷 방식으로 변경사항을 저장합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q2. Git의 세 가지 영역(Three Areas)을 설명해주세요.</b></summary>
  <div class="accordion-content">
<p>**Working Directory**는 실제 파일이 있는 작업 공간으로 수정 중인 파일들이 있습니다. **Staging Area(Index)**는 다음 커밋에 포함될 변경사항들을 임시로 저장하는 영역입니다. **Repository**는 실제 커밋된 히스토리가 저장되는 곳입니다. 파일은 Working Directory에서 수정되고, `git add`로 Staging Area에 추가되며, `git commit`으로 Repository에 영구 저장됩니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q3. Git 브랜치 전략들을 비교해주세요.</b></summary>
  <div class="accordion-content">
<p>**Git Flow**는 master, develop, feature, release, hotfix 브랜치로 구성된 복잡한 모델로 대규모 프로젝트에 적합합니다. **GitHub Flow**는 master와 feature 브랜치만 사용하는 단순한 모델로 지속적 배포에 유리합니다. **GitLab Flow**는 environment 브랜치를 추가하여 배포 환경별 관리가 가능합니다. **Trunk-based Development**는 매우 짧은 생명주기의 브랜치를 사용하거나 직접 main에 커밋하는 방식입니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q4. CI/CD란 무엇이며 각각의 역할은?</b></summary>
  <div class="accordion-content">
<p>**CI(Continuous Integration)**는 개발자들이 코드 변경사항을 자주 통합하고 자동화된 빌드와 테스트를 수행하여 통합 문제를 조기에 발견하는 것입니다. **CD(Continuous Deployment/Delivery)**는 Delivery의 경우 프로덕션 배포 준비 상태까지 자동화하고, Deployment는 프로덕션까지 완전 자동 배포하는 것입니다. 이를 통해 배포 리스크를 줄이고 릴리스 주기를 단축할 수 있습니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q5. Docker 컨테이너와 가상머신의 차이점은?</b></summary>
  <div class="accordion-content">
<p>가상머신은 하이퍼바이저 위에서 완전한 운영체제를 실행하며 강력한 격리를 제공하지만 리소스 오버헤드가 큽니다. Docker 컨테이너는 호스트 OS 커널을 공유하면서 애플리케이션 레벨에서 격리를 제공합니다. 컨테이너는 시작 시간이 빠르고 리소스 효율적이며 이미지 크기가 작지만, 보안 격리가 상대적으로 약하고 같은 커널을 공유하므로 OS 레벨 버그에 취약할 수 있습니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q6. 마이크로서비스 아키텍처의 장단점은?</b></summary>
  <div class="accordion-content">
<p>**장점**: 서비스별 독립적 개발과 배포가 가능하고, 기술 스택을 자유롭게 선택할 수 있으며, 장애 격리와 확장성이 우수합니다. 팀의 자율성이 높아지고 비즈니스 도메인에 맞는 최적화가 가능합니다. **단점**: 서비스 간 통신 복잡성이 증가하고, 분산 시스템의 복잡성(네트워크 지연, 장애 처리)을 다뤄야 하며, 데이터 일관성 관리와 모니터링이 어려워집니다. 운영 복잡도가 크게 증가합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q7. 인프라스트럭처 as 코드(IaC)의 개념과 도구들은?</b></summary>
  <div class="accordion-content">
<p>IaC는 인프라를 코드로 정의하고 관리하는 방식으로, 수동 설정 대신 선언적 파일로 인프라를 구성합니다. **Terraform**은 클라우드 무관한 프로비저닝 도구이고, **AWS CloudFormation**은 AWS 전용 서비스입니다. **Ansible**은 구성 관리와 애플리케이션 배포에 강점이 있고, **Kubernetes**는 컨테이너 오케스트레이션을 담당합니다. 이를 통해 인프라의 버전 관리, 재현성, 확장성을 확보할 수 있습니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q8. 모니터링과 로깅의 차이점 및 주요 도구들은?</b></summary>
  <div class="accordion-content">
<p>**모니터링**은 시스템의 현재 상태와 성능 지표를 실시간으로 추적하여 문제를 사전에 감지하는 것입니다. **로깅**은 시스템에서 발생하는 이벤트를 기록하여 문제 분석과 디버깅에 활용합니다. Prometheus와 Grafana는 메트릭 수집과 시각화에 사용되고, ELK Stack(Elasticsearch, Logstash, Kibana)이나 EFK Stack은 로그 수집과 분석에 활용됩니다. APM 도구로는 New Relic, DataDog 등이 있습니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q9. Blue-Green 배포와 Rolling 배포의 차이점은?</b></summary>
  <div class="accordion-content">
<p>**Blue-Green 배포**는 현재 환경(Blue)과 동일한 새로운 환경(Green)을 구성하고, 트래픽을 한 번에 전환하는 방식입니다. 롤백이 빠르고 다운타임이 없지만 리소스가 2배로 필요합니다. **Rolling 배포**는 인스턴스를 점진적으로 교체하는 방식으로 리소스 효율적이지만 배포 중 버전이 혼재되고 롤백이 복잡할 수 있습니다. **Canary 배포**는 소수 사용자에게만 먼저 배포하여 안정성을 검증하는 방식입니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q10. 컨테이너 오케스트레이션의 필요성과 Kubernetes의 주요 컴포넌트는?</b></summary>
  <div class="accordion-content">
<p>대규모 컨테이너 환경에서는 자동 배포, 스케일링, 로드밸런싱, 장애 복구, 롤링 업데이트 등이 필요합니다. **Kubernetes**의 주요 컴포넌트로는 API Server(클러스터 관리), etcd(설정 저장소), Scheduler(파드 배치), Controller Manager(상태 관리), kubelet(노드 에이전트), kube-proxy(네트워킹)가 있습니다. Pod, Service, Deployment, ConfigMap, Secret 등의 리소스로 애플리케이션을 선언적으로 관리합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q11. DevOps란 무엇이며 전통적인 개발 방식과의 차이점은?</b></summary>
  <div class="accordion-content">
<p>DevOps는 Development와 Operations의 합성어로, 개발팀과 운영팀 간의 협력과 소통을 강화하여 소프트웨어 개발과 배포를 자동화하는 문화와 방법론입니다. 전통적인 방식에서는 개발과 운영이 분리되어 사일로 효과가 발생했지만, DevOps는 전체 라이프사이클을 통합하여 빠른 피드백과 지속적인 개선을 추구합니다. 자동화, 협업, 측정, 공유의 핵심 가치를 통해 배포 빈도를 높이고 장애 복구 시간을 단축합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q12. Docker 이미지와 컨테이너의 관계를 설명해주세요.</b></summary>
  <div class="accordion-content">
<p>Docker 이미지는 애플리케이션과 그 실행 환경을 포함한 읽기 전용 템플릿입니다. 컨테이너는 이미지를 실행한 인스턴스로, 이미지 위에 쓰기 가능한 레이어가 추가됩니다. 하나의 이미지로 여러 개의 컨테이너를 생성할 수 있으며, 각 컨테이너는 독립적인 실행 환경을 가집니다. 이미지는 레이어 구조로 되어 있어 공통 레이어를 재사용하여 저장 공간을 효율적으로 사용합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q13. Kubernetes Pod와 Service의 역할과 관계는?</b></summary>
  <div class="accordion-content">
<p>**Pod**는 Kubernetes의 최소 배포 단위로, 하나 이상의 컨테이너를 포함하며 동일한 네트워크와 스토리지를 공유합니다. Pod는 일시적이고 IP가 변경될 수 있습니다. **Service**는 Pod에 대한 안정적인 네트워크 엔드포인트를 제공하는 추상화 계층입니다. 로드밸런싱과 서비스 디스커버리를 담당하며, ClusterIP, NodePort, LoadBalancer, ExternalName 타입이 있습니다. Selector를 통해 Pod를 동적으로 연결합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q14. 로드밸런싱의 종류와 각각의 특징은?</b></summary>
  <div class="accordion-content">
<p>**Layer 4 로드밸런싱**은 IP와 포트 정보를 기반으로 트래픽을 분산하며 속도가 빠르지만 세밀한 제어가 어렵습니다. **Layer 7 로드밸런싱**은 HTTP 헤더, URL, 쿠키 등을 분석하여 지능적인 라우팅이 가능하지만 처리 오버헤드가 있습니다. 알고리즘으로는 Round Robin(순차 분산), Least Connections(최소 연결), IP Hash(클라이언트 IP 기반), Weighted(가중치 기반) 등이 있습니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q15. 환경별 설정 관리 방법들을 설명해주세요.</b></summary>
  <div class="accordion-content">
<p>**환경변수**는 가장 기본적인 방법으로 12-factor app 원칙에 따라 코드와 설정을 분리합니다. **설정 파일**은 환경별로 다른 파일을 사용하며, **Kubernetes ConfigMap/Secret**은 설정과 민감 정보를 별도로 관리합니다. **외부 설정 서비스**(Consul, etcd, AWS Parameter Store)를 사용하여 중앙화된 설정 관리도 가능합니다. 설정 변경 시 자동 재배포나 동적 리로드 기능도 고려해야 합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q16. API Gateway의 역할과 주요 기능들은?</b></summary>
  <div class="accordion-content">
<p>API Gateway는 마이크로서비스 아키텍처에서 클라이언트와 백엔드 서비스 사이의 단일 진입점 역할을 합니다. **주요 기능**으로는 요청 라우팅과 로드밸런싱, 인증과 인가, Rate Limiting과 Throttling, 요청/응답 변환, 로깅과 모니터링, 캐싱, CORS 처리가 있습니다. Kong, AWS API Gateway, Istio Gateway, NGINX Plus 등의 솔루션이 있으며, 서비스별 횡단 관심사를 중앙에서 처리할 수 있습니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q17. 컨테이너 레지스트리의 역할과 보안 고려사항은?</b></summary>
  <div class="accordion-content">
<p>컨테이너 레지스트리는 Docker 이미지를 저장하고 배포하는 중앙 저장소입니다. Docker Hub, AWS ECR, Google GCR, Harbor 등이 있습니다. **보안 고려사항**으로는 이미지 취약점 스캔, 디지털 서명을 통한 이미지 무결성 검증, RBAC을 통한 접근 제어, 프라이빗 레지스트리 사용, 이미지 태그 관리가 있습니다. 또한 base 이미지 선택 시 공식 이미지나 최소 이미지(alpine) 사용을 권장합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q18. 자동화 테스트의 종류와 CI/CD에서의 역할은?</b></summary>
  <div class="accordion-content">
<p>**단위 테스트**는 개별 함수나 클래스를 검증하며 빠르고 격리된 테스트입니다. **통합 테스트**는 여러 컴포넌트 간의 상호작용을 검증하고, **E2E 테스트**는 전체 시스템의 동작을 사용자 관점에서 검증합니다. CI/CD에서는 단위 테스트→통합 테스트→E2E 테스트 순으로 실행하며, 실패 시 파이프라인을 중단합니다. 테스트 자동화를 통해 회귀 버그를 방지하고 배포 품질을 보장할 수 있습니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q19. 컨테이너의 상태 관리(Stateful vs Stateless)를 설명해주세요.</b></summary>
  <div class="accordion-content">
<p>**Stateless 애플리케이션**은 요청 간에 상태를 유지하지 않아 수평 확장이 쉽고 장애 복구가 간단합니다. 대부분의 웹 애플리케이션이 이에 해당합니다. **Stateful 애플리케이션**은 데이터베이스처럼 상태를 유지해야 하며, Kubernetes StatefulSet을 사용하여 관리합니다. Persistent Volume을 통해 데이터를 영구 저장하고, 순서가 있는 배포와 안정적인 네트워크 식별자를 제공합니다. 상태 분리 설계가 클라우드 네이티브의 핵심 원칙입니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q20. 캐싱 전략들과 적용 시나리오를 설명해주세요.</b></summary>
  <div class="accordion-content">
<p>**Redis/Memcached** 같은 인메모리 캐시는 빠른 응답이 필요한 데이터에 사용합니다. **CDN**은 정적 리소스의 지리적 분산 캐싱에 활용되고, **애플리케이션 레벨 캐싱**은 계산 비용이 높은 결과를 저장합니다. **데이터베이스 쿼리 캐싱**은 반복적인 조회 성능을 향상시킵니다. 캐시 무효화 전략(TTL, Cache-aside, Write-through, Write-behind)과 캐시 일관성 관리가 중요하며, 캐시 히트율 모니터링을 통해 효과를 측정해야 합니다.</p>
  </div>
</details>
  </div>
</details>

<!-- ② 심화 면접 Q&A -->
<details>
  <summary><span class="accordion-title">🚀 심화 면접 Q&A</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">
<details>
  <summary style="font-size:1rem;"><b>Q11. Git Rebase와 Merge의 차이점과 사용 시나리오는?</b></summary>
  <div class="accordion-content">
<p>**Merge**는 두 브랜치의 변경사항을 병합 커밋으로 합치는 방식으로 히스토리가 보존되지만 복잡해질 수 있습니다. **Rebase**는 커밋을 다른 브랜치 위에 재배치하여 선형적인 히스토리를 만듭니다. Rebase는 feature 브랜치를 깔끔하게 정리할 때 사용하고, Merge는 히스토리 보존이 중요한 경우나 공유 브랜치에서 사용합니다. **주의사항**: 공개된 브랜치에서는 rebase를 피해야 합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q12. 컨테이너 보안의 주요 고려사항들은?</b></summary>
  <div class="accordion-content">
<p>**이미지 보안**: 최소한의 베이스 이미지 사용, 취약점 스캔, 신뢰할 수 있는 레지스트리 사용이 중요합니다. **런타임 보안**: 비특권 사용자로 실행, 읽기 전용 파일시스템, 리소스 제한 설정이 필요합니다. **네트워크 보안**: 네트워크 정책으로 트래픽 제한, 서비스 메시로 암호화된 통신을 구현합니다. **액세스 제어**: RBAC(Role-Based Access Control)과 Pod Security Standards를 활용합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q13. DevSecOps의 개념과 구현 방법은?</b></summary>
  <div class="accordion-content">
<p>DevSecOps는 개발 라이프사이클 전반에 보안을 통합하는 방식입니다. **Shift-Left** 접근으로 개발 초기부터 보안을 고려하고, 자동화된 보안 테스트를 CI/CD 파이프라인에 통합합니다. SAST(정적 분석), DAST(동적 분석), 의존성 취약점 검사, 컨테이너 이미지 스캔을 자동화하고, Infrastructure as Code의 보안 검증도 포함합니다. 지속적인 모니터링과 컴플라이언스 검사도 중요합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q14. 분산 시스템에서의 데이터 일관성 문제와 해결 방법은?</b></summary>
  <div class="accordion-content">
<p>**CAP 정리**에 따르면 일관성(Consistency), 가용성(Availability), 분할 내성(Partition tolerance) 중 두 가지만 보장할 수 있습니다. **Eventually Consistent** 모델에서는 일정 시간 후 일관성이 보장되고, **Strong Consistency**는 모든 노드가 동시에 같은 값을 봅니다. **Saga 패턴**이나 **Two-Phase Commit**으로 분산 트랜잭션을 처리하고, **CQRS**와 **Event Sourcing**으로 읽기/쓰기를 분리할 수 있습니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q15. 서비스 메시(Service Mesh)의 개념과 필요성은?</b></summary>
  <div class="accordion-content">
<p>서비스 메시는 마이크로서비스 간 통신을 관리하는 인프라 계층입니다. **Istio**나 **Linkerd** 같은 도구로 서비스 간 통신 암호화, 로드밸런싱, 서킷 브레이커, 분산 추적, 카나리 배포를 자동화할 수 있습니다. 애플리케이션 코드와 네트워킹 로직을 분리하여 개발팀은 비즈니스 로직에 집중하고, 운영팀은 네트워킹과 보안을 중앙에서 관리할 수 있습니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q16. 클라우드 네이티브 애플리케이션의 12 Factor App 원칙들은?</b></summary>
  <div class="accordion-content">
<p>1. **코드베이스**: 하나의 코드베이스, 다양한 배포
2. **의존성**: 명시적 선언과 격리
3. **설정**: 환경별 설정을 환경변수로 관리
4. **백엔드 서비스**: 리소스로 취급
5. **빌드, 릴리스, 실행**: 단계별 엄격한 분리
6. **프로세스**: 무상태 프로세스로 실행
7. **포트 바인딩**: 서비스를 포트에 바인딩하여 내보내기
8. **동시성**: 프로세스 모델로 확장
9. **폐기 가능성**: 빠른 시작과 우아한 종료
10. **개발/프로덕션 일치**: 환경 간 차이 최소화
11. **로그**: 이벤트 스트림으로 처리
12. **관리 프로세스**: 일회성 관리 작업을 별도 프로세스로 실행</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q17. GitOps의 개념과 장점은?</b></summary>
  <div class="accordion-content">
<p>GitOps는 Git을 인프라와 애플리케이션 배포의 단일 진실 소스로 사용하는 운영 모델입니다. 모든 변경사항을 Git에서 관리하고, 자동화된 에이전트가 Git 상태와 실제 환경을 동기화합니다. **장점**으로는 배포의 추적성과 감사 기능, 롤백의 용이성, 선언적 인프라 관리, 개발자 친화적 워크플로우가 있습니다. ArgoCD, Flux 같은 도구로 구현할 수 있습니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q18. 컨테이너 성능 최적화 방법들은?</b></summary>
  <div class="accordion-content">
<p>**이미지 최적화**: 멀티스테이지 빌드 사용, 불필요한 패키지 제거, 레이어 캐싱 활용이 중요합니다. **리소스 관리**: CPU/메모리 requests와 limits 적절히 설정하고, HPA(Horizontal Pod Autoscaler)로 자동 스케일링을 구성합니다. **네트워킹**: 서비스 디스커버리 최적화, 로드밸런서 설정 튜닝을 진행합니다. **스토리지**: 적절한 볼륨 타입 선택, 데이터 지역성 고려가 필요합니다.</p>
  </div>
</details>
  </div>
</details>

<!-- ③ 추가 예상 질문 Q&A -->
<details>
  <summary><span class="accordion-title">💡 추가 예상 질문 Q&A</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">
<details>
  <summary style="font-size:1rem;"><b>Q19. 카오스 엔지니어링(Chaos Engineering)이란?</b></summary>
  <div class="accordion-content">
<p>카오스 엔지니어링은 의도적으로 시스템에 장애를 주입하여 복원력을 테스트하는 방법입니다. Netflix의 Chaos Monkey가 대표적인 예로, 무작위로 인스턴스를 종료하여 시스템의 내결함성을 검증합니다. 프로덕션 환경에서 작은 실험부터 시작하여 점진적으로 확대하고, 가설을 세우고 결과를 측정하여 시스템의 약점을 발견하고 개선합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q20. 옵저버빌리티(Observability)와 모니터링의 차이는?</b></summary>
  <div class="accordion-content">
<p>**모니터링**은 알려진 문제를 추적하고 미리 정의된 메트릭을 수집하는 것입니다. **옵저버빌리티**는 시스템의 내부 상태를 외부 출력만으로 얼마나 잘 이해할 수 있는지를 나타내며, 예상치 못한 문제도 디버깅할 수 있어야 합니다. Three Pillars는 메트릭(Metrics), 로그(Logs), 트레이스(Traces)로 구성되며, 분산 추적과 고차원 메트릭을 통해 복잡한 시스템의 동작을 이해할 수 있습니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q21. 제로 다운타임 배포 전략들을 비교해주세요.</b></summary>
  <div class="accordion-content">
<p>**Rolling Update**: 점진적 인스턴스 교체, 리소스 효율적이지만 버전 혼재 가능
**Blue-Green**: 완전한 환경 교체, 빠른 롤백 가능하지만 리소스 2배 필요
**Canary**: 일부 트래픽만 새 버전으로 라우팅, 위험 최소화하지만 복잡한 구현
**A/B Testing**: 사용자 그룹별 다른 버전 제공, 비즈니스 검증 가능
**Feature Toggles**: 코드는 배포하되 기능은 스위치로 제어</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q22. 클라우드 비용 최적화 전략은?</b></summary>
  <div class="accordion-content">
<p>**리소스 적정 사이징**: 실제 사용량에 맞는 인스턴스 타입 선택, 과도한 프로비저닝 방지가 중요합니다. **예약 인스턴스/스팟 인스턴스**: 장기 사용 예측되는 워크로드는 예약 인스턴스, 중단 가능한 작업은 스팟 인스턴스를 활용합니다. **자동 스케일링**: 수요에 따른 자동 확장/축소로 불필요한 리소스 사용을 방지하고, 스케줄링된 스케일링으로 예측 가능한 패턴에 대응합니다. **태깅과 모니터링**: 리소스별 비용 추적과 알림 설정이 필요합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q23. 멀티 클라우드와 하이브리드 클라우드의 차이점과 고려사항은?</b></summary>
  <div class="accordion-content">
<p>**멀티 클라우드**는 여러 클라우드 제공업체를 동시에 사용하는 것이고, **하이브리드 클라우드**는 온프레미스와 클라우드를 연결하여 사용하는 것입니다. 멀티 클라우드는 벤더 종속성 회피와 최적 서비스 선택이 가능하지만 복잡성이 증가합니다. 하이브리드는 민감한 데이터는 온프레미스에, 확장성이 필요한 워크로드는 클라우드에 배치할 수 있습니다. 두 방식 모두 네트워킹, 보안, 데이터 동기화의 복잡성을 관리해야 합니다.</p>
  </div>
</details>

<details>
  <summary style="font-size:1rem;"><b>Q24. 분산 추적(Distributed Tracing)의 중요성과 구현 방법은?</b></summary>
  <div class="accordion-content">
<p>마이크로서비스 환경에서 하나의 요청이 여러 서비스를 거치며 처리되므로, 전체 요청 경로를 추적하기 어렵습니다. 분산 추적은 요청의 전체 여정을 시각화하여 병목 지점과 장애 원인을 파악할 수 있게 합니다. **OpenTelemetry**로 표준화된 계측을 구현하고, **Jaeger**나 **Zipkin**으로 데이터를 수집하고 시각화합니다. 트레이스 ID를 통해 관련된 모든 스팬을 연결하고, 의미 있는 메타데이터를 태그로 추가합니다.</p>
  </div>
</details>
  </div>
</details>

<!-- ④ DevOps 개념 요약 노트 -->
<details>
  <summary><span class="accordion-title">📚 DevOps 개념 요약 노트</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">
<h3>🔄 버전 관리 (Git)</h3>
<b>Git 워크플로우</b>
<ul>
<li>Working Directory ↔ Staging Area ↔ Repository</li>
<li>add: Working → Staging</li>
<li>commit: Staging → Repository</li>
<li>checkout: Repository → Working</li>
</ul>
<b>브랜치 전략 비교</b>
<ul>
<li><b>Git Flow</b>: feature → develop → release → master</li>
<li><b>GitHub Flow</b>: feature → master (simple)</li>
<li><b>GitLab Flow</b>: feature → master → environment</li>
<li><b>Trunk-based</b>: 짧은 브랜치 또는 직접 master</li>
</ul>
<b>주요 명령어</b>
<pre><code class="language-bash">git add .                    # 스테이징
git commit -m &quot;message&quot;      # 커밋
git push origin branch       # 푸시
git pull origin branch       # 풀
git merge branch            # 머지
git rebase branch           # 리베이스
git stash                   # 임시 저장
git cherry-pick commit      # 특정 커밋 적용
</code></pre>
<h3>🐳 컨테이너화 (Docker)</h3>
<b>Docker 기본 개념</b>
<ul>
<li>이미지: 실행 가능한 패키지</li>
<li>컨테이너: 이미지의 실행 인스턴스</li>
<li>레지스트리: 이미지 저장소</li>
</ul>
<b>Dockerfile 최적화</b>
<pre><code class="language-dockerfile"># 멀티스테이지 빌드
FROM node:16 AS builder
WORKDIR /app
COPY package*.json ./
RUN npm ci --only=production
<p>FROM node:16-alpine
WORKDIR /app
COPY --from=builder /app/node_modules ./node_modules
COPY . .
EXPOSE 3000
CMD [&amp;quot;npm&amp;quot;, &amp;quot;start&amp;quot;]
&lt;/code&gt;&lt;/pre&gt;</p>
<h3>☸️ 오케스트레이션 (Kubernetes)</h3>
<b>핵심 리소스</b>
<ul>
<li><b>Pod</b>: 최소 배포 단위</li>
<li><b>Service</b>: 네트워킹과 로드밸런싱</li>
<li><b>Deployment</b>: 선언적 업데이트</li>
<li><b>ConfigMap/Secret</b>: 설정과 비밀 관리</li>
</ul>
<b>kubectl 주요 명령어</b>
<pre><code class="language-bash">kubectl get pods                    # Pod 목록
kubectl describe pod &lt;name&gt;         # Pod 상세 정보
kubectl logs &lt;pod-name&gt;            # 로그 확인
kubectl apply -f deployment.yaml   # 리소스 적용
kubectl delete -f deployment.yaml  # 리소스 삭제
kubectl exec -it &lt;pod&gt; -- /bin/sh  # Pod 내부 접속
</code></pre>
<h3>🔄 CI/CD 파이프라인</h3>
<b>CI (Continuous Integration)</b>
1. 소스 코드 푸시
2. 자동 빌드 트리거
3. 단위 테스트 실행
4. 정적 분석 수행
5. 아티팩트 생성
<b>CD (Continuous Deployment)</b>
1. 통합 테스트
2. 보안 스캔
3. 스테이징 배포
4. 승인 프로세스
5. 프로덕션 배포
<h3>📊 모니터링 & 옵저버빌리티</h3>
<b>Three Pillars</b>
<ul>
<li><b>Metrics</b>: 시계열 수치 데이터</li>
<li><b>Logs</b>: 구조화된 이벤트 데이터</li>
<li><b>Traces</b>: 분산 시스템의 요청 경로</li>
</ul>
<b>주요 도구</b>
<ul>
<li><b>Prometheus + Grafana</b>: 메트릭 수집/시각화</li>
<li><b>ELK/EFK Stack</b>: 로그 관리</li>
<li><b>Jaeger/Zipkin</b>: 분산 추적</li>
<li><b>AlertManager</b>: 알림 관리</li>
</ul>
<h3>🛡️ 보안 (DevSecOps)</h3>
<b>Shift-Left Security</b>
<ul>
<li>개발 초기부터 보안 고려</li>
<li>자동화된 보안 테스트</li>
<li>코드 스캔과 취약점 분석</li>
</ul>
<b>보안 도구</b>
<ul>
<li><b>SAST</b>: SonarQube, Checkmarx</li>
<li><b>DAST</b>: OWASP ZAP, Burp Suite</li>
<li><b>Container Scanning</b>: Twistlock, Aqua</li>
<li><b>Dependency Check</b>: Snyk, OWASP Dependency Check</li>
</ul>
<h3>☁️ 클라우드 네이티브</h3>
<b>12 Factor App 핵심 원칙</b>
1. 코드베이스 통합
2. 의존성 명시
3. 환경변수로 설정 관리
4. 백엔드 서비스를 리소스로 취급
5. 빌드/릴리스/실행 분리
6. 무상태 프로세스
<b>Infrastructure as Code</b>
<ul>
<li><b>Terraform</b>: 멀티 클라우드 프로비저닝</li>
<li><b>CloudFormation</b>: AWS 전용</li>
<li><b>Ansible</b>: 구성 관리</li>
<li><b>Helm</b>: Kubernetes 패키지 관리</li>
</ul>
<h3>🎯 성능 최적화</h3>
<b>컨테이너 최적화</b>
<ul>
<li>최소 베이스 이미지 사용</li>
<li>레이어 캐싱 활용</li>
<li>멀티스테이지 빌드</li>
<li>리소스 제한 설정</li>
</ul>
<b>Kubernetes 최적화</b>
<ul>
<li>HPA/VPA 자동 스케일링</li>
<li>리소스 requests/limits 적절 설정</li>
<li>노드 어피니티 활용</li>
<li>PDB(Pod Disruption Budget) 설정</li>
</ul>
  </div>
</details>

<!-- ⑤ 면접 팁 -->
<details>
  <summary><span class="accordion-title">💭 면접 팁</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">
<p>1. &lt;b&gt;실무 경험 중심&lt;/b&gt;: 이론보다는 실제 프로젝트에서의 경험과 해결한 문제들을 구체적으로 설명
2. &lt;b&gt;도구의 목적과 한계&lt;/b&gt;: 각 도구를 선택한 이유와 트레이드오프를 설명할 수 있어야 함
3. &lt;b&gt;전체적인 아키텍처 관점&lt;/b&gt;: 개별 기술보다는 시스템 전체의 관점에서 설명
4. &lt;b&gt;최신 트렌드 이해&lt;/b&gt;: GitOps, 서비스 메시, 옵저버빌리티 등 최신 개념에 대한 이해
5. &lt;b&gt;문제 해결 과정&lt;/b&gt;: 장애 상황이나 성능 문제를 어떻게 분석하고 해결했는지 설명
6. &lt;b&gt;비즈니스 영향&lt;/b&gt;: 기술적 개선이 비즈니스에 미친 영향을 정량적으로 설명
7. &lt;b&gt;보안과 컴플라이언스&lt;/b&gt;: DevSecOps 관점에서 보안을 어떻게 통합했는지 설명
8. &lt;b&gt;팀 협업&lt;/b&gt;: 개발팀과의 협업 방식과 문화 개선 경험</p>
  </div>
</details>
