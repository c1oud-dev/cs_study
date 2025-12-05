---
layout: default
title: "Spring Interview — 완벽 가이드"
---

<p class="breadcrumb"><a href="/cs_study/home.html">🏠 홈으로</a></p>

<section>
  <h2>스프링 면접 대비</h2>
  <p>구성: 📋 기본 면접 Q&amp;A → 💡 추가 예상 질문 Q&amp;A → 📚 면접 팁</p>
</section>

<!-- ① 기본 면접 Q&A -->
<details open>
  <summary><span class="accordion-title">📋 기본 면접 Q&amp;A</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">

<details>
    <summary style="font-size:1rem;"><b>Q1. 스프링 프레임워크란 무엇이며 주요 특징은?</b></summary>
    <div class="accordion-content">
    <p>스프링은 자바 기반의 오픈소스 애플리케이션 프레임워크로, 엔터프라이즈 애플리케이션 개발을 쉽게 만들어줍니다.</p>
    <p>주요 특징: <b>IoC(Inversion of Control)</b> — 객체의 생성과 의존성 관리를 컨테이너가 담당 / <b>DI(Dependency Injection)</b> — 의존성을 외부에서 주입 / <b>AOP(Aspect-Oriented Programming)</b> — 횡단 관심사 분리 / <b>PSA(Portable Service Abstraction)</b> — 서비스 추상화 / <b>경량 컨테이너</b> — 기존 EJB 대비 가벼움.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q2. IoC(Inversion of Control)와 DI(Dependency Injection)를 설명해주세요.</b></summary>
    <div class="accordion-content">
    <p><b>IoC(제어의 역전)</b>은 객체 생성·생명주기·의존관계를 프레임워크가 관리하는 개념이고, <b>DI(의존성 주입)</b>은 IoC를 구현하는 방식입니다.</p>
    <p><b>생성자 주입</b>(권장), <b>세터 주입</b>, <b>필드 주입</b>(비권장)이 있습니다.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q3. 스프링 빈(Bean)이란 무엇이며 스코프는 어떤 것들이 있나요?</b></summary>
    <div class="accordion-content">
    <p>스프링 빈은 IoC 컨테이너가 관리하는 객체입니다. 등록 어노테이션: @Component, @Service, @Repository, @Controller, 또는 @Bean.</p>
    <p><b>스코프</b>: <b>singleton</b>(기본), <b>prototype</b>, <b>request</b>, <b>session</b>, <b>application</b>.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q4. @Component, @Service, @Repository, @Controller의 차이점은?</b></summary>
    <div class="accordion-content">
    <p>모두 @Component 특수화. <b>@Service</b>는 서비스 레이어, <b>@Repository</b>는 DAO 계층(예외 번역), <b>@Controller</b>는 웹 요청 처리.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q5. ApplicationContext와 BeanFactory의 차이점은?</b></summary>
    <div class="accordion-content">
    <p><b>BeanFactory</b>: 기본 DI, 지연 로딩. <b>ApplicationContext</b>: BeanFactory + 국제화/이벤트/AOP 등, 즉시 로딩이 일반적.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q6. AOP(Aspect-Oriented Programming)란 무엇인가요?</b></summary>
    <div class="accordion-content">
    <p><b>Aspect</b>, <b>Advice</b>(@Before/@After/@Around), <b>Pointcut</b>, <b>Join Point</b>, <b>Weaving</b>. 스프링은 프록시 기반 런타임 위빙.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q7. 스프링에서 트랜잭션 처리는 어떻게 하나요?</b></summary>
    <div class="accordion-content">
    <p><b>선언적 트랜잭션</b>(@Transactional), <b>전파</b>(REQUIRED/REQUIRES_NEW/NESTED...), <b>격리 수준</b>(DEFAULT/READ_COMMITTED/...), <b>readOnly</b> 최적화.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q8. @Autowired 동작 원리와 주입 방법들을 설명해주세요.</b></summary>
    <div class="accordion-content">
    <p>AutowiredAnnotationBeanPostProcessor가 타입 기준 자동 주입. <b>생성자 주입</b>(권장), <b>세터</b>, <b>필드</b>(비권장).</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q9. 스프링 MVC의 구조와 동작 과정을 설명해주세요.</b></summary>
    <div class="accordion-content">
    <p>DispatcherServlet(Front Controller) 중심. 요청 → 매핑 → 컨트롤러 실행 → ModelAndView → ViewResolver → View 렌더링.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q10. @RequestMapping과 관련 어노테이션들을 설명해주세요.</b></summary>
    <div class="accordion-content">
    <p><b>@RequestMapping</b> 및 <b>@Get/Post/Put/Delete/PatchMapping</b>, @PathVariable 등으로 세밀한 매핑 구성.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q11. @ModelAttribute와 @RequestParam의 차이점은?</b></summary>
    <div class="accordion-content">
    <p><b>@RequestParam</b>: 단일 값 바인딩. <b>@ModelAttribute</b>: 객체 바인딩(자동 Model 추가).</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q12. 스프링 부트(Spring Boot)의 특징과 장점은?</b></summary>
    <div class="accordion-content">
    <p><b>Auto Configuration</b>, <b>Starter</b>, <b>Embedded Server</b>, <b>Actuator</b>, <b>Convention over Configuration</b>.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q13. @Configuration과 @Bean의 역할은?</b></summary>
    <div class="accordion-content">
    <p><b>@Configuration</b>은 설정 클래스(프록시로 싱글톤 보장), <b>@Bean</b>은 메서드 반환 객체를 빈으로 등록.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q14. 스프링의 예외 처리 방법들을 설명해주세요.</b></summary>
    <div class="accordion-content">
    <p><b>@ExceptionHandler</b>, <b>@ControllerAdvice</b>/<b>@RestControllerAdvice</b>, <b>ResponseEntityExceptionHandler</b>, <b>HandlerExceptionResolver</b>.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q15. 스프링 시큐리티의 기본 개념과 인증/인가 과정을 설명해주세요.</b></summary>
    <div class="accordion-content">
    <p><b>Security Filter Chain</b>, <b>Authentication</b>, <b>SecurityContext</b>, <b>UserDetailsService</b>, <b>PasswordEncoder</b>.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q16. 스프링에서 프로파일(Profile)과 프로퍼티(Properties) 관리는?</b></summary>
    <div class="accordion-content">
    <p><b>@Profile</b>로 환경별 빈, <b>application.yml</b>과 <b>@Value</b>/<b>@ConfigurationProperties</b>로 설정 바인딩.</p>
    </div>
