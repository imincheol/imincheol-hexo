---
title: Init hexo setting
date: 2016-07-13 17:14:35
tags:
---

First of all

You already install hexo then modify _config.yml like this

{% codeblock %}

title: imincheol technology blog
subtitle:
description:
author: imincheol
language: en

url: https://imincheol.github.io/

deploy:
  type: git
  repo: https://github.com/imincheol/imincheol.github.io.git

{% endcodeblock %}

그러면 정상적으로 자신의 github로 커밋이 된다

``` bash
$ hexo g -d
```

만약 아래와 같은 메시지가 나타나면
``` bash
ERROR Deployer not found: git
```

다음의 커맨드를 입력한다
``` bash
$ npm install hexo-deployer-git --save
```

그리고 다시 배포한다

``` bash
$ hexo g -d
```

