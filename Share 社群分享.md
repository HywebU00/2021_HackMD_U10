# Share / 社群分享
###### tags: `HyUI`

檔案名稱：sass/modual/_function_panel.scss

提供兩種圖檔檔案格式 <font color="#EE428B">svg</font> 以及 <font color="#EE428B">png</font>，替換img的檔名即可。預設提供 <font color="#009ee7">facebook</font>、<font color="#009ee7">twitter</font>、<font color="#009ee7">line</font>、<font color="#009ee7">youtube</font>、<font color="#009ee7">google+</font>、<font color="#009ee7">instagram</font>、<font color="#009ee7">linkedIn</font>...等常用社群媒體分享icon，如需要新增或刪除可自行調整。

## HTML 範例1 －SVG格式

<iframe height="265" style="width: 100%;" scrolling="no" title="Share / 社群分享 - SVG格式" src="https://codepen.io/u00hyui/embed/abJzdWb?height=265&theme-id=dark&default-tab=html,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/u00hyui/pen/abJzdWb'>Share / 社群分享 - SVG格式</a> by u00hyui
  (<a href='https://codepen.io/u00hyui'>@u00hyui</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

```htmlmixed=
<!-- 社群分享 -->
<div class="share">
    <ul>
        <li><a href="#"><img src="images/basic/icon_facebook.svg" alt="facebook"></a></li>
        <li><a href="#"><img src="images/basic/icon_twitter.svg" alt="twitter"></a></li>
        <li><a href="#"><img src="images/basic/icon_line.svg" alt="line"></a></li>
        <li><a href="#"><img src="images/basic/icon_youtube.svg" alt="youtube"></a></li>
        <li><a href="#"><img src="images/basic/icon_googleplus.svg" alt="google plus"></a></li>
        <li><a href="#"><img src="images/basic/icon_instagram.svg" alt="instagram"></a></li>
        <li><a href="#"><img src="images/basic/icon_linkedin.svg" alt="LinkedIn"></a></li>
        <li><a href="#"><img src="images/basic/icon_rss.svg" alt="RSS"></a></li>
    </ul>
</div>
```


## HTML 範例2 －加入function_panel內

<iframe height="265" style="width: 100%;" scrolling="no" title="Share / 社群分享 - 加入function_panel內" src="https://codepen.io/u00hyui/embed/RwpNrZV?height=265&theme-id=dark&default-tab=html,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/u00hyui/pen/RwpNrZV'>Share / 社群分享 - 加入function_panel內</a> by u00hyui
  (<a href='https://codepen.io/u00hyui'>@u00hyui</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>


```htmlmixed=
<div class="function_panel">
    <div class="share">
        <ul>
            <li><a href="#"><img src="images/basic/icon_facebook.svg" alt="facebook"></a></li>
            <li><a href="#"><img src="images/basic/icon_twitter.svg" alt="twitter"></a></li>
            <li><a href="#"><img src="images/basic/icon_line.svg" alt="line"></a></li>
            <li><a href="#"><img src="images/basic/icon_youtube.svg" alt="youtube"></a></li>
            <li><a href="#"><img src="images/basic/icon_googleplus.svg" alt="google plus"></a></li>
            <li><a href="#"><img src="images/basic/icon_instagram.svg" alt="instagram"></a></li>
            <li><a href="#"><img src="images/basic/icon_linkedin.svg" alt="LinkedIn"></a></li>
            <li><a href="#"><img src="images/basic/icon_rss.svg" alt="RSS"></a></li>
        </ul>
    </div>
</div>
```
可參考：[Function-Panel模組](/Oqp96iFITTilUfkBkoSbjA)


因  <font color="#EE428B">share</font> 原本裡面沒有預設的按鈕，因此需要用JQUERY另外判斷在  <font color="#EE428B">funtion_panel</font> 裡的  <font color="#EE428B">share</font> 加上  <font color="#EE428B">shareButton</font> 的按鈕樣式。以下也加入了無障礙的tab遊走設定。

## 範例2-JQuery設定:round_pushpin:

```javascript=
/*------------------------------------*/
    //////////分享按鈕 share dropdwon////////
    /*------------------------------------*/
    $('.function_panel .share').children('ul').hide();
    $('.function_panel .share').prepend('<a href="#" class="shareButton">share分享按鈕</a>');
    var _shareButton = $('.shareButton');
    _shareButton.off().click(function(e) {
        $(this).siblings('ul').stop(true, true).slideToggle();
        e.preventDefault();
    });
    _shareButton.keyup(function(event) {
        $(this).siblings('ul').stop(true, true).slideDown();
    });
    $('.function_panel .share').find('li:last>a').focusout(function(event) {
        $(this).parent().parent('ul').hide();
    });
    // 點外面關閉share
    $(document).on('touchend click', function(e) {
        var container = $(".function_panel .share");
        if (!container.is(e.target) && container.has(e.target).length === 0) {
            $('.function_panel .share ul').hide();
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