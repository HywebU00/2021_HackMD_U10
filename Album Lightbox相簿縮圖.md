# Album+Lightbox/相簿(縮圖)列表+燈箱

###### tags: `HyUI`

檔案名稱：sass/common/_grid.scss
檔案名稱：sass/modual/_thumbnail.scss


HyUI使用<font color="#009ee7"> fancybox </font>的燈箱套件，目前hyUI <font color="#EE428B"> vendor </font>內含<font color="#EE428B"> fancybox </font>已經有加入客製化設定，如需要最新版，請到 [fancybox](https://fancyapps.com/fancybox/3/docs/#usage) 官網參考下載。

## 匯入外掛fancybox CSS
```htmlmixed=
 <!-- 燈箱facybox -->
    <link rel="stylesheet" type="text/css" href="vendor/facybox/dist/jquery.fancybox.min.css">
```
## 匯入外掛fancybox js
```htmlmixed=
<!-- 燈箱facybox -->
    <script src="vendor/facybox/dist/jquery.fancybox.min.js"></script>
```

此為相簿列表模組示範範例。當相簿需要觸發的連結區塊，以及燈箱區塊設定放大瀏覽照片時，
請將<font color="#009ee7"> 圖片連結 </font>寫入 <font color="#EE428B">href</font> 裡，並在<font color="#EE428B">a </font>裡加上，<font color="#009ee7">data-fancybox</font> 及 <font color="#009ee7">data-caption</font>



<iframe height="550" style="width: 100%;" scrolling="no" title="Album+Lightbox/相簿列表+燈箱" src="https://codepen.io/u00hyui/embed/abprJKj?height=265&theme-id=dark&default-tab=html,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/u00hyui/pen/abprJKj'>Album+Lightbox/相簿列表+燈箱</a> by u00hyui
  (<a href='https://codepen.io/u00hyui'>@u00hyui</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>


## HTML範本

```htmlmixed=
<!-- grid:flex -->
<section class="flex-equal-3">
    <div class="container">
        <div class="Flex-set">
            <div class="thumbnail">
                <a href="images/demo/01.jpg" data-fancybox="images" data-caption="第1張圖說">
                    <div class="img-container">
                        <picture>
                            <source media="(min-width: 1200px)" data-srcset="images/demo/01.jpg">
                            <source media="(min-width: 992px)" data-srcset="images/demo/01.jpg">
                            <source media="(min-width: 576px)" data-srcset="images/demo/01.jpg">
                            <source media="(max-width: 575px)" data-srcset="images/demo/01.jpg">
                            <img data-src="images/demo/01.jpg" class="lazy">
                            <noscript><img src="images/demo/01.jpg"></noscript>
                        </picture>
                    </div>
                    <div class="caption">
                        <time>2018-01-01</time>
                        <h3>標題</h3>
                        <p>內文</p>
                    </div>
                </a>
            </div>
            <div class="thumbnail">
                <a href="images/demo/02.jpg" data-fancybox="images" data-caption="第2張圖說">
                    <div class="img-container">
                        <picture>
                            <source media="(min-width: 1200px)" data-srcset="images/demo/02.jpg">
                            <source media="(min-width: 992px)" data-srcset="images/demo/02.jpg">
                            <source media="(min-width: 576px)" data-srcset="images/demo/02.jpg">
                            <source media="(max-width: 575px)" data-srcset="images/demo/02.jpg">
                            <img data-src="images/demo/02.jpg" class="lazy">
                            <noscript><img src="images/demo/02.jpg"></noscript>
                        </picture>
                    </div>
                    <div class="caption">
                        <time>2018-01-01</time>
                        <h3>標題</h3>
                        <p>內文</p>
                    </div>
                </a>
            </div>
            <div class="thumbnail">
                <a href="images/demo/03.jpg" data-fancybox="images" data-caption="第3張圖說">
                    <div class="img-container">
                        <picture>
                            <source media="(min-width: 1200px)" data-srcset="images/demo/03.jpg">
                            <source media="(min-width: 992px)" data-srcset="images/demo/03.jpg">
                            <source media="(min-width: 576px)" data-srcset="images/demo/03.jpg">
                            <source media="(max-width: 575px)" data-srcset="images/demo/03.jpg">
                            <img data-src="images/demo/03.jpg" class="lazy">
                            <noscript><img src="images/demo/03.jpg"></noscript>
                        </picture>
                    </div>
                    <div class="caption">
                        <time>2018-01-01</time>
                        <h3>標題</h3>
                        <p>內文</p>
                    </div>
                </a>
            </div>
        </div>
    </div>
</section>
```

# Thumbnail / 卡片式縮圖 範例

<iframe height="550" style="width: 100%;" scrolling="no" title="" src="https://codepen.io/u00hyui/embed/MWpMRJQ?defaultTab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/MWpMRJQ">
  </a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

## HTML範本

```htmlmixed=
<section class="flex-equal-3">
  <div class="container">
    <div class="Flex-set">
      <div class="thumbnail">
        <a href="images/demo/01.jpg" data-fancybox="images" data-caption="第1張圖說">
          <div class="img-container">
            <picture>
              <source media="(min-width: 1200px)" data-srcset="images/demo/01.jpg">
              <source media="(min-width: 992px)" data-srcset="images/demo/01.jpg">
              <source media="(min-width: 576px)" data-srcset="images/demo/01.jpg">
              <source media="(max-width: 575px)" data-srcset="images/demo/01.jpg">
              <img src="images/demo/01.jpg">
              <noscript><img src="images/demo/01.jpg"></noscript>
            </picture>
          </div>
        </a>
        <div class="caption">
          <time>2018-01-01</time>
          <h3>標題</h3>
        </div>
        <hr>
        <div class="btn_grp">
          <button class="btn">按鈕</button>
        </div>
      </div>
      <div class="thumbnail">
        <a href="images/demo/02.jpg" data-fancybox="images" data-caption="第2張圖說">
          <div class="img-container">
            <picture>
              <source media="(min-width: 1200px)" data-srcset="images/demo/02.jpg">
              <source media="(min-width: 992px)" data-srcset="images/demo/02.jpg">
              <source media="(min-width: 576px)" data-srcset="images/demo/02.jpg">
              <source media="(max-width: 575px)" data-srcset="images/demo/02.jpg">
              <img src="images/demo/02.jpg">
              <noscript><img src="images/demo/02.jpg"></noscript>
            </picture>
          </div>
        </a>
        <div class="caption">
          <time>2018-01-01</time>
          <h3>標題</h3>
        </div>
        <hr>
        <div class="btn_grp">
          <button class="btn">按鈕</button>
        </div>
      </div>
      <div class="thumbnail">
        <a href="images/demo/03.jpg" data-fancybox="images" data-caption="第3張圖說">
          <div class="img-container">
            <picture>
              <source media="(min-width: 1200px)" data-srcset="images/demo/03.jpg">
              <source media="(min-width: 992px)" data-srcset="images/demo/03.jpg">
              <source media="(min-width: 576px)" data-srcset="images/demo/03.jpg">
              <source media="(max-width: 575px)" data-srcset="images/demo/03.jpg">
              <img src="images/demo/03.jpg">
              <noscript><img src="images/demo/03.jpg"></noscript>
            </picture>
          </div>
        </a>
        <div class="caption">
          <time>2018-01-01</time>
          <h3>標題</h3>
        </div>
        <hr>
        <div class="btn_grp">
          <button class="btn">按鈕</button>
        </div>
      </div>
    </div>
  </div>
</section>
```

<style>
.ui-infobar{
max-width:95%;
}
.markdown-body{
max-width:95%;
}
</style>
