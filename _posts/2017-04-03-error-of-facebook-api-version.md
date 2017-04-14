---
layout: post
title: "Facebook API 버전에 따른 로그인 오류"
categories: memo
author: "indexall"
meta: "Facebook API version error"
---
어느날 갑작이 이전 프로젝트에서 구현해 놓은 페이스북 소셜 로그인이 동작하지 않는다.   
아무리 찾아봐도 소스상에 오류는 없다.   
어쩔 수 없이 다시 처음부터 페이스북 문서를 보다 보니 API 버전 문제!   
갑자기 페이스북 소셜 로그인이 동작하지 않는다면 API 버전을 체크해 보자.   

- 페이스북 API V2.1 은 2016년 10월 30일까지 사용 가능
- 페이스북 API V2.6 은 2018년 4월 까지 사용 가능

### 참고 사이트들
#### Facebook 공식 doc 사이트
- [https://developers.facebook.com/docs/apps/changelog](https://developers.facebook.com/docs/apps/changelog)
- 플랫품 변경 사항이 정리되어 있는 페이스북 공식 사이트

#### 페이스북 API 2.1 변경사항이 정리되어 있는 사이트
- [http://blog.parkheesung.com/2014/08/api-21.htm](http://blog.parkheesung.com/2014/08/api-21.htm)
- 한글 블로그

#### 페이스북 Graph API Explorer 사이트
- [https://developers.facebook.com/tools/explorer/](https://developers.facebook.com/tools/explorer/)
- 페이스북 Developer 계정 필요
- 페이스북의 사용자 정보 API(Graph API) 사용시 필요한 기능 정보를 선 검색/테스트 가능

#### 페이스북 Graph API Reference 사이트
- [https://developers.facebook.com/docs/graph-api/reference](https://developers.facebook.com/docs/graph-api/reference)
- 페이스북 Developer 계정 필요
