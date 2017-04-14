---
layout: post
title: "AWS에 워드프레스 설치하기"
categories: memo
author: "indexall"
meta: "wordpress aws"
---
AWS(Amazon Web Service) 최초 가입자는 1년간 무료 티어를 이용할 수 있 수 있다.   
이 무료 티어에 워드프레스는 설치하는 방법을 정리해 본다.   
참고로 AWS 공식 문서가 한글화가 어느정도 진행되어 있어 시작하기 전에 한 번쯤 읽고 시작하면 많은 도움이 된다.   
   
참고로 무료 티어이지만 많은 사용자들이 과금을 경험하는 것 같다.   
이미 나도 과금(0.07 달러)을 경험한 상태이다.   
그러므로 과금체계를 완전 숙지하기 전까지는 꼭 예상 과금을 지속적으로 확인하여 요금 폭탄을 예방하시기 바란다.   
   
> $0.01 per GB - regional data transfer - in/out/between EC2 AZs or using elastic IPs or ELB 항목에서 과금이 올라간다면 각 인스턴스의 Availability zone 이 다른 곳으로 설정되어 있는지 확인을 해봐야 합니다.

#### Amazon web service 공식 홈페이지
- [http://aws.amazon.com/](http://aws.amazon.com/)

#### 아마존 웹서비스에 워드프레스 설치하기
- [http://selfwordpress.net/아마존-웹서비스에-워드프레스-설치하기/](http://www.selfwordpress.net/%EC%95%84%EB%A7%88%EC%A1%B4-%EC%9B%B9%EC%84%9C%EB%B9%84%EC%8A%A4%EC%97%90-%EC%9B%8C%EB%93%9C%ED%94%84%EB%A0%88%EC%8A%A4-%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/)
- 아마존 웹서비스에 워드프레스를 설치하고 인스턴스가 중지되면 다른 인스턴스가 자동으로 실행되는데 이때 최초에 올린 zip 파일이 다시 설치됨, 따라서 플러그인 설치나 워드프레스 업데이트를 하였다면 소스를 다운 받아 압축하여 다시 올려야 함

#### putty를 이용하여 인스턴스 접속하기
- [http://docs.aws.amazon.com/ko_kr/AWSEC2/latest/UserGuide/putty.html](http://docs.aws.amazon.com/ko_kr/AWSEC2/latest/UserGuide/putty.html)
- AWS 공식 사이트로 EC2 인스턴스를 생성한 후 putty를 이용하여 접속하는 방법이 설명되어 있음

#### 프리티어사용시 요금발생(폭탄)을 막기위한 팁
- [http://gun0912.tistory.com/45](http://gun0912.tistory.com/45)
- 프리티어 사용시 비용이 나오는 항목에 대해 자세한 설명

#### 과금폭탄의 실 예
- [http://sanghaklee.tistory.com/32 (말도 안 되는 과금의 추억. 요금 폭탄)](http://sanghaklee.tistory.com/32)
- 글쓴이의 요금폭탄 경험을 생생하게 전달하여 관련 자료를 열심히 찾아보게 만드는 곳

#### Amazon Web Service 한국 사용자 모임
- [https://m.facebook.com/groups/189675924467773](https://m.facebook.com/groups/189675924467773)
- "2012년 부터 시작된 사용자 그룹"이라는 소개가 있음
- 현재도 활발히 운영중이며 참고할 만한 내용이 많은 곳

#### 워드프레스 멀티 사이트 구축 관련 자료
- [http://igotit.tistory.com/88](http://igotit.tistory.com/88)
- 개념부터 상세하게 설명되어 있음
- 작업의 순서상 필요한 부분에 대해서는 링크를 통해 차례대로 접근 가능하도록 해 놓음