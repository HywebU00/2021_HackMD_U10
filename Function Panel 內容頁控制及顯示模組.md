# Function Panel / 內容頁控制及顯示模組

###### tags: `HyUI`
檔案名稱：sass/modual/_function_panel.scss

## 提供一組已組合好的內容頁文章控制及顯示模組

可自由組合 <font color="#009ee7">發布日期</font>、<font color="#009ee7">文字大小</font>、<font color="#009ee7">回上一頁</font>、<font color="#009ee7">友善列印</font>、<font color="#009ee7">轉寄友人</font> 、<font color="#009ee7">社群分享</font>...等目前以提供之模組，在父層包覆1個 <font color="#EE428B">function_panel</font> 的div，即可呈現以下樣式。 ，模組無需更改結構只需要放進 <font color="#EE428B">function_panel</font> 的div即可。

預設包含：
* 發布時間
* [文字大小](/6SM3arriSvSN_bUmeFjWAg)
* [回上一頁](/ecYKCMloQXazqZEqW8rqaQ)
* [友善列印](/ecYKCMloQXazqZEqW8rqaQ)
* [轉寄友人](/ecYKCMloQXazqZEqW8rqaQ)
* [社群分享](/mz6QuOJpQOa1LF84tNtFOQ)



<iframe height="400" style="width: 100%;" scrolling="no" title="Function Panel / 內容頁控制及顯示模組" src="https://codepen.io/u00hyui/embed/qBrWbRr?defaultTab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/qBrWbRr">
  Function Panel / 內容頁控制及顯示模組</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

## HTML範本
```htmlmixed=
<!-- function_panel -->
<div class="function_panel">
    <div class="publish_time">
        <span>發布日期：</span><time>2019-01-01</time>
    </div>
    <!-- 文字大小 -->
    <div class="font_size">
        <span>字型大小：</span>
        <!-- 英文用<span>font-size：</span> -->
        <ul>
            <li><a href="#" class="small">小</a></li>
            <li><a href="#" class="medium">中</a></li>
            <li><a href="#" class="large">大</a></li>
        </ul>
    </div>
    <!-- function功能區塊 -->
    <div class="function">
        <ul>
            <li class="back"><a href="javascript:history.back()">回上一頁</a></li>
            <li class="print"><a href="#">友善列印</a></li>
            <li class="forward"><a href="#">轉寄友人</a></li>
        </ul>
    </div>
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
            <li><a href="#"><img src="images/basic/icon_plurk.svg" alt="Plurk"></a></li>
        </ul>
    </div>
</div>
```
## JQuery設定:round_pushpin:
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
