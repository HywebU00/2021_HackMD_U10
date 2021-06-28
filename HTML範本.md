# HTML範本
###### tags: `HyUI`

```htmlembedded=
<!doctype html>
<html lang="zh-Hant" class="no-js">

<head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>HyUI kit</title>
    <!--HTML5 Shim and Respond.js IE8 support of HTML5 elements and media queries [if lt IE 9]>
    <script src="js/html5shiv.js"></script>
    <script src="js/respond.min.js"></script>
    <![endif]-->
    <!-- hyUI css -->
    <link rel="stylesheet" href="css/hyui.css">
    <!-- favicon -->
    <link href="images/favicon.png" rel="icon" type="image/x-icon">
</head>

<body>
    <a href="javascript:;" class="scrollToTop">回頁首</a>
    <!-- JQ -->
    <script src="js/jquery-3.6.0.min.js"></script>
    <!-- 外掛 plugin js -->
    <script src="vendor/jquery.easing.min.js"></script><!-- ease -->
    <!-- hyUI -->
    <script src="js/hyui.js"></script>
    <!-- 客製js -->
    <script src="js/customize.js"></script>
</body>
</head>

```
---
## 設定網頁的語系，讓瀏覽器能更正確解析與編碼

```htmlembedded=
<!doctype html>
<html lang="zh-Hant" class="no-js">
```
HTML 的 <font color="#ff0000">lang</font>  屬性可用於網頁或部分網頁的語言。這對搜索引擎和瀏覽器是有幫助的。 根據W3C 推薦標準，應該通過 <font color="#009ee7"><html></font> 標籤中的 <font color="#009ee7"><lang></font> 屬性對每張頁面中的主要語言進行聲明。相關資料請參考 <font color="#009ee7">W3C Language Codes</font>。



| 常見語系                      | 對應設定       |
|:----------------------------- |:-------------- |
| English                       | lang='en'      |
| 繁體中文Chinese (Traditional) | lang='zh-Hant' |
| 簡體中文Chinese (Simplified)  | Text           |


為了無障礙於關閉Javascript的檢測，請先預留此 <font color="#ff0000">class="no-js"</font> 的設定。更多內容請參考<font color="#009ee7">無障礙單元</font>。

---

## <font color="#009ee7"><head>內容</font>
### <meta>設定
```htmlmixed=
<meta charset="utf-8">
<meta http-equiv="X-UA-Compatible" content="IE=edge">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>HyUI kit</title>
<!--HTML5 Shim and Respond.js IE8 support of HTML5 elements and media queries [if lt IE 9]>
    <script src="js/html5shiv.js"></script>
    <script src="js/respond.min.js"></script>
    <![endif]-->
<!-- hyUI css -->
<link rel="stylesheet" href="css/hyui.css">
<!-- favicon -->
<link href="images/favicon.png" rel="icon" type="image/x-icon">
```
<font color="#009ee7">meta</font> http-equiv="<font color="#EE428B">X-UA-Compatible</font>" content="<font color="#EE428B">IE=edge</font>"> 預設指定IE瀏覽器按照最高的標準模式解析頁面。

<font color="#009ee7">meta</font> name="<font color="#EE428B">viewport</font>" content="<font color="#EE428B">width=device-width, initial-scale=1,shrink-to-fit=no</font>">預設畫面載入初始縮放比例 100%。

<font color="#EE428B">shrink-to-fit=no</font> 這個屬性為iOS 9 能新辨認的屬性：shrink-to-fit 並設定為 no，這設定可以讓網頁的寬度自動適應手機螢幕的寬度。


以下兩種設定都可以防止使用者做畫面縮放，將畫面鎖在縮放比例 100%

```xml
<meta name="viewport" content="width=device-width, initial-scale=1, minimum-scale=1, maximum-scale=1" >
```
```xml
<meta name="viewport" content="width=device-width, initial-scale=1, user-scalable=no">
```
## Internet Explorer 8 部分支援

```htmlmixed=
<!--HTML5 Shim and Respond.js IE8 support of HTML5 elements and media queries [if lt IE 9]>
    <script src="js/html5shiv.js"></script>
    <script src="js/respond.min.js"></script>
    <![endif]-->
```
hyUI預設不支持IE9以下版本，但某些情況下考慮使用者未更新的瀏覽器版本，預設加入給IE8選擇性讀取 <font color="#EE428B">HTML5 tag </font>之 <font color="#EE428B">html5shiv.js</font> 及 <font color="#EE428B">respond.min.js</font>，這2個檔案已經下載於hyUI之js檔案夾裡。


