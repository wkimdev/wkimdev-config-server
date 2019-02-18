# wkimdev-config-server 
- spring boot cloude의 eureka로 만든 심플 config server입니다. 
- 아직 수정중인 부분이 있습니다!

# project 구동 순서
- 1. wkimdev-server-config (admin 화면) run
- 2. wkimdev-config-server (API gate way 역할-eureka config server들 등록 기능)
- 3. api-goods-server run (goods들에 대한 서버 구동) 
  * http://localhost:8082/hello 실행시 screen에서 이 문구 확인 가능 ==> Hello from Api Gppds service on 192.168.1.176:8082
- 4. api-order-server run (order들에 대한 서버 구동)   
  * http://localhost:8081/hello 실행시 screen에서 이 문구 확인 가능 ==> Hello from Api Order service on 192.168.1.176:8081
- 5. api-pay-server run (order들에 대한 서버 구동)     
  * http://localhost:8084/hello 실행시 screen에서 이 문구 확인 가능 ==> Hello from Api pay service on 192.168.1.176:8084

  
  


