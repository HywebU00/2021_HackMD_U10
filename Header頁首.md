# Header頁首

###### tags: `HyUI`

檔案名稱：sass/modual/_header.scss
檔案名稱：sass/modual/_menu.scss

<font color="#EE428B">頁首</font> 由 <font color="#EE428B">header</font> 標籤包覆，目前已預先設定 <font color="#EE428B">h1 (logo圖檔)</font> 、 <font color="#EE428B">navigation</font> 、 <font color="#EE428B">search</font> 、 <font color="#EE428B">menu</font>等元素。

內含預設模組可參考
* <font color="#009ee7">Navigation 導覽列</font>
* <font color="#009ee7">Search 搜尋</font>
* <font color="#009ee7">Menu 主選單</font>

以下模組依照無障礙 <font color="#EE428B">tab</font> 遊走順序擺放，如無特殊需求，皆依照由上到下、由左到右之順序呈現。

頁首模組皆已設定響應式風格樣式，目前斷點預設為 <font color="#EE428B">768px</font> ，如需要更改斷點，請至 <font color="#EE428B">hyui.js</font>更改斷點變數，以及 <font color="#EE428B">_valuable.scss</font> 更改斷點變數。

## HTML範本
```htmlmixed=
<!-- header Start -->
<header class="header">
    <div class="container">
        <a class="accesskey" href="#aU" id="aU" accesskey="U" title="網站標題" tabindex="2">:::&l>
        <!-- navigation Start -->
        <nav class="navigation">
            <!-- 一組ul預設靠右 -->
            <!-- 兩組ul已寫JQ靠左靠右 -->
            <ul>
                <li><a href="#">回首頁</a></li>
                <li><a href="#">網站導覽</a></li>
                <li><a href="#">English</a></li>
                <li><a href="#">常見問答</a></li>
            </ul>
            <ul>
                <li><a href="#">第二組導覽</a></li>
                <li><a href="#">第二組導覽</a></li>
                <li><a href="#">第二組導覽</a></li>
            </ul>
            <div class="language">
                <a href="#">語言選擇</a>
                <ul>
                    <li><a href="#">繁體中文</a></li>
                    <li><a href="#">简体中文</a></li>
                    <li><a href="#">ENGLISH</a></li>
                </ul>
            </div>
        </nav>
        <!-- navigation End -->
        <h1>
            <a href="#"><img src="images/logo.png" alt="網站標題"/></a>
        </h1>
        <!-- Search Start -->
        <div class="search">
            <form action="" class="form_inline">
                <div class="form_grp">
                    <label for="mustSameAsId">帳號:</label>
                        <input name="username" id="mustSameAsId" type="text" placeholder="請輸入文字" accesskey="S">
                    <input name="" type="submit" value="查詢" />
                </div>
                <div class="btn_grp">
                    <input name="" type="submit" value="進階搜尋" />
                </div>
            </form>
            <div class="keywordHot">
                <ul>
                    <li><a href="#">熱門熱門</a></li>
                    <li><a href="#">查詢</a></li>
                    <li><a href="#">字詞三</a></li>
                </ul>
            </div>
        </div>
        <!-- Search End -->
        <!-- noscript -->
                <noscript> 您的瀏覽器不支援JavaScript語法，JavaScript語法並不影響內容的陳述。您可使用按鍵盤上的Ctrl鍵+ (+)鍵放大/(-)鍵縮小來改變字型大小；回到上一頁可使用瀏覽器提供的 Alt+左方向鍵(←) 快速鍵功能；列印可使用瀏覽器提供的(Ctrl+P)功能。您的瀏覽器，不支援script語法，若您的瀏覽器無法支援請點選此超連結 <a href="#">網站導gt;
        </noscript>
        <!-- menu Start -->
        <nav class="menu">
            <ul>
                <li><a href="#">第一層選單</a>
                    <ul>
                        <li><a href="#">第二層選單</a></li>
                        <li><a href="#">第二層選單</a></li>
                        <li><a href="#">第二層選單</a></li>
                        <li><a href="#">第二層選單</a></li>
                    </ul>
                </li>
                <li><a href="http://www.google.com">第一層有連結</a></li>
                <li><a href="http://www.google.com">第一層有連結</a>
                    <ul>
                        <li><a href="http://www.google.com">第二層有連結</a></li>
                        <li><a href="#">第二層選單</a></li>
                        <li><a href="#">第二層選單</a></li>
                        <li><a href="#">第二層選單</a></li>
                        <li><a href="#">第二層選單</a></li>
                        <li><a href="#">第二層選單</a></li>
                        <li><a href="#">第二層選單</a></li>
                        <li><a href="#">第二層選單</a></li>
                    </ul>
                </li>
                <li><a href="#">第一層選單</a>
                    <ul>
                        <li><a href="#">第二層選單</a></li>
                        <li><a href="#">第二層選單</a></li>
                        <li><a href="http://www.google.com">第二層有連結</a>
                            <ul>
                                <li><a href="http://www.google.com">第三層選單有下層</a>
                                    <ul>
                                        <li><a href="#">第四層選單</a></li>
                                        <li><a href="#">第四層選單</a></li>
                                    </ul>
                                </li>
                                        <li><a href="http://www.google.com">第三層選單有連結</a&li>
                                <li><a href="#">第三層選單</a></li>
                            </ul>
                        </li>
                        <li><a href="#">第二層選單</a></li>
                    </ul>
                </li>
                <li><a href="#">第一層選單</a>
                    <ul>
                        <li><a href="#">第二層選單</a></li>
                        <li><a href="#">第二層選單</a></li>
                        <li><a href="#">第二層選單</a></li>
                        <li><a href="#">第二層選單</a></li>
                    </ul>
                </li>
                <li><a href="#">第一層選單</a>
                    <ul>
                        <li><a href="#">第二層選單</a></li>
                        <li><a href="#">第二層選單</a></li>
                        <li><a href="#">第二層選單</a></li>
                        <li><a href="#">第二層選單</a></li>
                    </ul>
                </li>
            </ul>
        </nav>
        <!-- menu End -->
    </div>
</header>
<!-- header End -->
```



<style>
.ui-infobar{
max-width:95%;
}
.markdown-body{
max-width:95%;
}
</style>
