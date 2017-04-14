---
layout: post
title: "AngularJS helloworld 2nd"
categories: memo
author: "indexall"
meta: "angularJS helloworld"
---

#### controller를 사용하여 helloworld html 파일 생성
```
<!DOCTYPE html>
<html ng-app="myApp">
<head>
    <script src="/angular-1.6.4/angular.js"></script>
    <script>
        var myApp = angular.module('myApp', []);
        myApp.controller('MainCtrl', ['$scope', function ($scope) {
            $scope.text = 'Hello world';
        }]);
    </script>
</head>
<body>
    <div ng-controller="MainCtrl">
         {{ text }}
    </div>
</body>
</html>
```