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

## 서버 올린후 admin 화면 확인  
- config server에 등록된 서비스 서버 내역들을 확인할 수 있다. 서버 중단.실행 내역도 확인 가능하다.
  
<img width="1423" alt="2019-02-18 9 21 15" src="https://user-images.githubusercontent.com/32521173/52953472-ee8ae080-33ca-11e9-89cd-3aa48050de62.png">  

  
  


