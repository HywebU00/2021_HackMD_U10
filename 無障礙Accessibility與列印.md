# 無障礙(Accessibility)與列印
###### tags: `HyUI`

## 支持無障礙2.0 AA等級

針對國家通訊傳播委員會頒布之<font color="#009ee7">網站無障礙規範2.0版</font>，其中許多規範會影響到網站開發者處理無障礙的設定，讓無障礙檢測都能透過鍵盤使用，HyUI在 <font color="#EE428B">SASS</font> 及 <font color="#EE428B">hyui.js</font> 已經針對「連結」、「選單操作」...等預先調整了相關的設定，目前是以無障礙2.0AA版本為基礎。


:::warning
注意 :zap:
無障礙以機器檢測與人工檢測為準，HyUI只能預先處理基礎樣式，如遇到客製專案需求開發，仍需靠開發人員共同處理。
:::

## 快速鍵設定

本網站依無障礙網頁設計原則建置，網站的主要內容分為三大區塊：
>1. 上方功能區塊、 2. 中央內容區塊、 3.下方功能區塊。[color=#009ee7]

* Alt+U：上方功能區塊，包括回首頁、網站導覽、網站搜尋、字體選擇、版本選擇等。
* Alt+C：中央內容區塊，為本頁主要內容區。
* Alt+Z：下方功能區塊。
* Alt+S：網站搜尋。
* 如果您的瀏覽器是Firefox，快速鍵的使用方法是 Shift+Alt+(快速鍵字母)，例如 Shift+Alt+C會跳至網頁中央區塊，以此類推。



![](https://i.imgur.com/bpztC6e.png =300x420)


※當本網站項目頁籤無法以滑鼠點選時，您可利用以下鍵盤操作方式瀏覽資料
← → or ↑↓：按左右鍵或上下鍵移動標籤順序。
Home or End→：可直接跳至標籤第一項或者最後一項。
Tab：停留於該標籤後,可利用Tab鍵跳至內容瀏覽該筆資料，遇到radio按鈕時請配合使← → or↑↓鍵移動項目順序。
Tab + Shift：按Tab + Shift可往回跳至上一筆資料；當跳回至標籤項目時您可繼續利用← → or↑↓鍵移動標籤順序。

```htmlmixed=
<!-- 直接跳主內容區 -->
<a class="goCenter" href="#center" tabindex="1">按Enter到主內容區</a>
```
## 快捷錨點設定

目前提供之頁面範本，已先置入相對應位置，但可依照專案另外做客製化設定。
```htmlmixed=
<!-- 網站標題區 -->
<a class="accesskey" href="#aU" id="aU" accesskey="U" title="網站標題" tabindex="2">:::</a>
<!-- 網站搜尋 (放置input輸入框) -->
<input name="username" id="mustSameAsId" type="text" placeholder="請輸入文字" accesskey="S" title="請輸入文字" aria-label="搜尋網站內容">
<!-- 主要內容區 -->
<a class="accesskey" href="#aC" id="aC" accesskey="C" title="主要內容區">:::</a>
<!-- 頁尾區 -->
<a class="accesskey" href="#aZ" id="aZ" accesskey="Z" title="頁尾區">:::</a>
```


## JQuery設定:round_pushpin:

```javascript=
/*-----------------------------------*/
/////////// 無障礙快捷鍵盤組合  //////////
/*-----------------------------------*/
$(document).on('keydown', function(e) {
    // alt+S 查詢
    if (e.altKey && e.keyCode == 83) {
        $('html, body').animate({ scrollTop: 0 }, 200, 'easeOutExpo');
        $('.search').find('input[type="text"]').focus();
    }
    // alt+U header
    if (e.altKey && e.keyCode == 85) {
        $('html, body').animate({ scrollTop: 0 }, 200, 'easeOutExpo');
        $('header').find('.accesskey').focus();
    }
    // alt+C 主要內容區
    if (e.altKey && e.keyCode == 67) {
        $('html, body').stop(true, true).animate({ scrollTop: $('.main').find('.accesskey').offset().top - 70 }, 800, 'easeOutExpo');
        $('.main').find('.accesskey').focus();
    }
    // alt+Z footer
    if (e.altKey && e.keyCode == 90) {
        $('html, body').stop(true, true).animate({ scrollTop: $('footer').find('.accesskey').offset().top }, 800, 'easeOutExpo');
        $('footer').find('.accesskey').focus();
    }
});
//無障礙切換slick箭頭語系
if ($('html')[0].hasAttribute("labg")) {
    var weblang = $('html').attr('lang');
    if (weblang.substring(0, 2) == 'zh') {
        $('.slick-prev').attr('title', '上一筆');
        $('.slick-next').attr('title', '下一筆');
    } else if (weblang.substring(0, 2) !== 'zh') {
        $('.slick-prev').attr('title', 'previous');
        $('.slick-next').attr('title', 'next');
    }
}
// 無障礙錨點切換語系，更改accesskey的title名稱
var weblang = $('html').attr('lang');
if (weblang.substring(0, 2) == 'zh') {
    $('header').find('.accesskey').attr('title', '上方功能區塊');
    $('.main').find('.accesskey').attr('title', '中央內容區塊');
    $('footer').find('.accesskey').attr('title', '下方功能區塊');
    $('.search').find('.accesskey').attr('title', '關鍵字搜尋：文章關鍵字搜尋');
} else if (weblang.substring(0, 2) !== 'zh') {
    $('header').find('.accesskey').attr('title', 'header');
    $('.main').find('.accesskey').attr('title', 'content');
    $('footer').find('.accesskey').attr('title', 'footer');
    $('.search').find('.accesskey').attr('title', 'search');
}
```
## 列印

列印樣式，請於 <font color="#EE428B">_print.scss</font> 編寫SCSS，同樣統一匯出於 <font color="#EE428B">hyui.css</font> 內。

檔案名稱：檔案名稱：sass/common/_print.scss

:::warning
注意 :zap:

媒體格式需使用@media print；如需要預覽，請於瀏覽器點選列印 / 預覽列印 檢視。
:::

範例：

```sass=
// 列印樣式
@media print {
    %no-bg {
        background: none;
    }
    /* -------------------------------不需要列印的區塊，請放置於這----//*/
    header,
    .fatfooter,
    footer,
    .accesskey,
    .submenu {
        display: none;
    }
   ....
   ....
   ....
        p {
            a {
                word-wrap: break-word;
            }
            a[href^="http"]:after {
                content: " ("attr(href) ")";
                font-size: 90%;
            }
            a[href^="#"]:after {
                display: none;
            }
        }
        abbr[title]:after {
            content: " ("attr(title) ")";
        }
        table {
            background: #FFF;
        }
        li {
            content: "» ";
        }
    }
}
```
























<style>
.ui-infobar{
max-width:95%;
}
.markdown-body{
max-width:95%;
}
</style>