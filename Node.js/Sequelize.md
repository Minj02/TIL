# Sequelize

### Sequelize?
Node.js 애플리케이션에서 mysql을 쉽게 사용할 수 있도록 도와주는 모듈 💻
<br>

- **Sequelize** 모듈 설치하기  
```npm install --save sequelize```  
```yarn add sequelize ```    
<br>

- **Sequelize** 모듈 초기화하기   
```sequelize init```   


초기화를 진행하면 아래와 같은 폴더 및 파일들이 생긴다.
```
.
|-- README.md      
|-- config
|   `-- config.json
|-- migrations     
|-- models
|   `-- index.js   
|-- package.json  
`-- seeders  
```   

- **config** : 데이터베이스 설정 파일, 사용 이름, DB 이름, 비밀번호 등 정보가 들어있다.
- **migrations** : 데이터베이스의 변경사항을 추적할 수 있게 해준다.
- **models** : 데이터베이스 각 테이블의 정보 및 필드타입을 정의하고 하나의 객체로 모은다.
- **seeders** : 테이블에 기본 데이터를 넣고 싶은 경우 사용한다.


### Sequelize 설정
데이터베이스 관련 설정 파일 ```config.json```   
MySQL을 사용하기로 하고 test 란 이름의 데이터베이스를 생성해보자.

```
mysql -uroot -p # 입력하고 비밀번호 입력 
```
```
create database test;
use test;
```

#### config.json
데이터베이스를 생성하고 선택하기 <br>

``` json
 "development": {
  "username": "아이디",
  "password": "비밀번호",
  "database": test,
  "host": "127.0.0.1",
  "dialect": "mysql",
  "operatorsAliases": false
} 
```

 
