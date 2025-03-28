# Docker-to-k8s-springboot

![image](https://github.com/user-attachments/assets/9ff1df59-b75f-42d2-bb0a-cf66c84a2864)
![image](https://github.com/user-attachments/assets/9d04d9a3-78b5-4156-a24b-de076f800e45)

![image](https://github.com/user-attachments/assets/6dc49089-c146-4eef-80e4-02353d0ae854)

![image](https://github.com/user-attachments/assets/5c42cf2e-0fc0-44c1-9e3a-5fc9c2f1e99c)

![image](https://github.com/user-attachments/assets/b16e88ff-732d-48cf-bdb4-f5babc899c04)

![image](https://github.com/user-attachments/assets/ed5bb98f-ab42-4b65-8202-3b51b695b5db)

![image](https://github.com/user-attachments/assets/73ec4e0e-b287-4cff-919d-8851a8186ef6)

![image](https://github.com/user-attachments/assets/32d7d0a2-c35f-4caa-bc8a-0fe3ce2aae47)

```
docker start
```
![image](https://github.com/user-attachments/assets/e9aae388-317b-4393-a7fa-e60bb010a7ed)
![image](https://github.com/user-attachments/assets/9f1467ee-2e4a-447d-9523-e38e3d09f3f4)


![image](https://github.com/user-attachments/assets/8889a5c3-a775-45bc-858f-d6c3bd1d7c4d)
![image](https://github.com/user-attachments/assets/fef33bc4-2cca-4ff4-ba8d-8a500fc5fda2)



## 실습단계

### 1. Spring Boot APP -> JAR 변환
  <br>
  
  
  Spring Boot App [Run Configurations] -> [Gradle Task] -> [New_configuration]
  -> APP 선택 -> [Working Directory] -> [Run] -> JAR 파일 확인하기 [프로젝트dir/build/lib]
  

  <br>

  ```
  주의사항
      application.properties 파일의 server.port=8099 포트 확인하기
      -> 
  ```
  
  <img src="https://github.com/user-attachments/assets/1935104f-3002-46b8-9582-26ef72a9db17" width="600"/>
   
  <img src="https://github.com/user-attachments/assets/2c984fd6-9817-4c93-b827-40521dfaf8e9" width="400"/>
  <img src="https://github.com/user-attachments/assets/dc266e24-d497-4a2a-9cf4-7c35c6812101" width="400"/>

### 2. JAR -> Docker로 이미지화
   docker build -t littledocker377/springboot-app:latest .
   dockerfile 작성
   <img src="https://github.com/user-attachments/assets/80106be2-47e0-4374-82b2-ca2ec4c2a6aa" width="600"/>
  
### 3. k8s (minikube)로 파드 2개 생성
   type : loadbalancer, nodeport
### 4. curl, 브라우저 확인하기
