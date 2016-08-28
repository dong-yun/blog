---
layout: post
title:  "Facebook Comment 와 Jekyll"
date:   2016-08-27 20:10:00 +0900
categories: github/jekyll
---

 * 참고 사이트 : <https://joshuacox.github.io/jekyll/2015/11/28/facebook-comments-and-jekyll/>

#### 1. facebook development 에 계정 생성 후 app id 취득 ####

  * <https://developer.facebook.com>
  * 앱을 생성하는 과정을 거쳐야 app id 가 생겨남
  * 이때 github 에서 facebook comment 를 사용할 수 있도록 사이트 URL 을 반드시 적어야 함

#### 2. _includes/facebook-init.html, _layouts/post.html 생성 ####

  * root 디렉토리에 _layouts/post.html 이 있을 경우, markdown 파일이 파싱되면서 이 파일을 참조하는 듯 보임
  * 따라서 facebook comment 를 추가하기 위한 코드는 post.html 에 위치하게 됨
  * 코드에 들어가는 스크립트는 facebook development 에서 copy 할 수 있음


#### 참고 사이트 중 다른 부분  ####

  * `include facebook-like.html` 필요없음
  * `meta property` 필요없음
  * `fbcomments` 값은 true / false
  * `fbcomments` 값을 가져오는 코드는 `page.fbcomments` 가 아닌 `site.fbcomments`
