# wkimdev-config-server 
- spring boot cloude의 eureka로 만든 심플 config server입니다. 
- 아직 수정중인 부분이 있습니다!

# Eureka
  
## service discovery
- MSA와 같은 분산 환경은 서비스 간의 원격 호출로 구성이 된다. 원격 서비스 호출은 IP 주소와 포트를 이용하는 방식이 된다. 
- 서비스 클라이언트가 서비스를 호출할때 서비스의 위치 (즉 IP주소와 포트)를 알아낼 수 있는 기능이 필요한데, 이것을 바로 서비스 디스커버리 (Service discovery)라고 한다.
- Service A의 인스턴스들이 생성이 될때, Service A에 대한 주소를 Service registry (서비스 등록 서버) 에 등록해놓는다. Service A를 호출하고자 하는 클라이언트는 Service registry에 Service A의 주소를 물어보고 등록된 주소를 받아서 그 주소로 서비스를 호출  
- **Service discovery에 전문화된 솔루션**으로는 Netflix의 Eureka나 Hashcorp의 Consul과 같은 서비스가 있다. 
- 동적 서비스 등록, 발견 : 서버 개수 동적 조절 
- 장애가 발생시 서비스 레지스트리에서 제외 
- MSA 




# project 구동 순서
- 1. wkimdev-server-config (admin 화면) run
- 2. wkimdev-config-server (API gate way 역할-eureka config server들 등록 기능)
- 3. api-goods-server run (goods들에 대한 서버 구동) 
  * http://localhost:8082/hello 실행시 screen에서 이 문구 확인 가능 ==> Hello from Api Gppds service on 192.168.1.176:8082
- 4. api-order-server run (order들에 대한 서버 구동)   
  * http://localhost:8081/hello 실행시 screen에서 이 문구 확인 가능 ==> Hello from Api Order service on 192.168.1.176:8081
- 5. api-pay-server run (order들에 대한 서버 구동)     
  * http://localhost:8084/hello 실행시 screen에서 이 문구 확인 가능 ==> Hello from Api pay service on 192.168.1.176:8084

## 서버 올린후 admin 화면 확인  
- config server에 등록된 서비스 서버 내역들을 확인할 수 있다. 서버 중단.실행 내역도 확인 가능하다.
  
<img width="1423" alt="2019-02-18 9 21 15" src="https://user-images.githubusercontent.com/32521173/52953472-ee8ae080-33ca-11e9-89cd-3aa48050de62.png">  

  
  
## reference
- https://bcho.tistory.com/tag/Eureka



