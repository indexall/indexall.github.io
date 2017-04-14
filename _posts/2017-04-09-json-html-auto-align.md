---
layout: post
title: "JSON, HTML 자동 정렬 시키기"
categories: memo
author: "indexall"
meta: "json html auto align"
---

restful api 작업을 하다보면 관련 툴들을 사용하게 되는데 결과값으로 나온 json을 확인할 때는 괜찮지만
copy&paste할 때 indentation이 깨지는 일들이 종종 있다.
아래와 같이....
```
{“id”:”test”,”email”:”test@test.com”}
```
혹은
```
{
“id”:”test”,
“email”:”test@test.com”
}
```

데이터가 적으면 수작업 하면 되겠지만…. 양이 많을땐 역시 자동이 최고!  
위와 같은 json을 이쁘게 자동 정렬 시켜주는 사이트 링크

#### JSON
[https://jsonformatter.curiousconcept.com/](https://jsonformatter.curiousconcept.com/)
- 파일로도 다운로드 제공

[http://jsbeautifier.org/](http://jsbeautifier.org/)
- 첫번째 사이트 보다 옵션이 많음

#### HTML
[https://tools.arantius.com/tabifier](https://tools.arantius.com/tabifier)
- HTML 자동 정렬 사이트1

[http://prettydiff.com/?m=beautify](http://prettydiff.com/?m=beautify)
- HTML 자동 정렬 사이트2
