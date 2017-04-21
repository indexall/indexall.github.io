---
layout: post
title: "javascript (function())() 이해"
categories: javascript
author: "indexall"
meta: "javascript 즉시실행함수"
---
javascript (function())() 이해

```javascript
(function(){
    // ...
})();
```

## 함수를 만드는 방법
### 함수선언식(function declaration)
스크립트가 로딩되는 시점에 바로 초기화하고 이를 VO(variable object)에 저장, 따라서 함수 선언의 위치와는 상관없이 소스 내 어느 곳에서든지 호출이 가능

```javascript
// 함수선언식(function declaration)
function test() {  
    // ...
}
```

### 함수표현식(function expression)
스크립트 로딩 시점에 VO에 함수를 저장하지 않고 runtime시에 해석되고 실행

자바스크립트에서 함수는 first-class object 이므로 변수에 할당될 수 있기 때문에 아래와 같은 함수 표현식이 가능

> first-class object 의 특징
> - 변수에 저장할 수 있다.
> - 함수의 파라미터로 전달할 수 있다.
> - 함수의 반환값으로 사용할 수 있다.
> - 자료 구조에 저장할 수 있다.


```javascript
// 기명 함수표현식(named function expression) 
var test = function test() {  
    // ...
}; 

// 익명 함수표현식(anonymous function expression)
var test = function() {  
    // ...
};

// 기명 즉시실행함수(named immediately-invoked function expression)
(function test() {
    // ...
}());

// 익명 즉시실행함수(immediately-invoked function expression)
(function() {
    // ...
}());

// 익명 즉시실행함수(immediately-invoked function expression)
(function() {
    // ...
})();
```
