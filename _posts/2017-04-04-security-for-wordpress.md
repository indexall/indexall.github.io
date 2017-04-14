---
layout: post
title: "워드프레스 설치후 확인해야 할 보안 사항"
categories: memo
author: "indexall"
meta: "wordpress security"
---

자신의 사이트를 만들고, 운영하다 보면 걱정되는 부분 중의 하나가 보안 문제다.   
워드프레스 보안에 대한 자료를 수집하고 정리해 본다.   

### 보안 기초
- ID를 admin으로 사용하지 말것
- 패스워드 조합을 어렵게 사용할 것
- 최신버전 유지

### 워드프레스를 설치하고 수정해 줘야 하는 사항들
#### wp-config.php 파일이 노출되지 않도록 처리
- .htaccess 파일 수정

#### 디렉토리 구조 숨기기
- .htaccess 파일 수정

#### 테마 header.php에 워드프레스 버전 정보가 메타태그로 포함되어 있으면 삭제

### 워드프레스에서 사용되는 보안 플러그인
#### 스팸을 걸러주는 플러그인, Akismet
- [https://wordpress.org/plugins/akismet/](https://wordpress.org/plugins/akismet/)
- 스팸차단을 위해 설치해야 하는 플러그인, 필수

#### DDOS 공격에 사용되는 XML-RPC Pingback
- Disable XML-RPC Pingback 플러그인 설치 필요
> 워드프레스를 이용한 DDOS 공격은 핑백(Pingback : 외부 콘텐츠 링크 시 상대방에게 알림) 기능과 트랙백(Trackback: 외부 사용자가 콘텐츠 링크 시 관리자에게 알림) 기능을 지원하는  XML-RPC 취약점을 이용

#### 로그인 시도 제한 (Limit Login Attempts)
- [https://wordpress.org/plugins/limit-login-attempts/](https://wordpress.org/plugins/limit-login-attempts/)
- 로그인 시도를 제한하여 무작위 패스워드 대입에 대한 방어 효과가 있는 플러그인

#### 로그인 창 접근 제한(Stealth Login Page)
- [https://wordpress.org/plugins/stealth-login-page/](https://wordpress.org/plugins/stealth-login-page/)
- 로그인 접속 주소를 변경하여 해커의 접속을 미리 차단할 수 있는 플러그인

#### 접속 로그 검토(Simple Login Log)
- [https://wordpress.org/plugins/simple-login-log/](https://wordpress.org/plugins/simple-login-log/)
- 접속 로그를 쉽게 검토할 수 있는 플러그인
 
### 관련 사이트
#### 워드프레스 및 워드프레스 플러그인/테마 취약점 확인 사이트
- [https://www.exploit-db.com/](https://www.exploit-db.com/)
- [https://wpvulndb.com/](https://wpvulndb.com/)
- [http://www.cvedetails.com/](http://www.cvedetails.com/)

#### 워드프레스 사이트 필수 보안 Tip of Tip 
- [http://blog.plura.io/?p=4297](http://blog.plura.io/?p=4297)
- 개발자 수준의 보안 팁에 설명되어 있음
 
### 관련 뉴스
#### 워드프레스 플러그인 ‘젯팩’ 보안 결함
- [http://www.ciokorea.com/news/29879](http://www.ciokorea.com/news/29879)
