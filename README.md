# spring-security-jwt
Spring Boot + Spring Security + JWT from scratch

Run the application in 2 steps:
Open your postman 
 1- Make this call:
    Method: **POST**
    URL: **http://localhost:8080/authenticate**
    Body:`{
         	"username": "foo",
         	"password": "foo"
         }`
    Then copy the result, example:
        `{
            "jwt": "eyJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJmb28iLCJleHAiOjE1ODU4MDY1OTgsImlhdCI6MTU4NTc3MDU5OH0.mLSMUepbQ0bcagxR2Eyst0Bbw12GHj_fVHOnXrjkebM"
        }`

Then open another tab and run
 2- Method: **GET**
    URL: **http://localhost:8080/hello**
    Be attention: add in your header this parameter:
        Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJmb28iLCJleHAiOjE1ODU4MDY1OTgsImlhdCI6MTU4NTc3MDU5OH0.mLSMUepbQ0bcagxR2Eyst0Bbw12GHj_fVHOnXrjkebM
        
Done!
Your URL will be called as well.