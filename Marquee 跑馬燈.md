# Marquee / 跑馬燈

###### tags: `HyUI`

檔案名稱：sass/modual/_marquee.scss

HyUI提供跑馬燈的範例，有使用 <font color="#009ee7">slick</font> 的輪播模組，需先在網頁中匯入外掛CSS及js，可參考模組 [Slider圖片輪播](/VkhALd3wTYSt_ctD6W0XPQ)說明。

<iframe height="265" style="width: 100%;" scrolling="no" title="Marquee / 跑馬燈" src="https://codepen.io/u00hyui/embed/PopwGzj?height=265&theme-id=dark&default-tab=html,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/u00hyui/pen/PopwGzj'>Marquee / 跑馬燈</a> by u00hyui
  (<a href='https://codepen.io/u00hyui'>@u00hyui</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

## HTML範本
```htmlmixed=
<div class="marquee">
    <ul>
        <li><a href="javascript:;"><span>2018-11-13</span>因尼莎颱風來襲，7/31下午2時之我國化學物質管理政策綱領第一次跨部會研商會取消。</a></li>
        <li><a href="javascript:;"><span>2018-11-13</span>因尼莎颱風來襲，7/31下午2時之我國化學物質管理政策綱領第一次跨部會研商會取消。</a></li>
        <li><a href="javascript:;"><span>2018-11-13</span>因尼莎颱風來襲，7/31下午2時之我國化學物質管理政策綱領第一次跨部會研商會取消。</a></li>
        <li><a href="javascript:;"><span>2018-11-13</span>因尼莎颱風來襲，7/31下午2時之我國化學物質管理政策綱領第一次跨部會研商會取消。</a></li>
    </ul>
</div>
```

# JQuery設定
```javascript=

if ($('.marquee').length > 0) {
    $('.marquee ul').slick({
        dots: false,
        infinite: true,
        vertical: true,
        verticalSwiping: true,
        speed: 300,
        autoplaySpeed: 5000,
        slidesToShow: 1,
        slidesToScroll: 1,
        autoplay: true,
        pauseOnHover: true, //滑鼠移過後暫停自動撥放
        focusOnSelect: true,
    });
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