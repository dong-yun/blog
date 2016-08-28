---

layout: post 
title: "Jekyll 페이징 (jekyll-paginate)" 
date: 2016-08-28 16:23:00 +0900
categories: jekyll
tags:
- jekyll
- jekyll-paginate

---

 * [공식 가이드](http://jekyllrb-ko.github.io/docs/pagination/)
 
### 1. jekyll-paginate 설치 ###
 
  * Gemfile 에 jekyll-paginate 한줄 추가
  <pre>
  <code>
   gem "jekyll-paginate"
  </code>
  </pre>
  
  * console 에서 install 후 build
  <pre>
    <code>
     C:\blog>bundle install
     ....
     C:\blog>bundle exec jekyll build
     ....
    </code>
    </pre>
    
### 2. _config.xml 에 코드 추가 ###
  
   <pre>
      <code class="javascript">
       # paging
       gems: [jekyll-paginate]
       
       paginate: 2
       paginate_path: "paging/page:num"
      </code>
    </pre>
    
### 3. index.html 에 코드 추가 ###    

  * 공식 가이드에 있는 코드를 그대로 붙여 넣으면 된다.

### 4. main.scss 에 코드 추가 ###
   
   <pre>
        <code>
         .pagination{
             text-align : center;
           }
           .cusInnerPage{
             border : 1px solid #dddddd;
             padding : 4px 12px;
             margin : -2px;
             text-decoration : none;
             font-style : normal;
           }
           a.cusInnerPage:hover{
             background : #f5f5f5;
           }
           a.cusInnerPage:visited{
             color : #0088cc;
           }
        </code>
      </pre>
      
  