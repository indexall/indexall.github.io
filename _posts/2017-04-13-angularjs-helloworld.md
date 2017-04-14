---
layout: post
title: "AngularJS helloworld"
categories: memo
author: "indexall"
meta: "angularJS helloworld"
---

#### AMP 환경 설치
- OS : windows10
- xampp 를 받아서 설치
[https://www.apachefriends.org/index.html](https://www.apachefriends.org/index.html)

#### angularJS 다운로드
AngularJS 홈페이지 방문하여 zip으로 소스 다운로드
[https://angularjs.org/](https://angularjs.org/)

#### angularJS 설치
설치까지는 아니고, zip으로 받은 angular 소스의 압축을 풀어  
apache web root 에 복사

#### html 파일 생성
```
<!DOCTYPE html>
<html ng-app>
    <head>
        <script src="/angular-1.6.4/angular.js"></script>
    </head>
    <body>
        <input ng-model="text">
        <h1>{{text}}</h1>
    </body>
</html>
```

#### 테스트
localhost로 접속