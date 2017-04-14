---
layout: post
title: "nodejs에서 fs.readFileSync 사용시 발생하는 에러 확인"
categories: memo
author: "indexall"
meta: "nodejs readFileSync"
---

### 증상

nodejs 에서 fs.readFileSync 를 사용하는데 계속 에러가 발생  

```
  var fileContents;
  try {
    fileContents = fs.readFileSync('security/key.pem');
  } catch (err) {
    console.log('err=', err);
  }
```

### 분석
결국 try catch 로 확인해보니 파일을 찾지 못한다는 에러
```
err= { Error: ENOENT: no such file or directory, open './index.js'
    at Error (native)
    at Object.fs.openSync (fs.js:640:18)
    at Object.fs.readFileSync (fs.js:508:33)
    at /root/api-server/routes/search.js:621:23
    at Layer.handle [as handle_request] (/root/api-server/node_modules/express/lib/router/layer.js:95:5)
    at next (/root/api-server/node_modules/express/lib/router/route.js:131:13)
    at Route.dispatch (/root/api-server/node_modules/express/lib/router/route.js:112:3)
    at Layer.handle [as handle_request] (/root/api-server/node_modules/express/lib/router/layer.js:95:5)
    at /root/api-server/node_modules/express/lib/router/index.js:277:22
    at Function.process_params (/root/api-server/node_modules/express/lib/router/index.js:330:12) errno: -2, code: 'ENOE
NT', syscall: 'open', path: './index.js' }
```

### 원인
require 할 때는 현재 소스에서 상대경로로 찾지만
```
var index = require('./routes/index');
```

fs.readFileSync 에서는 절대경로로 사용해야 하는 것을 보임
```
fileContents = fs.readFileSync('security/key.pem');
```
> 시간이 없어 정확한 테스트는 하지 못하여 100% 장담 못함