</details>

  </div>
</details>

<!-- ② 추가 예상 질문 Q&A -->
<details>
  <summary><span class="accordion-title">💡 추가 예상 질문 Q&amp;A</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">
    <details>
      <summary style="font-size:1rem;"><b>Q17. 스프링의 빈 생명주기(Bean Lifecycle)를 설명해주세요.</b></summary>
      <div class="accordion-content">
        <p>인스턴스화 → 프로퍼티 설정 → Aware 콜백 → <b>@PostConstruct</b> → <b>afterPropertiesSet()</b> → 사용 → <b>@PreDestroy</b> → <b>destroy()</b>. <b>BeanPostProcessor</b>로 전/후 처리 가능.</p>
      </div>
    </details>

<details>
    <summary style="font-size:1rem;"><b>Q18. 스프링 데이터 JPA의 주요 기능들을 설명해주세요.</b></summary>
    <div class="accordion-content">
    <p><b>Repository</b> 상속, <b>쿼리 메서드</b>, <b>@Query</b>(JPQL/네이티브), <b>Specifications</b>, <b>페이징/정렬</b>, <b>Auditing</b>.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q19. @Transactional의 속성들과 주의사항은?</b></summary>
    <div class="accordion-content">
    <p><b>전파</b>, <b>격리</b>, <b>readOnly</b>, <b>rollbackFor</b>. private 메서드/내부 호출은 프록시를 거치지 않음, 체크 예외 기본 미롤백.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q20. 스프링 부트의 자동 설정(Auto Configuration) 원리는?</b></summary>
    <div class="accordion-content">
    <p><b>@EnableAutoConfiguration</b>, <b>spring.factories</b>, <b>@Conditional*</b>, <b>AutoConfigurationImportSelector</b>.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q21. REST API 설계 시 스프링에서 사용하는 어노테이션들은?</b></summary>
    <div class="accordion-content">
    <p><b>@RestController</b>, <b>@Get/Post/Put/Delete/PatchMapping</b>, <b>@PathVariable</b>, <b>@RequestParam</b>, <b>@RequestBody</b>, <b>ResponseEntity</b>, <b>@Valid</b>/<b>@Validated</b>.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q22. 스프링의 캐시(Cache) 기능을 설명해주세요.</b></summary>
    <div class="accordion-content">
    <p><b>@EnableCaching</b>, <b>@Cacheable</b>, <b>@CachePut</b>, <b>@CacheEvict</b>, SpEL 조건, 다양한 CacheManager.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q23. 스프링 WebFlux와 기존 Spring MVC의 차이점은?</b></summary>
    <div class="accordion-content">
    <p><b>MVC</b>: 동기/블로킹(요청당 스레드). <b>WebFlux</b>: 비동기/논블로킹(이벤트 루프), 반환 타입 <b>Mono/Flux</b>.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q24. 스프링 클라우드의 주요 구성 요소들은?</b></summary>
    <div class="accordion-content">
    <p><b>Service Discovery</b>(Eureka/Consul), <b>API Gateway</b>, <b>Config</b>, <b>Circuit Breaker</b>, <b>Load Balancer</b>, <b>Distributed Tracing</b>.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q25. 스프링의 테스트 지원 기능들을 설명해주세요.</b></summary>
    <div class="accordion-content">
    <p><b>@SpringBootTest</b>, <b>@WebMvcTest</b>, <b>@DataJpaTest</b>, <b>@MockBean</b>, <b>@TestPropertySource</b>, <b>@DirtiesContext</b>, <b>Testcontainers</b>.</p>
    </div>
</details>

  </div>
</details>

<!-- ④ 면접 팁 -->
<details>
  <summary><span class="accordion-title">📚 면접 팁</span> <span class="indicator">펼치기</span></summary>
  <div class="accordion-content">
    <ol>
      <li><b>핵심 개념 이해</b>: IoC/DI, AOP, PSA</li>
      <li><b>실무 경험 강조</b>: 사용 스택과 문제 해결 사례</li>
      <li><b>최신 동향</b>: Boot, Cloud, WebFlux</li>
      <li><b>성능 최적화</b>: 트랜잭션/캐시/N+1</li>
      <li><b>테스트 전략</b>: 단위·통합 테스트</li>
      <li><b>문제 해결</b>: 이슈와 해결 과정</li>
    </ol>
  </div>
</details>
