---
layout: post
title:  "Github 에 블로그 개설하기 ( with jekyll )"
date:   2016-08-27 16:14:00 +0900
categories: github/jekyll
---
* jekyll home page : <http://jekyllrb-ko.github.io>, <https://jekyllrb.com>
* markdown 참고 : <http://blog.kalkin7.com/2014/02/05/wordpress-markdown-quick-reference-for-koreans/>


#### 1. GitHub 에 계정을 만들고 블로그로 사용할 프로젝트를 생성 

* <http://dogfeet.github.io/articles/2012/github-pages.html> 에 잘 설명이 되어 있음
* 자동으로 페이지 만들기' 까지 참고 하였음 


#### 2. 1번에서 만든 블로그 프로젝트를 local 에 clone 


#### 3. local 에서 jekyll 서버를 돌리기 위해서 다음 url 을 참고함

* <http://jekyll-windows.juthilo.com/>
* 위 사이트에서는 ruby 를 설치하고, ruby gem 을 사용해 jekyll 을 설치함
* syntax highlighting 을 위해서 rouge, python, pip, pygments 를 설치함 (옵션인듯)
    

#### 4. 2번에서 clone 한 디렉토리를 이동하여 jekyll 서버를 구동함

* 명령어 
    * <code>jekyll serve -w</code>
* 나의 경우 server 구동시 필요한 library 나 버전이 안맞는 듯한 오류가 발생하여 추가로 bundle 을 설치함
    * <code>require': cannot load such file -- bundler (LoadError)...</code>
    * <code>Could not find gem 'minima x86-mingw32'.... </code>
    * 명령어: 
        * <code>gem install bundler </code>
        * <code>bundler install</code>

 

#### 5. 1번에서 자동으로 생성한 페이지가 마음에 안들어서 jekyll 을 사용해 blog 를 만들어 올리기로 함

* <http://halryang.net/Start-Blogging-With-Jekyll/>
* 명령어
    * <code>jekyll new blog</code>
* 새로 만들어진 source 를 clone 한 곳에 붙여 넣고 jekyll 서버를 구동하여 동작 확인 
    

#### 6. _config.yml 파일 수정

* title, email 등을 수정
* baseurl 을 본인의 github context path 로 맞춰야 함
    * https://example.github.io/blog 일 경우 '/blog'
     

#### 7. 이제 모든 파일을 github 에 push 하고 반영여부 확인
 

#### 8. 로컬에서 작업 후 jekyll 을 통해 확인해야 하는데 _config.yml 의 baseurl 을 수정하기 부담스러우므로 jekyll 서버를 띄울 때 baseurl 을 세팅함

* <code>jekyll serve -w --baseurl ''</code>
    

#### 9. 이제 markdown 문법을 확인하고 post 할 내용을 정리한다.

* 2016-08-26-welcome-to-jekyll.markdown 이라고 포스트할 블로그를 작업했을 경우, 이 파일을 그대로 github 에 push 함
* github 은 jekyll 을 내장하고 있으므로.. 이 markdown 을 해석해서 자동으로 publish 해 줌
* 2016-08-26-welcome-to-jekyll -> 2016/08/26/welcome-jekyll.html 에 파일 생성됨


~~~~
요약: github 에 프로젝트 생성 -> 로컬에 clone -> 로컬에 jekyll 설치 -> 작업 -> github 에 push.
~~~~