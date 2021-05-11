# Font-Size / 控制文章字體大小

###### tags: `HyUI`
檔案名稱：sass/modual/_function_panel.scss
檔案名稱：sass/element/_font.scss
檔案名稱：page/_template.scss



:::warning
注意 :zap: font-size 模組需搭配頁面上有文章內容作切換呈現，可用 <font color="#009ee7">內容的部分</font> 或 <font color="#009ee7">需要網站全域</font> 字級控制，可自行到 <font color="#ff0000">hyui.js</font> 將選擇器改為 <font color="#ff0000">innerpage</font>或 <font color="#ff0000">body</font> 即可。
:::

<iframe height="265" style="width: 100%;" scrolling="no" title="Font-Size / 控制文章字體大小" src="https://codepen.io/u00hyui/embed/wvJvqPx?height=265&theme-id=dark&default-tab=html,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/u00hyui/pen/wvJvqPx'>Font-Size / 控制文章字體大小</a> by u00hyui
  (<a href='https://codepen.io/u00hyui'>@u00hyui</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

## HTML範本
```htmlmixed=
<!-- font_size -->
<div class="font_size">
  <span>字型大小：</span>
  <!-- 英文用<span>font-size：</span> -->
  <ul>
    <li><a href="#" class="small">小</a></li>
    <li><a href="#" class="medium">中</a></li>
    <li><a href="#" class="large">大</a></li>
  </ul>
</div>
```

## SCSS預設的文字大中小設定
>可於 <font color="#EE428B">_template.scss</font> 設定文字的大小，預設為 <font color="#EE428B">medium</font> 適中字型 <font color="#EE428B">1em</font> 大小，為網站的基本設定，因此只需要設定 <font color="#EE428B">小</font> 、 <font color="#EE428B">大</font> 的字級即可，目前字級大小設定設於 <font color="#EE428B">.innerpage</font> 內，如有特殊需求，可自行修改預設值。


* 小型字體大小：0.938em(15px)
* 中型字體大小：1em(16px)
* 大型字體大小：1.125em(18px) 


```sass=
.innerpage {
    &.small_size {
        font-size: .938em;
    }
    &.large_size {
        font-size: 1.125em;
    }
}
```
:link: [內文示範字級連結](https://hywebu00.github.io/hyui_flex/cp_template.htm)
## JQuery設定:round_pushpin:
```javascript=
/*------------------------------------*/
/////////////字型大小 font-size//////////
/*------------------------------------*/
$('.font_size').find('.small').click(function(e) {
    $(this).parent('li').siblings('li').find('a').removeClass('active');
    $('.innerpage').removeClass('large_size').addClass('small_size');
    $(this).addClass('active');
    e.preventDefault();
    createCookie('FontSize', 'small', 356);
});
$('.font_size').find('.medium').click(function(e) {
    $(this).parent('li').siblings('li').find('a').removeClass('active');
    $('.innerpage').removeClass('large_size small_size');
    $(this).addClass('active');
    e.preventDefault();
    createCookie('FontSize', 'medium', 356);
});
$('.font_size').find('.large').click(function(e) {
    $(this).parent('li').siblings('li').find('a').removeClass('active');
    $('.innerpage').removeClass('small_size').addClass('large_size');
    $(this).addClass('active');
    e.preventDefault();
    createCookie('FontSize', 'large', 356);
});

function createCookie(name, value, days) {
    if (days) {
        var date = new Date();
        date.setTime(date.getTime() + (days * 24 * 60 * 60 * 1000));
        var expires = "; expires=" + date.toGMTString();
    } else expires = "";
    document.cookie = name + "=" + value + expires + "; path=/";
}

function readCookie(name) {
    var nameEQ = name + "=";
    var ca = document.cookie.split(';');
    for (var i = 0; i < ca.length; i++) {
        var c = ca[i];
        while (c.charAt(0) == ' ') c = c.substring(1, c.length);
        if (c.indexOf(nameEQ) == 0) return c.substring(nameEQ.length, c.length);
    }
    return null;
}
window.onload = function(e) {
    var cookie = readCookie("FontSize");
    //alert('cookie='+cookie);
    if (cookie == 'small') {
        //$('.font_size').find('.small').click();
        $('.font_size').find('.small').parent('li').siblings('li').find('a').removeClass('active');
        $('.innerpage').removeClass('large_size medium_size').addClass('small_size');
        $('.font_size').find('.small').addClass('active');
        e.preventDefault();
    } else {
        if (cookie == 'large') {
            //$('.font_size').find('.large').click();
            $('.font_size').find('.large').parent('li').siblings('li').find('a').removeClass('active');
            $('.innerpage').removeClass('small_size medium_size').addClass('large_size');
            $('.font_size').find('.large').addClass('active');
            e.preventDefault();
        } else {
            //這裡是預設宣告
            //$('.font_size').find('.medium').click();
            $('.font_size').find('.medium').parent('li').siblings('li').find('a').removeClass('active');
            $('.innerpage').removeClass('large_size small_size');
            $('.font_size').find('.medium').addClass('active');
            e.preventDefault();
        }
    }
}
```
可參考：[Function-Panel模組](/Oqp96iFITTilUfkBkoSbjA)

<style>
.ui-infobar{
max-width:95%;
}
.markdown-body{
max-width:95%;
}
</style>
