---
layout: post
title: "spring helloworld for restful api"
categories: memo
author: "indexall"
meta: "spring helloworld restful api"
---

### 설치
#### JDK
자기 시스템환경에 맞는 JDK 설치
[http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)

- 환경변수에 JAVA_HOME 추가
  JAVA_HOME : c:\Program Files\Java\jdk1.8.0_121

- path에 %JAVA_HOME%\bin 추가

#### Spring Tool Suite
Spring tool 다운로드
[http://spring.io/tools](http://spring.io/tools)

spring-tool-suite-3.8.3.RELEASE-e4.6.2-win32.zip 압축을 적당한 경로에 푼다

sts-bundle\sts-3.8.3.RELEASE\sts.exe 실행

### Helloworld
#### 프로젝트 생성
1. package explorer 위에서 우클릭하여 New > Spring starter Project 클릭
2. 프로젝트 정보 입력(본 포스트  소스를 그대로 사용하려면 Demo로 입력된 부분을 hello로 변경)
3. New Spring Starter Project Dependencies 에서 Web > Web 체크
4. Finish


#### resource representation class 생성
Greeting.java
```
package hello;

public class Greeting {
    private final long id;
    private final String content;
    public Greeting(long id, String content) {
        this.id = id;
        this.content = content;
    }
    public long getId() {
        return id;
    }
    public String getContent() {
        return content;
    }
}

```
#### resource controller 생성

GreetingController.java
```
package hello;

import java.util.concurrent.atomic.AtomicLong;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.bind.annotation.RestController;
@RestController
public class GreetingController {
    private static final String template = "Hello, %s!";
    private final AtomicLong counter = new AtomicLong();
    @RequestMapping("/greeting")
    public Greeting greeting(@RequestParam(value="name", required=false, defaultValue="World") String name) {
        return new Greeting(counter.incrementAndGet(),
                            String.format(template, name));
    }
}

```

### 테스트
1. 프로젝트에서 오른쪽 마우스 버튼 클릭
2. Run As > Spring Boot App 실행
3. 서버가 띄워지면 [http://localhost:8080/greeting](http://localhost:8080/greeting) 에 접속하여 확인


## 참고 사이트
https://spring.io/guides/gs/rest-service/

