# jwtAuthServer
run npm install
run node server.js

Next test this server from postman:
http://localhost:8083/api/auth/signup  --> User registration
body : {
    "username":"Charu",
    "email":"charu@gmail.com",
    "password":"---", //enter some password here
    "roles":["user","moderator"]
}


http://localhost:8083/api/auth/signin   ----> User login
body : {
    "username":"Charu",
    "password":"---" //enter the same password here
}
This call responds back with JWT token. Copy that token and paste it in Header under key 'x-access-token'

http://localhost:8083/api/test/user  ---> Use JWT token to verify user
