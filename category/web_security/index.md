---
layout: default
title: "Web Security"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>Web Security</h2>
  <p>
    Web Security는 웹 애플리케이션을 위협과 취약점으로부터 보호하여 데이터 기밀성, 무결성 및 가용성을 보장하는 것을 의미합니다. 핵심적인 보안 조치로는 강력한 인증 및 권한 부여 메커니즘, 안전한 데이터 전송을 위한 암호화(예: SSL/TLS) 사용, SQL 인젝션 및 크로스 사이트 스크립팅(XSS)과 같은 공격을 방지하기 위한 사용자 입력 검증 등이 있습니다. 보안 유지를 위해서는 보안 코딩, 효과적인 세션 관리, 정기적인 업데이트 및 패치 적용이 필수적입니다. 또한, 침투 테스트 및 취약점 평가를 포함한 지속적인 보안 테스트는 잠재적인 취약점을 파악하고 해결하여 애플리케이션을 보호하고 사용자 신뢰를 유지하는 데 도움이 됩니다.
  </p>
  <p><strong>정리: Web Security는 위협과 취약점으로부터 웹을 보호해 데이터 기밀성·무결성·가용성을 보장하는 기술과 절차이다.</strong></p>
</section>

<details open>
<summary><span class="accordion-title">Hashing Algorithms</span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  해싱 알고리즘은 데이터를 고정된 길이의 *해시 값으로 변환하여 원본 데이터를 보호하는 기술이다. 주로 비밀번호나 민감한 정보를 저장할 때 사용되며, 원래 데이터로 복원할 수 없는 단방향 특성을 가지고 있다. 보안을 강화하기 위해 해시 값에 *솔트(salt)를 추가하여 *무차별 대입 공격(Brute-force)과 *무지개 테이블(Rainbow Table) 공격을 방지한다. 안전한 *해싱 알고리즘을 사용하면 데이터 유출 시에도 원문이 노출되는 위험을 크게 줄일 수 있다.
  </p>
  <p><strong>정리: Hashing Algorithms는 데이터를 고정 길이 해시값으로 변환해 무결성을 검증하고 비밀번호를 안전하게 저장하는 알고리즘이다.</strong></p>

  <ul>
    <li><strong>해시(Hash):</strong> 데이터를 고정된 길이의 문자열(해시값)로 변환하는 함수의 출력값으로, 원본 데이터를 직접 알 수 없으며 동일한 입력은 항상 동일한 해시값을 생성</li>
    <li><strong>솔트(Salt):</strong> 해시 연산 전에 비밀번호에 추가하는 무작위 문자열로, 동일한 비밀번호라도 서로 다른 해시값을 생성해 무지개 테이블 공격과 같은 사전 공격을 방어</li>
    <li><strong>무차별 대입 공격(Brute-force Attack):</strong> 가능한 모든 비밀번호 조합을 시도해 해시값과 일치하는 원본을 찾는 공격 방식</li>
    <li><strong>무지개 테이블(Rainbow Table) 공격:</strong> 미리 계산된 해시값과 비밀번호의 매핑 테이블을 사용해 빠르게 해시를 역추적하는 공격 기법</li>
    <li><strong>해싱 알고리즘:</strong> 데이터를 고정된 길이로 변환하는 알고리즘으로, 대표적으로 MD5, SHA-1, SHA-256, bcrypt 등이 있으며 속도·보안성·충돌 가능성에 따라 선택함</li>
  </ul>

  <!-- 박스 추가 -->
  <details>
    <summary><span class="accordion-title">MD5 </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      MD5(Message-Digest Algorithm 5)는 널리 사용되는 암호화 해시 함수로, 일반적으로 32자리 16진수로 표현되는 128비트 해시 값을 생성한다. 모든 입력에 대해 고정된 크기의 출력(해시)을 생성하여 데이터의 고유 식별자를 제공하도록 설계되었다. MD5는 한때 데이터 무결성 검증 및 비밀번호 저장에 널리 사용되었지만, 현재는 충돌 공격(두 개의 서로 다른 입력이 동일한 해시 값을 생성하는 공격)을 허용하는 취약점으로 인해 암호학적으로 취약하며 보안에 민감한 애플리케이션에는 적합하지 않은 것으로 간주된다. 결과적으로 MD5는 SHA-256과 같은 더 안전한 해시 함수로 대체되었다.
      </p>
      <p><strong>정리: MD5는 128비트 해시값을 생성하는 빠른 해시 알고리즘이지만 충돌 취약성으로 인해 보안 용도로는 권장되지 않는다.</strong></p>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details>
    <summary><span class="accordion-title">SHA family </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      SHA(Secure Hash Algorithm)는 가변 크기의 입력 데이터에서 고정 크기의 해시 값을 생성하여 데이터 무결성과 보안을 보장하도록 설계된 암호화 해시 함수군이다. SHA 함수는 데이터 무결성 검증, 비밀번호 보안 저장, 디지털 서명 생성 등의 작업에 사용된다. SHA군에는 SHA-1, SHA-2, SHA-3 등 여러 버전이 있다. SHA-1은 160비트 해시 값을 생성하지만 현재 취약성으로 인해 취약한 것으로 간주된다. 반면, 224, 256, 384, 512비트 해시 크기를 가진 SHA-2는 더 강력한 보안을 제공한다. SHA-3는 가장 최근에 추가된 버전으로, 추가적인 보안 기능과 유연성을 제공한다.
      </p>
      <p><strong>정리: SHA(Secure Hash Algorithm) 계열은 다양한 길이의 고정 해시값을 생성해 데이터 무결성을 보장하는 보안 해시 알고리즘 집합이다.</strong></p>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details>
    <summary><span class="accordion-title">Scrypt </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      스크립트(scrypt)는 무차별 대입 공격이나 *GPU 또는 *ASIC을 사용하는 하드웨어 기반 공격에 대응하기 위해 계산 집약적이고 메모리 집약적으로 설계된 핵심 *유도 함수이다. 공격자가 대규모 공격을 수행하기 어렵게 하고 비용도 많이 들게 하여 안전한 암호 해싱을 제공하기 위해 개발되었다. 스크립트는 해시 함수와 대량의 메모리 사용량, 그리고 CPU 집약적인 계산 프로세스를 결합하여, 공격자가 여러 연산을 병렬로 수행할 수 있더라도 메모리 요구 사항으로 인해 이러한 공격은 실행 불가능하게 만든다. 스크립트는 안전한 암호 저장 및 암호화폐 채굴을 포함한 암호화 애플리케이션에서 일반적으로 사용된다.
      </p>
      <p><strong>정리: Scrypt는 메모리 집약적 설계를 통해 GPU·ASIC 기반 대규모 병렬 공격을 어렵게 만든 키 유도 함수이다.</strong></p>
      <ul>
        <li><strong>GPU (Graphics Processing Unit):</strong> 대규모 병렬 연산에 특화된 프로세서로, 비밀번호 해시 크래킹 같은 연산을 빠르게 수행할 수 있음</li>
        <li><strong>ASIC (Application-Specific Integrated Circuit):</strong> 특정 작업만 빠르고 효율적으로 수행하도록 설계된 맞춤형 칩으로, 암호화폐 채굴·해시 크래킹 등에서 높은 성능을 발휘함.</li>
        <li><strong>유도 함수 (Key Derivation Function, KDF):</strong> 입력 비밀번호와 솔트를 사용해 일정 길이의 암호 키를 생성하는 함수로, 반복 연산·메모리 사용 등을 통해 무차별 대입 및 사전 공격을 방어함.</li>
      </ul>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details>
    <summary><span class="accordion-title">Bcrypt </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      Bcrypt는 DB에 저장하기 위해 비밀번호를 안전하게 해싱하도록 설계된 비밀번호 해싱 함수이다. Niels Provos와 David Mazières가 개발한 이 함수는 *Blowfish 암호를 기반으로 하며, 레인보우 테이블 공격으로부터 보호하기 위해 솔트(salt)를 포함한다. Bcrypt의 핵심 기능은 적응형 특성으로, 연산 능력이 증가함에 따라 *비용 계수를 조정하여 속도를 느리게 만들 수 있으므로 시간이 지남에 따라 무차별 대입 공격에 대한 내성을 유지한다. 일반적으로 60자 길이의 고정 크기 해시 출력을 생성하며, 여기에는 솔트와 비용 계수가 포함된다. Bcrypt는 강력한 보안과 비교적 쉬운 구현으로 인해 많은 프로그래밍 언어와 프레임워크에서 널리 사용된다. 의도적으로 처리 속도가 느리기 때문에 속도가 중요하지 않지만 보안이 매우 중요한 비밀번호 저장에 특히 효과적이다.
      </p>
      <p><strong>정리: Bcrypt는 Blowfish 기반으로 설계된 적응형 해시 함수로, 비용 계수를 통해 해시 연산 난이도를 조절해 공격을 어렵게 한다.</strong></p>
      <ul>
        <li><strong>Blowfish 암호:</strong> 64비트 블록 크기와 가변 키 길이를 가진 대칭키 블록 암호 알고리즘으로, 빠르고 유연하며 특허 제한이 없음.</li>
        <li><strong>비용 계수(Cost Factor):</strong> Bcrypt에서 해시 계산 반복 횟수를 제어하는 값으로, 값이 높을수록 해시 연산 시간이 늘어나 무차별 대입 공격에 더 강해짐.</li>
      </ul>
    </div>
  </details>

