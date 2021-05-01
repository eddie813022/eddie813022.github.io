title: Docker_03 Linux環境安裝&設定
author: Eddie Chang
tags: []
categories:
  - Docker
date: 2021-04-30 11:55:00
---
# Linux如何安裝Docker

*linux安裝到啟動測試*

<!--more-->

[官方文檔](https://docs.docker.com/engine/install/centos/)

### 下載Yum-config軟件包

```shell
sudo yum install -y yum-utils
```

### 添加Docker Repository

```
sudo yum-config-manager \
--add-repo \
https://download.docker.com/linux/centos/docker-ce.repo
```

### 安裝最新版Docker Engine(ce)

```
sudo yum install docker-ce docker-ce-cli containerd.io
```

*如果安裝時遇到問題，請先移除容器套件*

```
yum remove runc
```

### 啟動Docker Service

```
sudo systemctl start docker
```

### 測試Docker HelloWorld

```
docker run hello-world
```

出現Hello from Docker!代表安裝成功，已可正常使用docker