# Tabs / 頁籤
###### tags: `HyUI`

檔案名稱：sass/modual/_tabs.scss

提供一組可響應式及通過無障礙tab遊走之tab頁籤模組。

>* 頁籤沒有數量限制，但請注意畫面上的均衡比例。建議勿超過5組為宜。
>* 可客製不同樣式，於 <font color="#EE428B">tabs</font> 後方新增不同的 <font color="#EE428B">classname</font> 即可。
>* 可自訂響應式斷點(breakpoit)，目前是以 <font color="#EE428B">wwSmall</font> 為預設斷點，如有 特殊需求，可另外替換變數或數值。

## HTML範本1

<iframe height="500" style="width: 100%;" scrolling="no" title="Tabs / 頁籤 1" src="https://codepen.io/u00hyui/embed/PopZyGm?height=265&theme-id=dark&default-tab=js,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/u00hyui/pen/PopZyGm'>Tabs / 頁籤 1</a> by u00hyui
  (<a href='https://codepen.io/u00hyui'>@u00hyui</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### <font color="#EE428B">tabs</font> 後方新增不同的 <font color="#EE428B">classname</font> ，可客製不同樣式


<iframe height="500" style="width: 100%;" scrolling="no" title="Tabs / 頁籤2" src="https://codepen.io/u00hyui/embed/VwpeVgB?height=265&theme-id=dark&default-tab=js,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/u00hyui/pen/VwpeVgB'>Tabs / 頁籤2</a> by u00hyui
  (<a href='https://codepen.io/u00hyui'>@u00hyui</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>


```htmlmixed=
<div class="tabSet">
    <section class="tabs example-2">
        <button type="button" class="tabItem active">第一個頁籤</button>
        <!--選到的頁籤項目-->
        <div class="tabContent">
            <ul>
                <li><a href="#">1第一則消息消息消息消息消息消息</a><time>107-01-01</time></li>
                <li><a href="#">第二則消息</a><time>107-01-01</time></li>
                <li><a href="#">第三則消息</a><time>107-01-01</time></li>
                <li><a href="#">第四則消息</a><time>107-01-01</time></li>
                <li><a href="#">第五則消息</a><time>107-01-01</time></li>
            </ul>
            <div class="more"><a href="#">更多</a></div>
        </div>
        <button type="button" class="tabItem">第二個頁籤</button>
        <div class="tabContent">
            <ul>
                <li><a href="#">2第一則消息</a><time>107-01-01</time></li>
                <li><a href="#">第二則消息</a><time>107-01-01</time></li>
                <li><a href="#">第三則消息</a><time>107-01-01</time></li>
                <li><a href="#">第四則消息</a><time>107-01-01</time></li>
                <li><a href="#">第五則消息</a><time>107-01-01</time></li>
            </ul>
            <div class="more"><a href="#">更多</a></div>
        </div>
        <button type="button" class="tabItem">第三個頁籤</button>
        <div class="tabContent">
            <ul>
                <li><a href="#">3第一則消息</a><time>107-01-01</time></li>
                <li><a href="#">第二則消息</a><time>107-01-01</time></li>
                <li><a href="#">第三則消息</a><time>107-01-01</time></li>
                <li><a href="#">第四則消息</a><time>107-01-01</time></li>
                <li><a href="#">第五則消息</a><time>107-01-01</time></li>
            </ul>
            <div class="more"><a href="#">更多</a></div>
        </div>
        <button type="button" class="tabItem">第四個頁籤</button>
        <div class="tabContent">
            <ul>
                <li><a href="#">4第一則消息</a><time>107-01-01</time></li>
                <li><a href="#">第二則消息</a><time>107-01-01</time></li>
                <li><a href="#">第三則消息</a><time>107-01-01</time></li>
                <li><a href="#">第四則消息</a><time>107-01-01</time></li>
                <li><a href="#">第五則消息</a><time>107-01-01</time></li>
            </ul>
            <div class="more"><a href="#">更多</a></div>
        </div>
    </section>
</div>
```

## JQuery設定:round_pushpin:
```javascript=
var _window = $(window),
    ww = _window.outerWidth(),
    wh = _window.height(),
    _body = $("body"),
    wwNormal = 1400,
    wwMedium = 992,
    wwSmall = 768,
    wwxs = 576;
var tab_headerHeight = Math.floor($(".header").outerHeight(true));

var resizeTimer1;
_window.resize(function() {
    clearTimeout(resizeTimer1);
    resizeTimer1 = setTimeout(function() {
        ww = _window.outerWidth();
        tabSet();
    }, 50);
});

function tabSet() {
    $(".tabs").each(function() {
        var _tab = $(this),
            _tabItem = _tab.find(".tabItem"),
            // _tabItemA = _tabItem.children('a'), //改button後，這行沒有
            _tabContent = _tab.find(".tabContent"),
            tabwidth = _tab.width(),
            tabItemHeight = _tabItem.outerHeight(),
            tabContentHeight = _tab.find(".active").next().innerHeight(),
            tiGap = 0,
            tabItemLength = _tabItem.length,
            tabItemWidth;
        _tab.find(".active").next(".tabContent").show();
        if (ww >= wwSmall) {
            _tabContent.css("top", tabItemHeight);
            _tab.height(tabContentHeight + tabItemHeight);
            tabItemWidth = (tabwidth - (tabItemLength - 1) * tiGap) / tabItemLength;
            _tabItem.width(tabItemWidth).css("margin-left", tiGap);
            _tabItem.first().css("margin-left", 0);
            _tabItem.last().css({ position: "absolute", top: 0, right: 0 }).width(tabItemWidth);
        } else {
            _tab.css("height", "auto");
            _tabItem.width(tabwidth);
            _tabItem.css("margin-left", 0).last().css("position", "relative");
        }
        _tabItem.focus(tabs); //改button後，前面改_tabItem
        _tabItem.click(tabs); //改button後，前面改_tabItem
        function tabs(e) {
            var _tabItemNow = $(this), //改button後，原來$(this).parent(),改$(this)
                tvp = _tab.offset().top,
                tabIndex = _tabItemNow.index() / 2,
                scollDistance = tvp + tabItemHeight * tabIndex - tab_headerHeight;
            _tabItem.removeClass("active");
            _tabItemNow.addClass("active");
            if (ww <= wwSmall) {
                _tabItem.not(".active").next().slideUp();
                _tabItemNow.next().slideDown();
                $("html,body").stop(true, false).animate({ scrollTop: scollDistance });
            } else {
                _tabItem.not(".active").next().hide();
                _tabItemNow.next().show();
                tabContentHeight = _tabItemNow.next().innerHeight();
                _tab.height(tabContentHeight + tabItemHeight);
            }
            e.preventDefault();
        }
    });
}
$(".tabs>.tabItem:first-child>a").trigger("click");
tabSet();
```




<style>
.ui-infobar{
max-width:95%;
}
.markdown-body{
max-width:95%;
}
</style>