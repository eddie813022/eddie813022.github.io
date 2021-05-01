title: docker_04 基本指令
author: Eddie Chang
tags: []
categories:
  - Docker
date: 2021-04-30 14:12:00
---
# Docker實際要怎麼使用

*基本實務用途，範例介紹*

<!--more-->

[官方指令文檔](https://docs.docker.com/reference/)

[DockerHub](https://hub.docker.com/)

### Docker 幫助指令

版本訊息

```shell
docker version
```

系統詳細訊息

```
docker info
```

查詢命令

```
docker --help
``` 

### Docker Image指令


查詢所有本地Image

```
docker images
-a # 列出所有Image
-q # 只顯示ID
```
查詢鏡像(與docker hub上相同)

```
docker search python
-f # 過濾器
```
範例: 

```
docker search python -f=STARS=3000 # 只顯示stars超過3000
```

下載鏡像，沒指定tag預設最新版

```
docker pull <name>[:tag]
```
範例:

```
docker pull python:3.9.4-slim
```

強制刪除鏡像

```
docker rmi -f <Image ID>   
or 
docker rmi <name:tag>
```

刪除全部鏡像

```
docker rmi -f $(docker images -aq)
```

### Docker Container指令

*必須先下載Image才能透過Image建立Container*

建立並啟動容器

```
docker run [para] image
para:
--name='' # 容器名稱
-d        # 後臺方式運行
-it       # 交互方式，進入容器中
-p        # 指定容器端口  EX:-p 主機端口:容器端口
-P        # 隨機指定端口
```

範例:

```
docker run -it centos /bin/bash
```

停止並退出容器

```
exit
```

退出但不停止運行容器

```
CTRL + P + Q
```

查詢正在運行的容器

```
docker ps
-a # 包含歷史紀錄運行過的容器
-q # 只顯示ID
```

啟動容器

```
docker start <Container ID>
```

停止容器

```
docker stop <Container ID>
```

進入正在運行的容器

```
docker exec -it <Container ID> /bin/bash
```

重啟容器

```
docker restart <Container ID>
```

刪除容器(需要先停止容器)

```
docker rm <Container ID>
```

刪除全部容器(強制)

```
docke rm -f $(docker ps -aq)
```

### Docker Log指令

查詢日誌

```
docker logs[para] <Container ID>
para:
-t           # 顯示時間軸
-f           # 顯示輸出
--tail <int> # 顯示特定筆數
```

範例:

```
docker logs -tf --tail 5 5f1dc5556d60
```

