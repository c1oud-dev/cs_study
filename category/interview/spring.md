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
    <summary style="font-size:1rem;"><b>Q1. 스프링 프레임워크란 무엇이며 주요 특징은?</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
    <div class="accordion-content">
    <p>스프링 프레임워크는 자바 기반 엔터프라이즈 애플리케이션을 만들기 위한 오픈소스 프레임워크로, 인프라 코드를 공통으로 제공해서 개발자가 비즈니스 로직에 집중할 수 있게 해주는 기반 기술이라고 이해하고 있습니다.</p>
    <p>가장 핵심적인 특징은 IoC/DI(Inversion of Control / Dependency Injection) 입니다. 객체 생성과 의존성 주입을 스프링 컨테이너가 대신 관리해 주기 때문에, 클래스들이 서로 강하게 결합되지 않고 느슨하게 연결됩니다. 그 결과로 테스트가 쉬워지고, 구현체 교체나 구조 변경에 유연한 설계가 가능해집니다.</p>
    <p>또 하나의 특징은 AOP(Aspect Oriented Programming) 지원입니다. 로그, 트랜잭션, 보안처럼 여러 계층에 공통으로 흩어지는 관심사를 별도의 관점으로 분리해서 관리할 수 있습니다. 이를 통해 핵심 비즈니스 로직과 공통 기술 로직을 분리해서 코드를 더 깔끔하고 유지보수하기 좋게 만들 수 있습니다.</p>
    <p>스프링은 POJO 기반의 경량 프레임워크라는 점도 중요합니다. 특정 컨테이너나 규격에 강하게 묶이지 않은 일반적인 자바 객체를 중심으로 개발할 수 있고, XML뿐만 아니라 애노테이션과 자바 설정을 통해 유연하게 설정할 수 있습니다. 여기에 더해 트랜잭션 관리, 데이터 접근(JDBC/JPA 등), 스프링 MVC 웹 계층까지 전체 애플리케이션 레이어를 아우르는 기능을 제공합니다.</p>
    <p>마지막으로, 단순 프레임워크를 넘어서 풍부한 생태계를 가지고 있다는 것도 큰 장점입니다. 예를 들어 스프링 부트(Spring Boot), 스프링 데이터, 스프링 시큐리티 같은 프로젝트들과 연계해서 사용하면, 설정은 최소화하면서도 실무에서 필요한 기능들을 빠르게 갖춘 애플리케이션을 만들 수 있다는 점이 스프링 프레임워크의 큰 강점이라고 생각합니다.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q2. IoC(Inversion of Control)와 DI(Dependency Injection)를 설명해주세요.</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
    <div class="accordion-content">
    <p>IoC와 DI는 스프링을 이해할 때 가장 중요한 개념이라고 생각합니다.</p>
    <p>먼저 IoC(Inversion of Control, 제어의 역전) 는 말 그대로 “제어 흐름이 뒤바뀌는 것”을 의미합니다. 원래는 객체를 누가 만들지, 언제 생성하고 언제 연결할지, 어떤 구현체를 쓸지 등을 애플리케이션 코드가 직접 결정합니다. 그런데 IoC 환경에서는 이런 제어 권한을 프레임워크나 컨테이너에게 넘기고, 우리는 규약에 맞게 코드만 작성하는 구조가 됩니다. 즉, “내가 라이브러리를 호출하는” 게 아니라, “프레임워크가 내가 만든 코드를 호출해 주는 구조”가 IoC라고 이해하고 있습니다. 이를 통해 객체 생성과 생명주기 관리가 분리되어, 애플리케이션 코드는 비즈니스 로직에 집중할 수 있습니다.</p>
    <p>DI(Dependency Injection, 의존성 주입) 는 IoC를 구체적으로 구현하는 방법 중 하나입니다. 어떤 객체가 사용할 다른 객체를 직접 new로 생성하는 대신, 외부에서 주입받는 방식입니다. 예를 들어 스프링 컨테이너가 미리 빈(Bean)을 생성해 두고, 생성자나 세터, 필드 등을 통해 필요한 의존성을 대신 넣어 줍니다. 이렇게 하면 클래스는 “어떤 구현체를 쓸지”에 대해 몰라도 되고, 단지 “이 인터페이스가 필요하다”는 의존 관계만 선언하면 되기 때문에 결합도가 낮아지고, 테스트 시에 Mock 객체로 쉽게 교체할 수 있다는 장점이 있습니다.</p>
    <p>정리하면, IoC는 전체적인 제어 권한을 프레임워크가 가져가는 큰 개념이고, DI는 그 안에서 객체 간 의존성을 외부에서 주입함으로써 IoC를 실현하는 구체적인 기법이라고 이해하고 있습니다.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q3. 스프링 빈(Bean)이란 무엇이며 스코프는 어떤 것들이 있나요?</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
    <div class="accordion-content">
    <p>스프링 빈은 스프링 컨테이너가 관리하는 객체를 말합니다. 개발자가 직접 new로 생성하고 의존성을 연결하는 대신, 스프링이 설정 정보나 애노테이션(@Component, @Service, @Repository, @Controller, @Configuration 등)을 보고 객체를 만들고, 의존성을 주입하고, 생명주기까지 관리해 주는 대상이 바로 빈이라고 이해하고 있습니다. 그래서 애플리케이션 코드에서는 “어떻게 생성할지”보다는 “어떤 빈이 필요한지”에만 집중할 수 있고, 테스트나 교체도 훨씬 유연해집니다.</p>
    <p>스프링 빈에는 여러 가지 스코프(scope) 가 있는데, 대표적으로 다음과 같이 정리할 수 있습니다.</p>
    <p>가장 많이 쓰이는 것은 singleton 스코프입니다. 싱글톤 스코프는 스프링 컨테이너당 인스턴스를 하나만 생성해서 전체에서 공유하는 방식이고, 별도 설정을 하지 않으면 기본값으로 사용됩니다. 대부분의 서비스/리포지토리 빈이 싱글톤으로 관리되고, 메모리 사용과 성능 측면에서 효율적이기 때문에 기본 선택이라고 보면 됩니다.</p>
    <p>그다음은 prototype 스코프입니다. 프로토타입 스코프는 스프링 컨테이너에 빈을 요청할 때마다 항상 새로운 인스턴스를 생성해서 반환합니다. 컨테이너는 생성까지만 관여하고 이후 생명주기는 직접 관리해야 합니다. 주로 상태를 내부에 많이 가지고, 매번 새로 써야 하는 객체가 필요할 때 고려할 수 있습니다.</p>
    <p>웹 애플리케이션에서는 request, session, application 같은 웹 스코프도 있습니다.</p>
    <ul>
      <li>request 스코프는 HTTP 요청 하나당 빈 인스턴스를 하나 생성해서, 그 요청이 처리되는 동안만 유지합니다.</li>
      <li>session 스코프는 HTTP 세션마다 하나씩 생성해서 사용자의 세션이 유지되는 동안 공유합니다.</li>
      <li>application 스코프는 서블릿 컨텍스트 단위로 하나만 만들어져 애플리케이션 전체에서 공유됩니다.</li>
    </ul>
    <p>정리하면, 스프링 빈은 컨테이너가 생성·주입·관리하는 객체이고, 스코프는 그 빈의 생성 시점과 생존 범위를 정의하는 개념입니다. 실무에서는 기본적으로 싱글톤을 사용하되, 필요에 따라 프로토타입이나 웹 스코프 빈을 선택하는 식으로 설계하는 것이 일반적이라고 생각합니다.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q4. @Component, @Service, @Repository, @Controller의 차이점은?</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
    <div class="accordion-content">
    <p>@Component, @Service, @Repository, @Controller는 전부 스프링이 빈으로 등록해서 관리하도록 표시하는 컴포넌트 스캔 대상 애노테이션이고, 각각 어느 레이어를 담당하는지 나타내는 “역할 이름(스테레오타입)”이라고 이해하고 있습니다.</p>
    <p>먼저 @Component는 가장 기본이 되는 애노테이션으로, “스프링이 관리해야 할 일반적인 빈”일 때 사용합니다. 특정 계층에 한정되지 않고, 유틸성 클래스나 공통 컴포넌트처럼 어디에도 딱 맞지 않는 경우에 주로 사용합니다.</p>
    <p>@Service는 비즈니스 로직을 담당하는 서비스 계층을 나타내는 스테레오타입입니다. 기능적으로는 @Component와 거의 동일하지만, 코드만 봐도 “여기는 도메인/비즈니스 로직을 처리하는 서비스 레이어구나”를 알 수 있어서 레이어 구분과 역할 표현에 도움이 됩니다. 트랜잭션 AOP를 적용할 때도 주로 서비스 계층 메서드에 붙이는 패턴을 많이 씁니다.</p>
    <p>@Repository는 데이터 접근 계층(DAO, Repository) 을 나타내며, 여기서 중요한 차이는 스프링이 이 애노테이션이 붙은 클래스에 대해 데이터 접근 예외를 스프링의 DataAccessException 계층 구조로 변환해 주는 기능을 제공한다는 점입니다. 그래서 단순히 이름만 다른 게 아니라, 예외 변환(AOP)까지 함께 적용되는 레이어 전용 애노테이션이라고 이해하고 있습니다.</p>
    <p>마지막으로 @Controller는 웹 MVC에서 요청을 처리하는 프레젠테이션 계층을 의미합니다. 클라이언트의 HTTP 요청을 받아서 모델을 만들고 뷰를 반환하는 역할을 하고, REST API를 만들 때는 @Controller에 @ResponseBody가 결합된 형태인 @RestController를 사용합니다.</p>
    <p>정리하면, 네 애노테이션 모두 스프링 빈이 되도록 도와주지만,</p>
    <ul>
      <li>@Component는 일반 컴포넌트,</li>
      <li>@Service는 비즈니스 로직,</li>
      <li>@Repository는 데이터 접근 + 예외 변환,</li>
      <li>@Controller는 웹 계층 요청 처리</li>
    </ul>
    <p>라는 각 레이어의 역할을 표현하기 위해 구분해서 사용한다고 생각합니다.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q5. ApplicationContext와 BeanFactory의 차이점은?</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
    <div class="accordion-content">
    <p>스프링에서 BeanFactory와 ApplicationContext는 둘 다 IoC 컨테이너이고, ApplicationContext가 BeanFactory를 확장한 상위 개념입니다.</p>
    <p>먼저 BeanFactory는 가장 기본적인 컨테이너로, 빈 생성과 의존성 주입 같은 핵심 DI 기능만 제공합니다. 기본 전략은 필요해질 때까지 빈을 만들지 않는 지연 로딩(lazy loading)이고, 부가적인 애플리케이션 지원 기능은 거의 없습니다.</p>
    <p>반대로 ApplicationContext는 BeanFactory 기능을 모두 포함하면서, 실무에서 바로 쓰기 좋은 기능들이 추가된 컨테이너입니다.</p>
    <p>예를 들어</p>
    <ul>
      <li>메시지 국제화 처리</li>
      <li>이벤트 발행과 리스너 등록</li>
      <li>Environment·프로파일 기반 설정 관리</li>
      <li>AOP 적용, 리소스 로딩</li>
    </ul>
    <p>같은 것들을 지원해서 애플리케이션 전반을 관리하는 역할을 합니다. 그리고 보통 애플리케이션 시작 시점에 필요한 빈을 한 번에 초기화해서, 런타임 동안 더 안정적으로 동작하게 합니다.</p>
    <p>정리하면, BeanFactory는 “가장 기본적인 DI 컨테이너”이고, ApplicationContext는 “BeanFactory에 각종 부가 기능을 올린 실무용 컨테이너”라서 실제 개발에서는 거의 항상 ApplicationContext를 사용한다고 정리할 수 있습니다.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q6. AOP(Aspect-Oriented Programming)란 무엇인가요?</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
    <div class="accordion-content">
    <p>AOP는 <b>관점 지향 프로그래밍</b>이라고 하고, 한마디로 말하면 <b>비즈니스 로직과 공통으로 반복되는 부가 기능을 깔끔하게 분리해서 모듈화하는 방식</b>입니다.</p>
    <p>실제 서비스 코드를 짜다 보면, 메서드마다 <b>로그 출력, 트랜잭션 처리, 보안 체크, 성능 측정</b> 같은 코드가 계속 반복해서 들어가게 됩니다. 이런 것들을 AOP에서는 <b>공통 관심사(cross-cutting concern)</b>라고 부르고, 별도의 모듈인 <b>Aspect</b>로 분리해서 한 곳에 모아둔 다음, <b>필요한 지점에만 붙여서 사용</b>합니다.</p>
    <p>이렇게 하면 <b>핵심 비즈니스 로직은 그대로 깔끔하게 유지</b>하고, 공통 기능은 Aspect 쪽에서 관리하기 때문에 <b>중복 코드가 줄어들고, 비즈니스 코드가 읽기 쉬워지고, 공통 기능을 변경할 때도 한 군데만 수정하면 된다</b>는 장점이 있습니다.</p>
    <p>그리고 스프링에서는 <b>프록시 기반 AOP</b>를 많이 쓰는데, 대표적인 예가 <b>@Transactional</b>입니다. 메서드에 이 애노테이션만 붙이면 <b>트랜잭션 시작·커밋·롤백 로직이 메서드 호출 앞뒤에 자동으로 적용</b>되기 때문에, 이 부분이 <b>AOP의 대표적인 활용 사례</b>라고 설명할 수 있습니다.</p>
    </div>
