# TIL
basic
# 동기
 - 스프링부트로 프로젝트를 쉽고 빠르게 생성했지만, 스프링의 원리를 공부하기 위해 dependencies는 생성하지 않는다.
 - 원리를 공부하기전 스프링이 없던 시절 개발로 먼저 개발을 해보면서 스프링을 하나씩 도입하면서 스프링을 익히기 위해.

# 프로젝트 개발환경
- Language : JAVA
- IDE : IntelliJ
- Spring Boot : 2.5.4
- Packaging : Jar
- JAVA : 11

# 요구사항
 - 회원   
    -- 회원을 가입하고 조회를 할 수 있다.  
    -- 회원등급은 2가지로 일반등급과 VIP등급이 존재한다.  
    -- 회원 데이터는 DB를 구축할지, 외부 시스템과 연동할지 (미확정)  
    
 - 주문과 할인 정책  
   -- 회원은 상품을 조회할 수 있다.  
   -- 회원등급에 따라 할인 정책을 적용할 수 있다.  
   -- 할인 정책은 모든 VIP는 1000원을 할인해주는 고정 금액 할인을 적용해야함(추후 변경 가능성 높음)  
   -- 할인 정책은 변경 가능성이 높기 때문에 (미확정)  
   
 # 새로운 할인 정책 개발
  - 기존 고정 할인금액에서 퍼센트로 할인 정책을 변경  
  - 변경시 기존 구현체의 코드 수정으로 인하여 OCP/DIP 같은 객체지향 설계 원칙 위배함  
  - 의존관계를 인터페이스에만 의존하도록 변경 해야함  
  - 애플리케이션의 전체 동작 방식을 구성(config)하기 위해, 구현 객체를 생성하고, 연결하는 책임을 가지는 별도의 설정 클래스 생성.  
  - 인터페이스에 의존하게 되고 구현체에는 더이상 의존하지 않게됨 - DIP 해결
  - 정책등 변경 발생 시 구현체를 변경하지 않으면서 확장 가능해짐 - OCP 해결  

# 스프링으로 전환
 - 스프링 컨테이너는 @Cofiguration이 붙은 AppConfig를 설정 정보로 사용
 - @Bean이라 적힌 메서드를 모두 호출해서 반환된 객체를 스프링 컨테이너에 등록한다
 - @ComponentScan과 @Autowired를 이용한 의존관계 자동 주입
