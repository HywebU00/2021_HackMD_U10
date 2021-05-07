# Menu 主選單

###### tags: `HyUI`

檔案名稱：sass/modual/_menu.scss
檔案名稱：sass/modual/_megamenu.scss

主選單標籤為<font color="#EE428B">nav.menu</font>及<font color="#EE428B">nav.megamenu</font>([範例](https://hywebu00.github.io/hyui_flex/lp_template.htm))目前預設為最多 <font color="#EE428B">4</font> 層，在使用上請注意，如有多層選單會造成瀏覽器右方空間不足，這部分請自行客製設定。

主選單在手機版預設放置於畫面左方<font color="#EE428B">sidebar</font>，手機版會自動產生選單按鈕，用於打開收合左側選單。

## Menu HTML範本
```htmlmixed=
<!-- menu Start -->
<nav class="menu" role="navigation" aria-label="About page">
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
                        <li><a href="http://www.google.com">第三層選單有連結</a></li>
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
```
## Megamenu HTML範本
```htmlmixed=
<!-- megamenu Start -->
<nav class="megamenu" role="navigation" aria-label="About page">
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
                <li><a href="#">第二層選單</a>
                    <ul>
                        <li><a href="http://www.google.com">第三層選單有下層</a></li>
                        <li><a href="http://www.google.com">第三層選單有連結</a></li>
                        <li><a href="#">第三層選單</a></li>
                        <li><a href="#">第三層選單</a></li>
                        <li><a href="#">第三層選單</a></li>
                    </ul>
                </li>
                <li><a href="#">第二層選單</a>
                    <ul>
                        <li><a href="http://www.google.com">第三層選單有下層</a></li>
                        <li><a href="http://www.google.com">第三層選單有連結</a></li>
                        <li><a href="#">第三層選單</a></li>
                    </ul>
                </li>
                <li><a href="http://www.google.com">第二層有連結</a>
                    <ul>
                        <li><a href="http://www.google.com">第三層選單有下層</a>
                            <ul>
                                <li><a href="#">第四層選單第四層選單</a></li>
                                <li><a href="#">第四層選單</a></li>
                            </ul>
                        </li>
                        <li><a href="http://www.google.com">第三層選單有連結</a></li>
                        <li><a href="#">第三層選單</a></li>
                    </ul>
                </li>
                <li><a href="#">第二層選單</a></li>
                <li><a href="#">第二層選單</a>
                    <ul>
                        <li><a href="http://www.google.com">第三層選單有下層</a></li>
                        <li><a href="http://www.google.com">第三層選單有連結</a></li>
                        <li><a href="#">第三層選單</a></li>
                        <li><a href="#">第三層選單</a></li>
                        <li><a href="#">第三層選單</a></li>
                    </ul>
                </li>
                <li><a href="#">第二層選單</a>
                    <ul>
                        <li><a href="http://www.google.com">第三層選單有下層</a></li>
                        <li><a href="http://www.google.com">第三層選單有連結</a></li>
                        <li><a href="#">第三層選單</a></li>
                    </ul>
                </li>
                <li><a href="http://www.google.com">第二層有連結</a>
                    <ul>
                        <li><a href="http://www.google.com">第三層選單有下層</a>
                            <ul>
                                <li><a href="#">第四層選單</a></li>
                                <li><a href="#">第四層選單</a></li>
                            </ul>
                        </li>
                        <li><a href="http://www.google.com">第三層選單有連結</a></li>
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
<!-- megamenu End -->
```

<style>
.ui-infobar{
max-width:95%;
}
.markdown-body{
max-width:95%;
}
</style>