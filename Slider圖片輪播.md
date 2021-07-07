# Slider/圖片輪播

###### tags: `HyUI`


檔案名稱：vendor/slick/slick-theme.css
檔案名稱：vendor/slick/slick.css
檔案名稱：sass/modual/_slick.scss (合併上面兩個)

HyUI使用 <font color="#009ee7">slick</font> 的輪播模組，目前hyUI  <font color="#EE428B">vendor</font> 內含 <font color="#EE428B">slick</font> 已經有加入客製化設定，如需要最新版，請到 <font color="#009ee7">[slick](https://kenwheeler.github.io/slick/)</font> 官網下載。

## 請在網頁中匯入slick 外掛

slick屬於外掛，故放在 <font color="#EE428B">vendor</font> 資料夾裡，包括所有的圖檔、js、css

## 匯入外掛CSS

```htmlmixed=
<link rel="stylesheet" type="text/css" href="vendor/slick/slick.css" />
<link rel="stylesheet" type="text/css" href="vendor/slick/slick-theme.css" />
```

## 匯入JS

```htmlmixed=
<script src="vendor/slick/slick.min.js "></script>
```
## Slick的基本設定

使用設定以slick官方文件為準。
```javascript=
$(document).ready(function(){
  $('.your-class').slick({
    arrows: true,                       //左右箭頭
    autoplay: false,                    //自動播放
    autoplaySpeed: 3000,                //自動播放秒數
    dots: false,                        //顯示圓點
    dotsClass:  'slick-dots',           //原點css
    draggable: true,                    //滑鼠可以拖曳
    infinite: true,                     //無限輪播
    pauseOnHover: true,                 //滑鼠移過後暫停自動撥放
    pauseOnDotsHover: false,            //滑鼠移過圓點後暫停自動撥放
    rtl: false,                         //改變輪播方向
    slidesToShow: 1,                    //一次顯示幾張
    slidesToScroll: 1,                  //一次輪播幾張
    vertical: false ,                   //改成垂直方向
    fade: true,                         // 淡入
    centerMode: true,                   //圖片中心模式
  });
});
```

## <font color="#009ee7">01.大圖輪播範例</font> 

本版本輪播圖檔可使用 <font color="#EE428B">obect-fit</font> 設定，故上稿內容不限尺寸，皆可正常呈現。

<iframe height="500" style="width: 100%;" scrolling="no" title="Slider 大圖輪播" src="https://codepen.io/u00hyui/embed/poeMgrd?defaultTab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/poeMgrd">
  Slider 大圖輪播</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

## HTML範本

圖檔顯示比例可參考image.htm
```htmlmixed=
<!-- 圖片輪播 start -->
<div class="mpSlider">
    <div class="img-container">
        <a href="#" title="">
            <picture>
                <source media="(min-width: 1200px)" data-srcset="images/demo/01.jpg">
                <source media="(min-width: 992px)" data-srcset="images/demo/01.jpg">
                <source media="(min-width: 576px)" data-srcset="images/demo/01.jpg">
                <source media="(max-width: 575px)" data-srcset="images/demo/01.jpg">
                <img data-src="images/demo/01.jpg" class="cover lazy" alt="圖說1">
                <noscript><img src="images/demo/01.jpg" alt="圖說1"></noscript>
            </picture>
            <span class="caption">圖說1</span>
        </a>
    </div>
    <div class="img-container">
        <a href="#" title="">
            <picture>
                <source media="(min-width: 1200px)" data-srcset="images/demo/02.jpg">
                <source media="(min-width: 992px)" data-srcset="images/demo/02.jpg">
                <source media="(min-width: 576px)" data-srcset="images/demo/02.jpg">
                <source media="(max-width: 575px)" data-srcset="images/demo/02.jpg">
                <img data-src="images/demo/02.jpg" class="cover lazy" alt="圖說2">
                <noscript><img src="images/demo/02.jpg" alt="圖說2"></noscript>
            </picture>
            <span class="caption">圖說2</span>
        </a>
    </div>
    <div class="img-container">
        <a href="#" title="">
            <picture>
                <source media="(min-width: 1200px)" data-srcset="images/demo/03.jpg">
                <source media="(min-width: 992px)" data-srcset="images/demo/03.jpg">
                <source media="(min-width: 576px)" data-srcset="images/demo/03.jpg">
                <source media="(max-width: 575px)" data-srcset="images/demo/03.jpg">
                <img data-src="images/demo/03.jpg" class="cover lazy" alt="圖說3">
                <noscript><img src="images/demo/03.jpg" alt="圖說3"></noscript>
            </picture>
            <span class="caption">圖說3</span>
        </a>
    </div>
</div>
<!-- 圖片輪播 end -->
```



## <font color="#009ee7">02.廣告輪播範例</font> 

<iframe height="300" style="width: 100%;" scrolling="no" title="廣告輪播範例" src="https://codepen.io/u00hyui/embed/oNZKobG?defaultTab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/oNZKobG">
  廣告輪播範例</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

## HTML範本

```htmlmixed=
<!-- 廣告輪播   start -->
<div class="adSlider">
    <div class="img-container">
        <a href="#" title="">
            <img data-lazy="images/demo/ad_01.jpg" class="contain" alt="圖片說明1">
        </a>
    </div>
    <div class="img-container">
        <a href="#" title="">
            <img data-lazy="images/demo/ad_02.jpg" class="contain" alt="圖片說明2">
        </a>
    </div>
    <div class="img-container">
        <a href="#" title="">
            <img data-lazy="images/demo/ad_03.jpg" class="contain" alt="圖片說明3">
        </a>
    </div>
    <div class="img-container">
        <a href="#" title="">
            <img data-lazy="images/demo/ad_04.jpg" class="contain" alt="圖片說明4">
        </a>
    </div>
    <div class="img-container">
        <a href="#" title="">
            <img data-lazy="images/demo/ad_05.jpg" class="contain" alt="圖片說明5">
        </a>
    </div>
    <div class="img-container">
        <a href="#" title="">
            <img data-lazy="images/demo/ad_06.jpg" class="contain" alt="圖片說明6">
        </a>
    </div>
    <div class="img-container">
        <a href="#" title="">
            <img data-lazy="images/demo/ad_07.jpg" class="cover" alt="圖片說明7">
        </a>
    </div>
</div>
<!-- 廣告輪播   end -->
```
## <font color="#009ee7">03.照片輪播範例</font> 

<iframe height="750" style="width: 100%;" scrolling="no" title="照片輪播" src="https://codepen.io/u00hyui/embed/vYxoWRz?defaultTab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/vYxoWRz">
  照片輪播</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

## HTML範本

```htmlmixed=
<div class="Syncing_slider">
    <!--大圖slider-for-->
    <div class="Slider-for">
        <div>
            <div class="img-container">
                <img src="https://assets.imgix.net/examples/kingfisher.jpg?w=500&h=480&fit=crop&auto=format%2Cenhance&usm=20">
            </div>
            <p>第一張圖說</p>
        </div>
        <div>
            <div class="img-container">
                <img src="https://assets.imgix.net/examples/puffins.jpg?w=800&h=480&fit=crop&auto=format%2Cenhance&usm=20">
            </div>
            <p>第二張圖說</p>
        </div>
        <div>
            <div class="img-container">
                <img src="https://assets.imgix.net/examples/womanlandscape.jpg?w=800&h=480&fit=crop&auto=format%2Cenhance&usm=20">
            </div>
            <p>第三張圖說</p>
        </div>
        <div>
            <div class="img-container">
                <img src="https://assets.imgix.net/unsplash/paperlamp.jpg?w=800&h=480&fit=crop&auto=format%2Cenhance&usm=20">
            </div>
            <p>第四張圖說</p>
        </div>
    </div>
    <!-- slider-for end-->
    <div class="controls"></div>
    <!--小圖slider-nav-->
    <div class="Slider-nav">
        <div>
            <div class="img-container">
                <img src="https://assets.imgix.net/examples/kingfisher.jpg?w=800&h=480&fit=crop&auto=format%2Cenhance&usm=20">
            </div>
            <p>第一張圖說</p>
        </div>
        <div>
            <div class="img-container">
                <img src="https://assets.imgix.net/examples/puffins.jpg?w=800&h=480&fit=crop&auto=format%2Cenhance&usm=20">
            </div>
            <p>第二張圖說</p>
        </div>
        <div>
            <div class="img-container">
                <img src="https://assets.imgix.net/examples/womanlandscape.jpg?w=800&h=480&fit=crop&auto=format%2Cenhance&usm=20">
            </div>
            <p>第三張圖說</p>
        </div>
        <div>
            <div class="img-container">
                <img src="https://assets.imgix.net/unsplash/paperlamp.jpg?w=800&h=480&fit=crop&auto=format%2Cenhance&usm=20">
            </div>
            <p>第四張圖說</p>
        </div>
    </div>
    <!-- slider-nav end-->
</div>
```

## JQuery設定:round_pushpin:

### 關於slick按鈕的title語系

因應無障礙需求，在左右箭頭需要有替代文字，但往往因為網站有不同語系需求，因此按鈕需要呈現不同語言的替代文字，例如:

<<font color="#009ee7">html</font> lang="<font color="#EE428B">zh-Hant</font>">中按鈕會呈現<<font color="#009ee7">button</font> class="slick-prev" ... title="<font color="#EE428B">前一則</font>">Previous</button>或是
<<font color="#009ee7">html</font> lang="<font color="#EE428B">en</font>" >中按鈕會呈現或是<<font color="#009ee7">button</font> class="<font color="#EE428B">slick-prev</font>" ... title="<font color="#EE428B">previous</font>">Previous</button>，
此時無法用同一種語言因應各種語系，HyUI提供一組判斷語系之javascript設定，語系參照[W3C ISO Language Codes](https://www.w3schools.com/tags/ref_language_codes.asp)，可自行複製到各專案修改語系及對應之替代文字即可。注意：此程式並無預設放入 <font color="#EE428B">hyui.js</font>。

其中，程式是判斷語系字串中的前面字符作為判斷依據，目的是同一語系可能會有分支語系，但以開頭之語系英文字母做判斷。

## hyui.js 範例

```javascript=
//不同語系
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
```

## 輪播項目之索引標籤(點點)提示


需補充較詳細之提示文字，讓使用導讀軟體之使用者可以明確了解該元件之功能與用途，目前以 <font color="#EE428B">單張輪播</font> 修改。

<font color="#009ee7">在所需 slider 做 js 調整</font>

```javascript=
取文字
customPaging: function(slider, i) {
                var title = $(slider.$slides[i]).find('.title').html().trim();
                return $('<button type="button" aria-label="'+title+'"/>').text(title);
            }
      
取圖片的alt    
customPaging: function(slider, i) {
             var title = $(slider.$slides[i]).find('img').attr('alt').trim();
            return $('<button type="button" aria-label="'+title+'"/>').text(title);
            }
```
<font color="#009ee7">slick.js 修改拿掉</font>

![](https://i.imgur.com/ABKdv6Z.jpg)

<font color="#009ee7">slick.min.js 修改拿掉</font>

![](https://i.imgur.com/gZlbY5u.jpg)

















<style>
.ui-infobar{
max-width:95%;
}
.markdown-body{
max-width:95%;
}
</style>