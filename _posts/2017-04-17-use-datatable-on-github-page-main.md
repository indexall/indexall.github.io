---
layout: post
title: "Github page main page를 DataTable로 깔끔하게 정리하기"
categories: memo
author: "indexall"
meta: "github page datatable"
---

github page로 블로그를 바꾸면서 메인페이지를 어떻게 처리할까 고민이 많았다.

하고 싶은 것은
1. 포스트 목록을 한눈에 볼수 있고
2. 이왕이면 검색도 가능하면....

그렇다고 jekyll을 자세히 공부하기에는...   
그래서 일단, datatable을 이용하여 정리해 보았다.


### 준비
필요한 css와 javascript를 다운로드 하여 적당한 위치에 업로드

- 아래 사이트는 datatable example 페이지
[https://datatables.net/examples/basic_init/zero_configuration.html](https://datatables.net/examples/basic_init/zero_configuration.html)

필요한 리소스 
- https://code.jquery.com/jquery-1.12.4.js
- https://cdn.datatables.net/1.10.13/js/jquery.dataTables.min.js
- https://cdn.datatables.net/1.10.13/css/jquery.dataTables.min.css

### 적용
메인 페이지(나의 경우 home.html) 수정   
```
---
layout: default
---

<div class="home">
  <script src="/assets/js/jquery-1.12.4.js"></script>
  <script src="/assets/js/jquery.dataTables.min.js"></script>
  
  <script>

    $(document).ready(function() {
      $('#example').DataTable( {
        "paging":   false,
        "ordering": false,
        "info":     false
      } );
    } );
  </script>

  <h2 class="page-heading">Posts</h2>
  <table id="example" class="display" cellspacing="0" width="100%">
    <thead>
        <tr>
            <th>Title</th>
            <th>date</th>
        </tr>
    </thead>
    <tbody>
      {% for post in site.posts %}
        <tr>
          {% assign date_format = site.minima.date_format | default: "%b %-d, %Y" %}
          <td><a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></td>
          <td>{{ post.date | date: date_format }}</td>
        </tr>
      {% endfor %}
    </tbody>
  </table>
</div>
```

### 결과
생각보다 깔금해서 이대로 계속 써도 될 듯...

![현재 메인페이지](https://dl.dropboxusercontent.com/u/75945505/indexall/2017/04/%EB%B8%94%EB%A1%9C%EA%B7%B8%EB%A9%94%EC%9D%B8.PNG)
