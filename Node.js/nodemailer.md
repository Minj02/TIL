# Nodemailer

### Nodemailer?
Node.js 애플리케이션에서 메일을 쉽게 보낼 수 있도록 도와주는 모듈 📨
<br><br>

- **nodemailer** 모듈 설치하기 <br>
```npm i nodemailer```<br>
```yarn add nodemailer ```<br><br>


- 이메일을 보낼 **transporter** 객체 생성 <br>
```javascript
let transporter = nodemailer.createTransport(transport[, defaults])
```
<br><br>

- 메일 보내기
```javascript
transporter.sendMail(data[, callback])
```
<br><br>


### mail 구성
```javascript
var message = {
  from: "sender@server.com",
  to: "receiver@sender.com",
  subject: "Message title",
  text: "Plaintext version of the message",
  html: "<p>HTML version of the message</p>"
};
```

<br>
