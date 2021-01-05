---
layout: post
title:  "Dockerのチートシート"
date:   2021-01-02 12:39:36 +0900
categories: docker-cheatsheet
permalink: /docker-cheatsheet
excerpt_separator: <!--more-->
---
![image here](/assets/img/thumbnail/ten.jpeg)
<!-- <div style="text-align: center;">
<img src="/assets/img/thumbnail/ten.jpeg" width="550px" height="400px">
</div> -->
<!--more-->
 

<br><br>

## コンテナ、イメージの削除コマンド


```bash:bash
$ docker stop $(docker ps -q)
$ docker rm $(docker ps -aq)
$ docker rmi $(docker images -q)
```


