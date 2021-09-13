# TIL
basic
# 동기
 - 스프링부트로 프로젝트를 쉽고 빠르게 생성했지만, 스프링의 원리를 공부하기 위해 dependencies는 생성하지 않는다.
 - 원리를 공부하기전 스프링이 없던 시절 개발로 먼저 개발을 해보면서 스프링을 하나씩 도입해본다.

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
   
  
