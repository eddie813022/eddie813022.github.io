title: Hexo_01 安裝&配置
tags: []
categories:
  - Hexo
author: eddie chang
date: 2021-04-28 11:34:00
---
# Hexo+Next+Github=個人靜態網站

*安裝與基本配置*
<!--more-->

[Hexo官方文檔](https://hexo.io/zh-cn/docs/#%E4%BB%80%E4%B9%88%E6%98%AF-Hexo%EF%BC%9F)

Hexo : 快速、簡潔打造靜態網站，並使用Markdown語法編輯文章

Next : Hexo支援的熱門主題之一

Github : 提供靜態網站運作的服務商(存放及運作你的網站)

### Hexo安裝條件:

1.  Node.Js 10.13up(建議12以上)  [->Node Download](https://nodejs.org/en/download/)
2. Git  [->Git Download](https://git-scm.com/downloads)


### Hexo安裝方式:

1.使用npm安裝Hexo-cli

```
npm install -g hexo-cli
```

2.開啟Command-Line Interface移動到想安裝的資料夾位置上

```
cd <想要安裝初始hexo的資料夾位置>
```

3.初始化hexo資料夾

```
hexo init
```

### Hexo連結github

1.先將github上的repository複製到本地hexo資料夾內(如果沒指定目錄就是在當前資料夾)

```
https://github.com/<username>/<repository_name.git> <指定的本地資料夾>
```

### 下載Hexo主題(Next)

[新版Next Github
](https://github.com/theme-next/hexo-theme-next)

1.開啟cli將位置移動到hexo資料夾中

```
cd <本機hexo資料夾>
```

2.從hithub上下載next主題

```
git clone https://github.com/theme-next/hexo-theme-next.git themes/next
```

### Hexo基本配置




### 參考資料：