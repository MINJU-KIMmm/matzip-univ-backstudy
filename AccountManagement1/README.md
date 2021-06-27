# <비밀번호 찾기> 기능을 위한 스터디

## 참고
-스프링부트로 이메일보내기(비밀번호 찾기 / 회원가입 이메일 인증)
https://1-7171771.tistory.com/85

-[Spring] 비밀번호 암호화 SHA-256 / MD5
https://1-7171771.tistory.com/82

## 임시비밀번호 이메일로 전송
1. 보안수준이 낮은 앱 액세스 허용
2. gradle 의존성 추가
<pre>
<code>
implementation 'org.springframework.boot:spring-boot-starter-mail
</code>
</pre>
3. application.yml에 내용 추가
<pre>
<code>
spring:
     mail:
    	host: smtp.gmail.com
    	port: 587
   	 	username: 본인의 구글 계정 @gmail.com
    	password: 본인의 구글 계정 비밀번호
    	properties:
      	mail.smtp.auth: true
      	mail.smtp.starttls.enable: true
</pre>
</code>

## 비밀번호 암호화
회원가입을 구현할 때 회원의 password를 암호화해줌
SHA-256 알고리즘이 MD5 알고리즘보다 더 강력함


