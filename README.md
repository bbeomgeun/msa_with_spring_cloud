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