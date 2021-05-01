title: Docker_01 基礎概念
author: Eddie Chang
tags: []
categories:
  - Docker
date: 2021-04-28 17:07:00
---
# Docker，最熱門的容器技術

*Docker核心技術與優點*

<!--more-->

### Docker概念

[Docker官方文檔](https://docs.docker.com/)

Docker架構圖

![](pasted-4.png)

傳統虛擬機內部

![](virtualmachine.png)

Docker內部

![](container.png)

Docker 是一項解決環境的容器技術，基於Go語言開發

相比傳統虛擬化技術以作業系統為中心，Docker則是以應用程式為中心的虛擬化技術，

透過直接在内核系統層打造虛擬執行環境共用同一個Host OS，取代了個別建置OS的作法

為了與傳統虛擬機區隔開來，我們稱之為`Container`。

Docker使用aufs檔案系統設計層層堆疊的Container Image，

將Container內的所有程式(應用程式、函式庫、設定檔)都包進Image中，

並透過`Docker File`來記錄建立Contrainer的步驟與參數，

後續需要建立Container時只要透過Docker File就能在任意支援Docker的環境中部屬。

充分解決了"我的電腦可以運作，為甚麼你的不行?"這種問題的發生

### Docker優點

Docker也是一種內核虛擬化技術

- 容器之間互相隔離
- 占用容量更小
- 開源技術
- 文檔齊全
- 啟動速度更快
- 開發及運維一條路

### Docker元件

- 鏡像(Image)
- 容器(Container)
- 倉庫(Repository)

`鏡像(Image)`

就像是Python中的類或是模板，提供容器運行單個或多個服務

`容器(Containter)`

容器之間互相隔離，基本上就像是在對虛擬機開關機一樣，容器也能做到開啟與關閉

`倉庫(Repository)`

存放鏡像的地方:Dockerhub，一樣有分成Public與Private，
基於git的命令，一樣可以提供使用者上傳及下載

### Docker安裝

- Windows [->Download](https://docs.docker.com/get-docker/)
- MacOs [->Download](https://docs.docker.com/get-docker/)
- Linux [->Download](https://docs.docker.com/get-docker/)