# Spring-Security 와 JWT 를 이용한 기능 구현

## 기능설명
### 1. 회원가입 <br/>
설명: 회원가입시, Email 과 password 를 입력하면 해당 사용자에 admin 권한을 부여한다.
- REST API URL : /join <br/>
- Body : { <br/>
   "email" : "kabsung1",<br/>
   "password" : "1q2w3e4r"<br/>
}<br/>
- 기능 결과 : <br/>
![image](https://user-images.githubusercontent.com/54669100/168466237-de3dfbe5-464a-4861-9034-722aa19d054f.png)

### 2. 로그인<br/>
설명: 사용자가 최초 로그인시, JWT값을 Front로 반환한다.
- REST API URL : /login <br/>
- Body : { <br/>
   "email" : "kabsung1",<br/>
   "password" : "1q2w3e4r"<br/>
}<br/>
- 기능 결과 : <br/>  eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJyb2xlcyI6WyJST0xFX0FETUlOIl0sImVtYWlsIjoia2Fic3VuZzEiLCJpYXQiOjE2NTI2MDY3MzYsImV4cCI6MTY1MjYwODUzNn0.Nf0h4-Umwwj38Cxq0HijC1heTHfKgdTICt6T2ZAIBV0 

### 3. 권한이 필요한 페이지 방문 <br/>
설명: 권한이 필요한 페이지를 요청할때 Header JWT 를 넘겨서 권한 여부를 확인 후, <br/>
요청한 페이지를 보여주거나 막는다. <br/>
- REST API URL : /myPage <br/>
- Header : <br/>
![image](https://user-images.githubusercontent.com/54669100/168466708-a9507cae-9d83-43c1-be0a-aeeb61655c77.png)
<br/>
- 기능 결과 : <br/>  
권한 있는 경우: </br>


권한이 없는 경우: <br>
![image](https://user-images.githubusercontent.com/54669100/168466666-e31076b1-f5bc-4112-9aef-3918fd78ad37.png)

