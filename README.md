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
