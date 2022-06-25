# msa_with_spring_cloud

demo project with msa with springCloud
- springboot : 2.4.2
- java : 11
- spring-cloud : 2020.0.0
- build : maven

---

## discovery-service
- port : 8761
- netflix-eureka-server
- http://127.0.0.1:8761 : registered service를 볼 수 있는 console

## user-service
- port : 9001
- netflix-eureka-client

## netflix-zuul 테스트
- first-service : 8081
- second-service : 8082
- zuul-service : 8080
  - 2.3.10.RELEASE (2.4 미만 버전에서 zuul 사용 가능)
- 이후 zuul-service 포트로 호출 시 각 서비스로 라우팅

### zuul logging filter
- zuulFilter를 상속 받아서 구현
- 서비스로 들어오는 요청에 대한 로깅 작업을 할 수 있음

## Spring Cloud Gateway
- Spring에서 자체적으로 Gateway를 만들어서 zuul 서비스를 대체
- zuul과 달리 **비동기 처리**가 가능해진다는 점