</details> 

<details>
    <summary style="font-size:1rem;"><b>Q7. 스프링에서 트랜잭션 처리는 어떻게 하나요?</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
    <div class="accordion-content">
    <p>스프링에서는 보통 선언적 트랜잭션을 사용해서 트랜잭션을 관리합니다. 핵심은 @Transactional 애노테이션과 PlatformTransactionManager 조합입니다.</p>
    <p>실무에서는 주로 서비스 레이어 메서드에 @Transactional을 붙여서 하나의 비즈니스 로직 단위를 트랜잭션 경계로 잡습니다. 메서드가 시작될 때 스프링이 트랜잭션을 열어주고, 예외 없이 정상 종료되면 커밋, 런타임 예외(언체크 예외)가 발생하면 자동으로 롤백하는 방식입니다. 체크 예외는 기본적으로 롤백 대상이 아니고, 필요하면 rollbackFor 속성으로 조정합니다.</p>
    <p>내부적으로는 스프링이 AOP 프록시를 만들어서, 메서드 호출 앞뒤에 트랜잭션 시작·커밋·롤백 로직을 끼워 넣습니다. 개발자는 비즈니스 로직에만 집중하고, 트랜잭션 처리 코드는 신경 쓰지 않아도 되는 점이 장점입니다.</p>
    <p>또한 @Transactional의 옵션으로 트랜잭션 전파 방식(propagation), 격리 수준(isolation level), 읽기 전용 여부(readOnly) 등을 설정해서 동시성이나 성능 요구사항에 맞게 세밀하게 조정할 수 있습니다.</p>
    <p>필요하다면 PlatformTransactionManager나 TransactionTemplate을 사용해서 직접 트랜잭션 경계를 코드로 잡는 프로그래밍 방식 트랜잭션도 쓸 수 있지만, 일반적인 비즈니스 로직에서는 @Transactional을 사용하는 선언적 방식이 보편적입니다.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q8. @Autowired 동작 원리와 주입 방법들을 설명해주세요.</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
    <div class="accordion-content">
    <p>@Autowired는 스프링 컨테이너가 필요한 빈을 타입 기준으로 찾아서 자동으로 주입해 주는 애노테이션입니다.</p>
    <p>먼저 동작 원리를 간단히 말하면, 스프링이 컨테이너를 초기화할 때 @Autowired가 붙은 생성자/필드/메서드를 스캔하고, 그 타입과 맞는 빈을 컨테이너에서 찾아서 넣어 줍니다. 같은 타입의 빈이 여러 개면 @Qualifier, 빈 이름, @Primary 같은 정보들을 보고 최종 후보 하나를 결정하고요. 이 과정은 내부적으로 BeanPostProcessor가 담당해서, 개발자가 new로 객체를 만들 필요가 없게 됩니다.</p>
    <p>주입 방법은 크게 세 가지로 나눌 수 있습니다.</p>
    <ol>
      <li>생성자 주입</li>
      <ul>
        <li>생성자 파라미터에 @Autowired를 붙이거나, 생성자가 한 개뿐이면 생략해도 됩니다.</li>
        <li>의존성이 없으면 객체를 만들 수 없어서, 설계 상으로도 더 안전하고 테스트하기도 편해서 실무에서 가장 권장되는 방식입니다.</li>
      </ul>
      <li>필드 주입</li>
      <ul>
        <li>필드 위에 바로 @Autowired를 붙이는 방식입니다.</li>
        <li>코드가 간단하긴 하지만, final을 못 쓰고, 테스트나 리팩터링 시에 불편해서 보통은 지양하는 편이고, 간단한 예제나 레거시 코드에서 많이 보입니다.</li>
      </ul>
      <li>수정자(Setter) / 일반 메서드 주입</li>
      <ul>
        <li>setter 메서드나 특정 메서드 파라미터에 @Autowired를 붙이는 방식입니다.</li>
        <li>선택적인 의존성이나, 변경 가능한 의존성을 넣을 때 사용할 수 있습니다.</li>
      </ul>
    </ol>
    <p>추가로, 주입 대상이 선택 사항일 때는 required = false나 @Nullable을 같이 써서 빈이 없어도 예외가 나지 않도록 조절할 수 있습니다.</p>
    <p>정리하자면, @Autowired는 스프링 컨테이너가 타입을 기준으로 의존성을 자동 주입해 주는 기능이고, 주로 생성자 주입을 기본으로 사용하고, 필드/세터 주입은 상황에 따라 보조적으로 사용한다 정도로 설명할 수 있습니다.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q9. 스프링 MVC의 구조와 동작 과정을 설명해주세요.</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
    <div class="accordion-content">
    <p>스프링 MVC는 프론트 컨트롤러 패턴을 쓰는 웹 MVC 프레임워크이고, 중심에는 DispatcherServlet이 있습니다. 구조를 간단히 말하면, DispatcherServlet – HandlerMapping – Controller – ViewResolver – View 이 흐름으로 이어집니다.</p>
    <p>동작 과정은 이렇게 설명할 수 있습니다.</p>
    <ol>
        <li>클라이언트가 HTTP 요청을 보내면, 서블릿 컨테이너가 그 요청을 먼저 DispatcherServlet으로 전달합니다. (보통 특정 URL 패턴으로 모든 요청을 몰아줍니다.)</li>
        <li>DispatcherServlet은 HandlerMapping을 통해 이 URL, HTTP 메서드(GET/POST 등)에 어떤 컨트롤러 메서드가 매핑되어 있는지 찾습니다. 여기서 @Controller, @RestController, @RequestMapping 같은 애노테이션 정보가 사용됩니다.</li>
        <li>찾아낸 컨트롤러 메서드가 호출되고, 내부에서 서비스, 리포지토리 등을 이용해 비즈니스 로직을 처리한 뒤 모델 데이터 + 논리적인 뷰 이름을 반환하거나, @RestController처럼 바디에 들어갈 응답 객체를 그대로 반환합니다.</li>
        <li>뷰 이름을 반환한 경우에는 DispatcherServlet이 ViewResolver를 사용해서 논리 이름을 실제 뷰(JSP, Thymeleaf 템플릿 등)로 바꾸고, 뷰에 모델 데이터를 넘겨서 화면을 렌더링합니다. 반대로 @ResponseBody나 @RestController인 경우에는 HttpMessageConverter를 통해 객체를 JSON 같은 형태로 변환해서 바로 응답 바디에 실어 보냅니다.</li>
        <li>최종적으로 렌더링된 결과나 JSON이 HTTP 응답으로 클라이언트에 전달됩니다.</li>
    </ol>
    <p>요약하면, 스프링 MVC는 DispatcherServlet을 중심으로 요청을 한 곳에서 받고, 핸들러 매핑을 통해 컨트롤러를 호출하고, ViewResolver·HttpMessageConverter를 통해 화면이나 JSON 응답을 만드는 구조라서 요청 처리, 비즈니스 로직, 뷰 렌더링이 명확하게 분리된다는 점이 핵심입니다.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q10. @RequestMapping과 관련 어노테이션들을 설명해주세요.</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
    <div class="accordion-content">
    <p>@RequestMapping은 한마디로, 어떤 URL에 어떤 HTTP 요청이 들어왔을 때, 어느 컨트롤러 메서드가 처리할지를 연결해 주는 애노테이션입니다.</p>
    <p>보통 컨트롤러 클래스 위에 한 번 붙여서 공통 경로를 잡아주고, 메서드마다 이 메서드는 /users 중에서도 /list를 처리한다, 이 메서드는 /users 중에서도 /detail을 처리한다 이런 식으로 더 구체적인 경로와 HTTP 메서드(GET, POST 등)를 지정해 줍니다. 이렇게 해서 스프링이 “이 URL + 이 메서드 조합이면 이 컨트롤러 메서드를 호출해야겠구나” 하고 매핑할 수 있게 됩니다.</p>
    <p>이 @RequestMapping을 조금 더 편하게 쓰기 위해서, 스프링에서는 HTTP 메서드별로 나뉜 관련 애노테이션들도 제공합니다. 예를 들면 @GetMapping, @PostMapping, @PutMapping, @DeleteMapping, @PatchMapping 같은 것들인데요, 각각 “GET 요청용 RequestMapping”, “POST 요청용 RequestMapping”처럼 보시면 되고, 특정 HTTP 메서드에 특화되어 있어서 코드가 훨씬 읽기 좋습니다.</p>
    <p>그리고 요청에서 넘어온 값을 메서드 파라미터로 어떻게 받을지도 여러 애노테이션으로 같이 정리합니다. 예를 들어 주소 경로 안에 들어 있는 값은 @PathVariable로, 쿼리 스트링이나 폼으로 넘어오는 값은 @RequestParam으로, JSON 같은 요청 본문은 @RequestBody로 받으면서, @RequestMapping이나 @GetMapping 같은 매핑 애노테이션과 함께 사용합니다.</p>
    <p>정리해서 말하면, @RequestMapping은 “요청 → 컨트롤러 메서드”를 연결하는 기본 애노테이션이고, @GetMapping, @PostMapping 같은 것들은 그걸 HTTP 메서드별로 줄여 쓴 형태, 그리고 @PathVariable, @RequestParam, @RequestBody 같은 애노테이션들은 요청 안에 들어 있는 다양한 데이터를 메서드 파라미터에 깔끔하게 바인딩해 주는 역할을 한다고 설명할 수 있습니다.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q11. @ModelAttribute와 @RequestParam의 차이점은?</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
    <div class="accordion-content">
    <p>스프링 MVC에서 @ModelAttribute랑 @RequestParam은 둘 다 요청 값을 컨트롤러 매개변수에 바인딩할 때 쓰는데, 쓰임새가 조금 다릅니다.</p>
    <p>먼저 @RequestParam은 말 그대로 “요청 파라미터 하나를 그대로 받겠다”는 의미에 가깝습니다. 쿼리 스트링이나 폼 데이터에서 단일 값을 가져올 때 주로 쓰이고, 예를 들면 페이지 번호, 검색어, 정렬 기준처럼 간단한 값들을 받을 때 사용합니다. 이 애노테이션을 쓰면 해당 파라미터가 필수인지 선택인지, 기본값은 무엇인지 이런 것들을 세밀하게 설정할 수 있습니다.</p>
    <p>반대로 @ModelAttribute는 요청에 들어 있는 여러 파라미터를 한 번에 모아서 객체(모델)에 바인딩하고 싶을 때 사용합니다. 회원 가입 폼처럼 이름, 이메일, 비밀번호, 나이처럼 필드가 많은 경우, 각각을 @RequestParam으로 하나씩 받기보다는, 도메인 객체나 DTO 하나를 매개변수로 두고 @ModelAttribute로 한 번에 묶어서 받는 식입니다.</p>
    <p>또 한 가지 차이는, @ModelAttribute로 바인딩된 객체는 자동으로 뷰에서 사용할 수 있는 모델에도 같이 실린다는 점입니다. 그래서 화면 렌더링할 때 폼 값 다시 뿌려주거나, 검증 에러와 함께 다시 보여줄 때 유용합니다.</p>
    <p>정리해서 말하면,</p>
    <ul>
        <li>@RequestParam → 단일 요청 파라미터를 바로 값으로 받고 싶을 때</li>
        <li>@ModelAttribute → 여러 요청 파라미터를 객체로 묶어서 받고, 동시에 모델에도 올리고 싶을 때</li>
    </ul>
    <p>이렇게 역할이 나뉜다고 설명할 수 있습니다.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q12. 스프링 부트(Spring Boot)의 특징과 장점은?</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
    <div class="accordion-content">
    <p>스프링 부트는 한마디로 스프링 애플리케이션을 빠르고 쉽게 만들 수 있게 도와주는 스프링 기반 프레임워크입니다.</p>
    <p>먼저 가장 큰 특징은 자동 설정입니다. <br>
    일반 스프링에서는 빈 설정, 설정 파일, XML이나 자바 설정을 일일이 많이 작성해야 하는데, 스프링 부트는 프로젝트에 포함된 라이브러리를 보고 웹 애플리케이션인지, JPA를 쓰는지 등을 스스로 판단해서 기본 설정을 자동으로 잡아 줍니다. 덕분에 설정 코드가 크게 줄어듭니다.</p>
    <p>둘째는 스타터 의존성 제공입니다. <br>
    웹, JPA, 시큐리티처럼 자주 쓰는 조합을 미리 묶어 둔 스타터를 제공해서, 필요한 기능을 의존성 하나 추가하는 것만으로 바로 가져다 쓸 수 있습니다. 어떤 라이브러리 버전을 맞춰야 할지 일일이 고민할 필요가 적어집니다.</p>
    <p>셋째는 내장 서버 지원입니다.<br>
    톰캣 같은 WAS를 따로 설치해서 올리는 게 아니라, 애플리케이션 안에 내장해서 실행하기 때문에, 그냥 애플리케이션을 실행하면 바로 서버가 뜹니다. 배포할 때도 실행 가능한 하나의 파일로 패키징해서 배포가 단순해집니다.</p>
    <p>넷째는 운영에 필요한 기능들을 기본으로 제공한다는 점입니다.<br>
    액추에이터 같은 기능을 통해 헬스 체크, 모니터링, 메트릭 수집 등을 쉽게 붙일 수 있어서, 개발뿐 아니라 운영 단계에서도 편리합니다. 설정 값 외부화 같은 부분도 잘 되어 있어서 환경별 설정 관리도 수월합니다.</p>
    <p>정리하자면, 스프링 부트의 특징과 장점은 복잡한 설정을 자동으로 처리해 주고, 필요한 의존성을 한 번에 묶어서 제공하고, 내장 서버와 모니터링 기능까지 갖춰서 개발자가 인프라 설정보다 비즈니스 로직에 더 집중할 수 있게 해 준다는 점이라고 설명할 수 있습니다.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q13. @Configuration과 @Bean의 역할에 대해서 설명해주세요.</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
    <div class="accordion-content">
    <p>@Configuration이랑 @Bean은 둘 다 스프링 설정을 자바 코드로 정의할 때 쓰는 애노테이션인데, 역할이 조금 다릅니다.</p>
    <p>먼저 @Configuration은 “이 클래스는 스프링 설정 클래스이고, 안에 있는 메서드들로 빈을 등록할 거야”라고 컨테이너에 알려주는 역할을 합니다. 그래서 @Configuration이 붙은 클래스는 예전 XML 설정 파일을 자바 코드로 옮겨 놓은 것처럼, 애플리케이션에서 사용할 빈들을 모아 두는 설정용 클래스라고 보면 됩니다. 이 클래스 자체도 하나의 빈으로 관리됩니다.</p>
    <p>그 안에서 @Bean은 “이 메서드가 반환하는 객체를 스프링 빈으로 등록해 달라”는 의미입니다. 메서드가 반환하는 객체가 컨테이너에 등록되고, 메서드 이름이 기본 빈 이름이 됩니다. 주로 외부 라이브러리처럼 내가 직접 new 해서 구성해야 하는 객체, 혹은 자동 컴포넌트 스캔으로 만들기 애매한 객체들을 등록할 때 많이 씁니다.</p>
    <p>하나 더 덧붙이면, @Configuration이 붙어 있으면 스프링이 내부적으로 프록시를 만들어서, @Bean 메서드끼리 서로를 호출하더라도 항상 컨테이너에 등록된 동일한 빈을 돌려주도록 처리해 줍니다. 그래서 싱글톤 빈이 깨지지 않고, 설정 코드 안에서 의존 관계를 안전하게 구성할 수 있습니다.</p>
    <p>정리해서 말하면, @Configuration은 “이 클래스는 빈 설정을 담고 있는 설정 클래스다”라고 표시하는 애노테이션이고, @Bean은 “이 메서드의 반환값을 스프링이 관리하는 빈으로 등록해 달라”라고 지정하는 애노테이션이라고 설명할 수 있습니다.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q14. 스프링의 예외 처리 방법들을 설명해주세요.</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
    <div class="accordion-content">
    <p>스프링의 예외 처리는 크게 컨트롤러 단 처리, 전역 공통 처리, HTTP 상태 코드·응답 제어 이 세 가지 관점으로 정리할 수 있습니다.</p>
    <p>먼저 컨트롤러 단에서는 기본적으로 try-catch로 바로 처리할 수도 있지만, 보통은 컨트롤러 안에 예외 타입별 메서드를 두고 @ExceptionHandler를 사용합니다. 이렇게 하면 비즈니스 로직 메서드는 예외만 던지고, 예외를 어떻게 응답으로 바꿀지는 별도의 메서드에서 담당하게 되어 역할을 분리할 수 있습니다.</p>
    <p>두 번째로, 예외 처리를 애플리케이션 전역에서 통일하고 싶을 때는 @ControllerAdvice나 @RestControllerAdvice를 사용합니다. 별도의 클래스를 하나 두고 공통 @ExceptionHandler 메서드들을 모아 두면, 모든 컨트롤러에서 발생한 예외를 한 곳에서 받아서 처리할 수 있고, 에러 코드, 메시지, 타임스탬프 같은 공통 에러 응답 포맷도 여기서 일관되게 관리할 수 있습니다. 실무에서는 주로 이 방식으로 전역 예외 처리 레이어를 만듭니다.</p>
    <p>세 번째로, HTTP 상태 코드와 응답 제어입니다. 예외 클래스나 핸들러에 @ResponseStatus를 붙여 특정 예외에 대해 400, 404, 500 같은 상태 코드를 매핑할 수 있고, 필요할 때는 ResponseStatusException을 던져 상태 코드와 메시지를 명시적으로 지정하기도 합니다. 전역 예외 처리 메서드에서 응답을 ResponseEntity로 감싸서 바디와 상태 코드를 함께 제어하는 방식도 자주 사용됩니다.</p>
    <p>마지막으로, 더 낮은 수준에서는 HandlerExceptionResolver라는 확장 포인트를 통해 프레임워크 레벨에서 예외를 가로채어 로깅이나 특수한 처리 로직을 추가할 수 있는 구조를 제공합니다.</p>
    <p>요약하면, 스프링은 @ExceptionHandler와 @ControllerAdvice 계층을 중심으로 예외를 처리하고, @ResponseStatus나 ResponseStatusException을 통해 HTTP 상태 코드와 응답 형식을 유연하게 제어할 수 있도록 설계되어 있습니다.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q15. 스프링 시큐리티의 기본 개념과 인증/인가 과정을 설명해주세요.</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
    <div class="accordion-content">
    <p>스프링 시큐리티는 한마디로 스프링 기반 애플리케이션에서 인증과 인가를 담당하는 보안 프레임워크입니다. 사용자가 “누구인지” 확인하는 게 인증, 그 사용자가 “무엇까지 할 수 있는지”를 확인하는 게 인가라고 할 수 있습니다.</p>
    <p>먼저 인증 과정부터 말해 보겠습니다.<br> 사용자가 로그인을 하거나, 토큰을 가지고 API를 호출하면 그 요청이 먼저 스프링 시큐리티의 필터 체인을 지나갑니다. 여기서 아이디·비밀번호나 토큰 같은 자격 증명을 꺼내서, 내부의 인증 매니저에게 넘깁니다.<br> 인증 매니저는 등록된 인증 프로바이더들을 통해 사용자 정보를 조회하고, 비밀번호가 맞는지, 토큰이 유효한지 등을 검사합니다.<br> 검증에 성공하면 사용자 정보와 권한이 들어 있는 Authentication 객체를 만들고, 이를 SecurityContext라는 곳에 저장합니다. 세션 기반이면 세션에도 연결되고, 토큰 기반이면 이후 요청마다 토큰에서 다시 복원해서 사용하게 됩니다.</p>
    <p>그 다음은 인가 과정입니다.<br> 인증이 끝난 뒤, 사용자가 어떤 URL에 접근하거나 컨트롤러 메서드를 호출하려고 하면, 시큐리티가 먼저 SecurityContext에 있는 Authentication을 보고 “이 사용자가 가진 권한이 이 리소스에 접근할 수 있는 수준인가?”를 검사합니다. 여기서 미리 설정해 둔 URL별 권한 규칙이나, 메서드 단위 권한 애노테이션에 정의한 규칙과 비교를 해서, 권한이 충분하면 요청을 계속 진행시키고, 아니면 403 같은 접근 거부 응답을 돌려줍니다.</p>
    <p>정리해서 말하면, 스프링 시큐리티는 필터 체인을 통해 요청 초입에서 공통 보안 로직을 처리하고, 인증 단계에서 사용자 정보를 확정한 뒤, 인가 단계에서 권한 규칙을 적용해서 접근을 제어하는 구조라서, 비즈니스 로직과 보안 로직을 깔끔하게 분리할 수 있다는 점이 핵심입니다.</p>
    </div>
