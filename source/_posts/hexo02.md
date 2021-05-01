title: Hexo_02 後臺管理
author: Eddie Chang
date: 2021-04-29 01:17:56
tags:
---
### Hexo後臺管理插件
<!--more-->

[hexo-admin Github](https://github.com/jaredly/hexo-admin)

一般情況使用Hexo發布文章需要透過指令再進行更新及部屬

hexo-admin提供Web方式呈現文章編輯與瀏覽，並實時呈現

### 安裝

移動到專案根目錄資料夾下

```
cd <專案根目錄資料夾>
```

輸入安裝npm安裝指令

```
npm install --save hexo-admin
```

### 執行&操作

開啟後臺webserver，預設占用port 4000

```
hexo s
```

開啟瀏覽器進入

```
http://localhost:4000/admin
```

### Hexo插入圖片方式


*不推薦絕對路徑，因為圖片路徑變更時便無法正常顯示*

1. 網路路徑
2. 相對路徑

#### 網路路徑

	![圖片描述](Url)

#### 相對路徑

開啟專案根目錄_config.yml

```
post_asset_folder: true
```

使用指令新增文章時會自動在專案根目錄的source底下創建同名資料夾

也可以直接在專案根目錄的source底下創建資料夾

```
hexo new post "<新文章名稱>"
```

將要放在網頁上的圖片放進資料夾中，網頁中插入圖片

	![圖片敘述](<圖片名稱.副檔名>)