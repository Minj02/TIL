# Nodemailer

### Nodemailer?
Node.js 애플리케이션에서 메일을 쉽게 보낼 수 있도록 도와주는 모듈 📨     
<br> 

- **nodemailer** 모듈 설치하기  
```npm install nodemailer```  
```yarn add nodemailer ```    
<br>

- 이메일을 보낼 **transporter** 객체 생성   
```javascript
let transporter = nodemailer.createTransport(transport[, defaults])
```     
<br>

- 메일 보내기
```javascript
transporter.sendMail(data[, callback])
```     
<br>

### Code
```javascript
const nodemailer = require('nodemailer');

const smtpServerURL = "email SMTP 서버 주소"
const authUser = "email 이메일"
const authPass = "email 계정 비밀번호"
const fromEmail = '보내는 사람 이메일 주소'

function sendEmail(toEmail, title, txt) {    
  let transporter = nodemailer.createTransport({
    host: smtpServerURL,
    secure: true, //보안 서버 사용 false로 적용시 port 옵션 추가 필요
    auth: {
        user: authUser, 
        pass: authPass 
      }
    });
    
    let mailOptions = {
      from: fromEmail, 
      to: toEmail , 
      subject: title, //제목
      text: txt //본문
    };

    //전송 시작
    transporter.sendMail(mailOptions, function(error, info){
      if (error) {
        console.log(error);
      }
      //전송 완료
        console.log("Finish sending email : " + info.response);        
        transporter.close()
    })
}

```


<br>