</details>

<details>
    <summary style="font-size:1rem;"><b>Q16. 스프링에서 프로파일(Profile)과 프로퍼티(Properties) 관리는?</b><span style="float:right;">✅🟩🟩🟩🟩</span></summary>
    <div class="accordion-content">
    <p>스프링에서 프로파일은 환경별 빈 구성 세트를 나누는 기능이고, 프로퍼티 관리는 그 환경별 설정 값들을 외부에서 관리하는 메커니즘입니다.</p>
    <p>프로파일은 보통 dev, test, prod처럼 나누어 사용하며, 개발에선 H2, 운영에선 RDS처럼 환경마다 다른 빈과 설정을 선택적으로 활성화할 때 사용합니다. 특정 설정 클래스나 빈에 프로파일을 걸어 두면, 활성화된 프로파일에 따라서 로딩되는 빈 구성이 달라집니다.</p>
    <p>프로퍼티는 이렇게 나뉜 환경에서 필요한 값을 application 기본 설정과 application-dev, application-prod 같은 프로파일별 설정 파일에 분리해 두고, 공통 값은 기본 파일에, 환경에 따라 달라지는 값은 프로파일별 파일이나 환경 변수로 오버라이드하는 방식으로 관리합니다. 이때 DB URL, 계정, API 키처럼 민감한 값은 코드나 Git이 아니라 환경 변수나 외부 설정 서버를 통해 주입하는 것이 일반적입니다.</p>
    <p>정리하면, 프로파일로 “어떤 설정 묶음을 쓸지”를 고르고, 프로퍼티로 그 안의 구체적인 값을 환경별로 외부화해 관리한다라고 설명할 수 있습니다.</p>
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