參考資料：<font color="#009ee7">Html5shiv</font>、<font color="#009ee7">respond.js</font>

## 載入CSS

```xml
<link rel="stylesheet" href="css/hyui.css">
```
範本已先預設匯入 <font color="#EE428B">hyui.css</font>

---

## <font color="#009ee7"><body>內容</font>

```xml
<a href="#" class="scrollToTop">回頁首</a>
```
<font color="#009ee7"><body></font> 預設已存在"回頁首"的按鈕，但這只是一個範例。hyUI並無預設任何文本才能執行，只需要針對開發所需，可參考本網站提供之範例自由組合，或是自行開發都是彈性的。

---
## <font color="#009ee7">Javascript 與 jQuery</font>

```htmlmixed=
<!-- JQ -->
<script src="js/jquery-3.6.0.min.js"></script>
<!-- 外掛 plugin js -->
<script src="vendor/jquery.easing.min.js"></script><!-- ease -->
<script src="vendor/slick/slick.min.js "></script><!-- slick -->
<script src="vendor/slick/slick-lightbox.js "></script><!-- slick lightbox -->
<script src="vendor/lazyload/lazyload.js"></script><!-- lazyload -->
<script src="vendor/picturefill/picturefill.min.js" async></script><!-- picturefill -->
<script src="vendor/scrolltable/jquery.scroltable.min.js"></script><!-- scrolltable -->
<!-- hyUI -->
<script src="js/hyui.js"></script>
<!-- 客製js -->
<script src="js/customize.js"></script>
```
 ## 透過jQuery建構所有的互動效果
 
 hyUI內建提供所有的互動模組，皆由jQuery開發而成，jQuery版本為 <font color="#EE428B">jquery-3.6.0</font> 的版本。
 
 ```xml
 <script src="js/jquery-3.6.0.min.js"></script>
 ```
 :::warning
注意 :zap:

由於JQuery 1x版本無法通過黑白箱檢測作業，因此使用最新版本，但有可能會造成匯入外掛無法執行或是部分瀏覽器無法支援，此情況為不可避免之風險，如果沒有限制，可自行改為JQuery1x或2x版本。
:::
 
## 外掛請放入vendor資料夾

範例:

 
 
 ### 匯入lazyload.js
 
 是一款可以將圖片延遲載入網頁的JQuery套件，主要功能可以減少伺服器多餘的流量輸出/減輕伺服器負擔及提高使用者體驗。它會依照用戶在滾動頁面時當用戶快要滾動到圖片時才開始跟伺服器請求這張圖片下來，然後即時顯示給用戶觀看。
 ```xml
 <script src="vendor/lazyload/lazyload.js"></script>
 ```
 
 ### 匯入picturefill.min.js
 
 它則是透過html5的picture的標籤，來實現在不同的裝置的解析，載入相對應的圖檔大小，如此一來在3G吃不飽，4G又不穩的情況下，對於使用者來說真是一大福音，而目前這個方法是用JS來進行切換，因此在製作圖檔時，就多存幾個檔案即可解決。
```xml
 <script src="vendor/picturefill/picturefill.min.js" async></script>
 ```
 
## 匯入hyui.js
預設提供常用之互動模組，例如：lightbox、menu等效果，例如：無障礙檢測 <font color="#EE428B">tab</font> 鍵盤操作瀏覽網頁之設定。如果沒有特殊的版本更新需求，請不任意新增或刪除 <font color="#EE428B">hyui.js</font> 的預設設定。

```xml
<script src="js/hyui.js"></script>
```

## 自行撰寫之Javascript效果

可自行撰寫所需要的互動程式，可寫在 <font color="#EE428B">customize.js</font>


當禁用JavaScript時，請視情況於網頁顯示 <font color="#009ee7"><noscript></font>，並標記上相關說明文字。
```xml
<script src="js/customize.js"></script>
```


<style>
.ui-infobar{
max-width:95%;
}
.markdown-body{
max-width:95%;
}
</style>









