# Bootstrap grid system

###### tags: `HyUI`
## <font color="#EE428B">一般情況下，請盡量不使用Bootstrap之格線系統，期望網站開發者於tag放置有語意之class名稱。</font>
bootstrap是一個基本的響應式網頁格線，他有兩個基本概念，第一個概念是把一個 <font color="#009ee7">網頁分為12欄</font>，第二個概念就是斷點(breakpoint)，bootstrap已經先把裝置尺寸分為四類分別是 <font color="#009ee7">XS</font>、 <font color="#009ee7">SM</font> 、 <font color="#009ee7">MD</font> 、 <font color="#009ee7">LG</font> ，而HyUI預設提供使用 bootstrap 3 float的格線系統，建立完成基本的格線。
:::warning
格線系統：以<span class="focus2">float</span>為計算基礎，主要功能是分割欄位。
檔案名稱：sass / common / <span class="focus2">_grid.scss</span>
:::

<style>
/* 顏色設定 <span class="blue"></span>*/

.focus2 {
    color: #222; border: solid 1px #c8c8c8;
    display: inline-block;
    padding: 2px 10px; margin: 0 4px;
    border-radius: 4px;
    background: #fff;
}

</style>


## HTML範本
<iframe height="1000" style="width: 100%;" scrolling="no" title="" src="https://codepen.io/u00hyui/embed/ZEKEYxJ?defaultTab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/ZEKEYxJ">
  </a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>


## scss範本
```sass=
// _grid.scss

// 單欄
.col-12 {}
// 兩欄 6-6
.col-6-6 {
    .col {
        @include make-xs-column(12);
        @include make-sm-column(6);
        @include make-md-column(6);
        @include make-lg-column(6);
    }
}
// 三欄 4-4-4
.col-4-4-4 {
    .col {
        @include make-xs-column(12);
        @include make-sm-column(4);
        @include make-md-column(4);
        @include make-lg-column(4);
    }
}
// 四欄 3-3-3
.col-3-3-3-3 {
    .col {
        @include make-xs-column(12);
        @include make-sm-column(6);
        @include make-md-column(3);
        @include make-lg-column(3);
    }
}
// 雙欄 8-4
.col-8-4 {
    .col {
        @include make-xs-column(12);
        @include make-sm-column(8);
        @include make-md-column(8);
        @include make-lg-column(8);
    }
    .col:nth-of-type(2n) {
        @include make-xs-column(12);
        @include make-sm-column(4);
        @include make-md-column(4);
        @include make-lg-column(4);
    }
}
// 雙欄 4-8
.col-4-8 {
    .col {
        @include make-xs-column(12);
        @include make-sm-column(4);
        @include make-md-column(4);
        @include make-lg-column(4);
    }
    .col:nth-of-type(2n) {
        @include make-xs-column(12);
        @include make-sm-column(8);
        @include make-md-column(8);
        @include make-lg-column(8);
    }
}
// 六欄 2-2-2-2-2-2
.col-2-2-2-2-2-2 {
    .col {
        @include make-xs-column(6);
        @include make-sm-column(2);
        @include make-md-column(2);
        @include make-lg-column(2);
    }
}
// 進階設定：自行命名
.cssname {
    .news {
        @include make-xs-column(12);
        @include make-sm-column(8);
        @include make-md-column(8);
        @include make-lg-column(8);
    }
    .video {
        @include make-xs-column(12);
        @include make-sm-column(4);
        @include make-md-column(4);
        @include make-lg-column(4);
    }
}
// 進階設定：非均等欄位
.col-3-6-3 {
    .col {
        @include make-xs-column(12);
        @include make-sm-column(3);
        @include make-md-column(3);
        @include make-lg-column(3);
        &:nth-child(2) {
            @include make-xs-column(12);
            @include make-sm-column(6);
            @include make-md-column(6);
            @include make-lg-column(6);
        }
    }
}
// 進階設定：五欄
.col-5 {
    .col {
        @include make-xs-column(12);
        @include make-sm-column(2);
        @include make-md-column(2);
        @include make-lg-column(2);
        &:first-child {
            @include make-xs-column-offset(0);
            @include make-sm-column-offset(1);
            @include make-md-column-offset(1);
            @include make-lg-column-offset(1);
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