</div>
</details>

<details open>
<summary><span class="accordion-title">API Security </span> <span class="indicator">펼치기</span></summary>
<div class="accordion-content">
  <p>
  API 보안은 애플리케이션이 제공하는 API를 외부 위협과 취약점으로부터 보호하여 데이터 기밀성, 무결성, 가용성을 보장하는 것을 의미합니다. 이를 위해 HTTPS/SSL을 통한 안전한 통신, 접근 제어, CORS 정책 설정, 콘텐츠 보안 정책(CSP) 적용, OWASP에서 제시하는 취약점 방지, 서버 환경 보안 강화 등의 조치가 필요합니다. 정기적인 보안 점검과 패치, 인증 및 권한 부여 절차, 로그 모니터링을 통해 잠재적인 위험을 사전에 차단하고, 안전하고 신뢰할 수 있는 API 서비스를 유지할 수 있습니다.
  </p>
  <p><strong>정리: API Security는 API를 통한 데이터·서비스 접근을 인증·인가·암호화로 보호해 무단 사용과 공격을 방지하는 보안 체계이다.</strong></p>

  <!-- 박스 추가 -->
  <details>
    <summary><span class="accordion-title">HTTPS </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      HTTPS(Hypertext Transfer Protocol Secure)는 클라이언트(예: 브라우저)와 서버 간의 데이터 전송을 보호하기 위해 설계된 HTTP의 확장 프로토콜이다. *SSL/TLS 프로토콜을 통한 암호화를 사용하여 데이터 기밀성, 무결성 및 신뢰성을 보장한다. 이를 통해 로그인 정보나 결제 정보와 같은 민감한 정보가 공격자에 의해 가로채거나 변조되는 것을 방지한다. HTTPS는 웹 애플리케이션 보안에 필수적이며, 특히 사용자 데이터를 처리하는 웹사이트에서 *중간자 공격(man-in-the-middle attack)과 도청으로부터 보호하는 데 도움이 되므로 대부분의 웹사이트, 특히 사용자 데이터를 처리하는 웹사이트에서 표준으로 자리 잡았다.
      </p>
      <p><strong>정리: HTTPS는 SSL/TLS를 사용해 웹 통신을 암호화하여 데이터 기밀성과 무결성을 보장하는 프로토콜이다.</strong></p>
      <ul>
        <li><strong>SSL (Secure Sockets Layer):</strong> 웹 브라우저와 서버 간의 통신을 암호화하고 인증하는 초기 보안 프로토콜로, 현재는 보안 취약점 때문에 사용이 거의 중단됨.</li>
        <li><strong>TLS (Transport Layer Security):</strong> SSL을 개선·표준화한 최신 보안 프로토콜로, 강력한 암호화와 인증·무결성 검증을 제공하며 현재 HTTPS에서 사용되는 표준 방식</li>
        <li><strong>중간자 공격(Man-in-the-Middle Attack):</strong> 공격자가 통신 중간에 개입해 데이터를 도청하거나 변조하는 공격 방식으로, HTTPS는 암호화와 인증서를 통해 이를 방지</li>
      </ul>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details>
    <summary><span class="accordion-title">CORS </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      CORS(Cross-Origin Resource Sharing)는 웹 브라우저가 웹 페이지를 제공하는 도메인과 다른 도메인의 웹 페이지에 있는 리소스(API 또는 글꼴 등)에 대한 액세스를 제어하기 위해 구현하는 보안 메커니즘이다. CORS는 *동일 출처 정책을 확장하고 유연성을 높여 서버가 리소스에 액세스할 수 있는 사용자를 지정할 수 있도록 한다. CORS는 *HTTP 헤더 시스템을 통해 작동한다. 브라우저는 *교차 출처 리소스를 호스팅하는 서버에 사전 요청을 보내고, 서버는 실제 요청의 허용 여부를 나타내는 헤더를 응답으로 보낸다. 이 메커니즘은 민감한 데이터에 대한 무단 액세스를 방지하는 동시에 합법적인 교차 출처 요청을 허용한다. CORS는 여러 도메인의 서비스와 리소스를 통합하는 최신 웹 애플리케이션에 필수적이며, 보안 요구 사항과 복잡한 분산 웹 시스템의 기능 요구 사항 간의 균형을 유지한다.
      </p>
      <p><strong>정리: CORS는 교차 출처 간 리소스 공유를 허용·제한하는 HTTP 헤더 기반 보안 메커니즘이다.</strong></p>
      <ul>
        <li><strong>동일 출처 정책(Same-Origin Policy):</strong> 웹 브라우저에서 보안상 서로 다른 출처(프로토콜·도메인·포트) 간의 리소스 접근을 기본적으로 차단하는 정책</li>
        <li><strong>HTTP 헤더 시스템:</strong> 클라이언트와 서버가 요청·응답 시 메타데이터를 전달하는 구조로, CORS에서는 Access-Control-Allow-Origin 같은 헤더로 권한을 제어</li>
        <li><strong>교차 출처 리소스(Cross-Origin Resource):</strong> 현재 웹 페이지와 다른 출처(도메인·프로토콜·포트)에 위치한 리소스로, API 서버, 외부 스크립트, 이미지 등이 해당됨.</li>
      </ul>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details>
    <summary><span class="accordion-title">CSP </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      콘텐츠 보안 정책(Content Security Policy)은 웹 브라우저에서 구현하는 보안 표준으로, *XSS(크로스 사이트 스크립팅), *클릭재킹 및 기타 코드 삽입 공격을 차단한다. 웹 개발자는 CSP를 통해 신뢰할 수 있고 웹 페이지에 로드할 수 있는 콘텐츠 소스를 지정할 수 있다. CSP는 일반적으로 HTTP 헤더 또는 *메타 태그를 통해 구현되며, 스크립트, 스타일시트, 이미지, 글꼴 등 다양한 유형의 리소스에 대한 규칙을 정의한다. CSP는 콘텐츠가 로드될 수 있는 출처를 제한함으로써 악성 코드 실행 위험을 크게 줄인다. 또한 개발자가 잠재적인 보안 문제를 파악하고 해결할 수 있도록 위반 사항 보고 기능을 제공한다. CSP는 강력하지만, 특히 타사 리소스나 *인라인 스크립트를 사용하는 사이트의 경우 보안과 기능 간의 균형을 맞추기 위한 세심한 구성이 필요하다.
      </p>
      <p><strong>정리: CSP(Content Security Policy)는 허용된 콘텐츠 출처를 지정해 XSS·클릭재킹 등 공격을 방지하는 보안 정책이다.</strong></p>
      <ul>
        <li><strong>XSS(크로스 사이트 스크립팅):</strong> 악성 스크립트를 웹 페이지에 삽입해 사용자의 브라우저에서 실행시키는 공격으로, 쿠키 탈취·세션 하이재킹 등이 가능함.</li>
        <li><strong>클릭재킹(Clickjacking):</strong> 사용자가 의도하지 않은 동작을 하도록 투명 프레임 등을 덮어씌워 클릭을 유도하는 공격 기법.</li>
        <li><strong>메타 태그(Meta Tag):</strong> HTML 문서의 메타데이터를 정의하는 태그로, 보안 지침(예: CSP)이나 브라우저 동작 방식을 설정할 수 있음.</li>
        <li><strong>인라인 스크립트(Inline Script):</strong> HTML 내부에 직접 작성된 script 코드로, CSP 설정 시 기본적으로 차단 대상이 되어 XSS 방지에 기여함.</li>
      </ul>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details>
    <summary><span class="accordion-title">OWASP Security Risks </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      OWASP(Open Web Application Security Project)는 웹 애플리케이션 보안 분야에서 무료로 이용 가능한 기사, 방법론, 문서, 도구 및 기술을 제공하는 온라인 커뮤니티이다.
      </p>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details>
    <summary><span class="accordion-title">SSL/TLS </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      SSL(Secure Sockets Layer)과 TLS(Transport Layer Security)는 인터넷 통신 보안을 제공하는 데 사용되는 암호화 프로토콜이다. 이 프로토콜들은 웹을 통해 전송되는 데이터를 암호화하므로 패킷을 가로채려는 사람은 데이터를 해석할 수 없다. 중요한 차이점 중 하나는 SSL이 보안 결함으로 인해 더 이상 사용되지 않으며 대부분의 최신 웹 브라우저에서 더 이상 지원되지 않는다는 것이다. 하지만 TLS는 여전히 안전하고 널리 지원되므로 TLS를 사용하는 것이 좋다.
      </p>
      <p><strong>정리: SSL/TLS는 인터넷 통신을 암호화·인증·무결성 검증으로 보호하는 보안 프로토콜이다.</strong></p>
    </div>
  </details>

  <!-- 박스 추가 -->
  <details>
    <summary><span class="accordion-title">Server Security </span> <span class="indicator">펼치기</span></summary>
    <div class="accordion-content">
      <p>
      서버 보안은 서버를 위협과 취약점으로부터 보호하여 관리하는 데이터와 서비스의 기밀성, 무결성, 가용성을 보장하는 것을 의미한다. 주요 보안 수칙은 다음과 같다.
        <ol>
          <li><strong>패치 관리:</strong> 취약점을 수정하기 위해 소프트웨어와 운영 체제를 정기적으로 업데이트한다.</li>
          <li><strong>접근 제어:</strong> 강력한 인증 메커니즘을 구현하고 권한이 있는 사용자에게만 접근을 제한한다.</li>
          <li><strong>방화벽 및 침입 탐지:</strong> 방화벽을 사용하여 무단 액세스를 차단하고 침입 탐지 시스템을 사용하여 의심스러운 활동을 모니터링하고 대응한다.</li>
          <li><strong>암호화:</strong> 전송 중인 데이터와 저장 중인 데이터를 모두 암호화하여 민감한 정보를 무단 액세스로부터 보호한다.</li>
          <li><strong>보안 강화:</strong> 최소한의 서비스와 기능으로 서버를 구성하고, 보안 모범 사례를 적용하여 공격 표면을 줄인다.</li>
          <li><strong>정기적 백업:</strong> 데이터가 손실되거나 손상된 경우 복구할 수 있도록 정기적 백업을 수행한다.</li>
          <li><strong>모니터링 및 로깅:</strong> 서버 활동을 지속적으로 모니터링하고 감사를 위해 로그를 유지 관리하며 잠재적인 보안 사고를 감지한다.</li>
        </ol>
      </p>
    </div>
  </details>

</div>
</details>
