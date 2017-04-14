---
layout: post
title: "Jekyll 기반의 GitHub Pages 에서 google analytics 활성화 시키기"
categories: memo
author: "indexall"
meta: "jekyll github pages analytics"
---

### _config.yml 파일에 analytics 코드 추가

google_analytics: UA-XXXXXXXX-X

### build 설정 추가
이것 때문에 한참 해맸음
/script/build 파일에 **JEKYLL_ENV=production** 설정 추가
```
#!/bin/sh

set -e

echo "Building the example site..."
bundle exec JEKYLL_ENV=production jekyll build

```
### 확인
아래 사이트를 참고하여 tracking이 제대로 되는지 확인  
[https://minegi.github.io/2017/01/29/attach-ga-and-disqus/](https://minegi.github.io/2017/01/29/attach-ga-and-disqus/)