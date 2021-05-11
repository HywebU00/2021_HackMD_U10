# Language 選擇語系選單

###### tags: `HyUI`

檔案名稱：sass/element/_language.scss


此模組可單獨使用，語系數量不限，目前已預設用於<font color="#EE428B">header</font>之<font color="#EE428B">.navigation</font>區塊中，並已經自動設定偵測<font color="#EE428B">html</font>裡面是否有<font color="#EE428B">language</font>模組，讓<font color="#EE428B">navigation</font>自動排版，讓模組放置於適當位置，如需要調整請參考以下設定。


<iframe height="265" style="width: 100%;" scrolling="no" title="language" src="https://codepen.io/u00hyui/embed/NWdVpNP?height=265&theme-id=dark&default-tab=js,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/u00hyui/pen/NWdVpNP'>language</a> by u00hyui
  (<a href='https://codepen.io/u00hyui'>@u00hyui</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

## HTML範本
```htmlmixed=
<div class="language">
    <a href="#">語言選擇</a>
    <ul>
        <li><a href="#">繁體中文</a></li>
        <li><a href="#">简体中文</a></li>
        <li><a href="#">ENGLISH</a></li>
    </ul>
</div>
```

## JQuery設定:round_pushpin:

### 自動偵測模組存在設定
```javascript=
$('.navigation').has('.language').addClass('have_language');
```
### 語言模組 無障礙遊走設定
```javascript=
/*-----------------------------------*/
//////// 語言模組 無障礙遊走設定  ////////
/*-----------------------------------*/
$('.language').find('ul').hide();
var openLang = $('.language').children('a');
openLang.off().click(function(e) {
    $(this).next('ul').stop(true, true).slideToggle();
    e.preventDefault();
});
openLang.keyup(function() {
    $(this).next('ul').stop(true, true).slideDown();
});
$('.language').find('ul li:last>a').focusout(function() {
    $('.language').find('ul').hide();
});
$(document).on('touchend click', function(e) {
    var target = e.target;
    if (!$(target).is('.language a')) {
        $('.language').find('ul').hide();
    }
});
```


<style>
.ui-infobar{
max-width:95%;
}
.markdown-body{
max-width:95%;
}
</style>
