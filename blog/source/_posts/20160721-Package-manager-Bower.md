---
title: 패키지 매니저 Bower
date: 2016-07-21 15:27:47
tags:
---

Package manager Bower

## 패키지 매니저
- Like. Npm, maven, gem
- 라이브러리를 간편하게 관리, 설치해줄 수 있다. ( jQuery, Bootstrap, … )
- https://bower.io/

## 설치
- `$ npm install bower --save`

## 사용법
- 시작하기
    - bower.json 파일을 만든다.
    - `$ bower init `
- 라이브러리 설치
    - Bower를 사용하여 jQeury를 설치한다.
    -  bower_components > jquery 에 설치된다.
    - `$ bower install jquery --save`
-  bower-installer 설치
    -  bower_components에 있으면 사용하기가 어렵다. 따라서 해당 파일들을 사용하기 쉽게 설치(복사)해주는 installer를 설치하자.
    - `$ npm install -g bower-installer`
    -  bower.json 수정
{% codeblock lang:JSON %}
"install" : {
  "path" : {
    "css" : "static/css",
    "js" : "static/js"
  }
}
{% endcodeblock %}
    -  bower로 설치한 라이브러리 중 css 파일과 js파일을 옮겨준다.
    - `$ bower-installer`
    - https://github.com/blittle/bower-installer

## 설명
- 사용가능한 라이브러리 종류
    - Github
        - Shorthand
            - [사용자명]/[패키지명] 으로 바로 설치 가능
            - `$ bower install user/package`
        - Endpoint
            - Github .git
            - `$ bower install git://github.com/user/package.git`
    - URL
        - Java script
            - .js
            - `$ bower install http://example.com/script.js`

