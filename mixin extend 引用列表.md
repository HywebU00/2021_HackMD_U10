# mixin / extend 引用列表

[![hackmd-github-sync-badge](https://hackmd.io/jf1_RTDUTVaQRlk3J1Gc1w/badge)](https://hackmd.io/jf1_RTDUTVaQRlk3J1Gc1w)


###### tags: `HyUI` `切切切`
## <font color=purple> extend </font>
### extend
:::warning
原始設定：../sass/common/mixins/<span class="focus2">_extend.scss</span>
:::
```sass=
// 繼承
@extend %slash;              // 斜線
@extend %arrow_setting;      // 箭頭
@extend %arrow_down;         // 箭頭：下
@extend %arrow_right;        // 箭頭：右
@extend %arrow_up;           // 箭頭：上
@extend %arrow_left;         // 箭頭：左
@extend %clearfix;           // 清除浮動
@extend %flex_set;           // 啟動 display:flex
```
## <font color=purple> mixin </font>
### 1、瀏覽器斷點
:::warning
原始設定：../sass/common/mixins/<span class="focus2">_mediaquery.scss</span>
:::
```sass=
@include screen('desktop'){}            // min-width: 1400px
@include screen('notebook'){}           // max-width: 1399px
@include screen('tablet'){}             // max-width: 991px
@include screen('mobile'){}             // max-width: 767px
@include screen('xs_mobile'){}          // max-width: 575px
```
### 2、格線系統
#### 2-1 bootstrap 格線系統
:::warning
原始設定：：../sass/common/mixins/<span class="focus2">_bootstrap-grid.scss</span>
:::
```sass=
.col{
    @include make-xs-column(12);              // xs_mobile
    @include make-sm-column(6);               // mobile
    @include make-md-column(3);               // tablet
    @include make-lg-column(3);               // desktop
    @include gutter();                        // 容器內距 padding
}
```
#### 2-2 flex 格線系統
:::warning
原始設定：../sass/common/mixins/<span class="focus2">_flex-grid.scss</span>


使用 flex 分割欄位，有兩種分割方式：
1、均分：每欄 <b class="focus">欄寬都相同</b>
2、自由分配：每欄 <b class="focus">欄寬不相同，加總等於12</b>。

[『均分』、『自由分配』的算式原理](https://hackmd.io/@lizewu/r1eU6MPBw) :arrow_right:
:::

```sass=
// step 0、設定 flex 的 margin gutter
$m-gutter: 4px;

// 均分 equal    
.papa{
    // step 1、父層設定：
    // 1. display: flex;
    // 2. flex-flow: row wrap;
    // 3. justify-content: space-between;
    @extend %flex_set;

    // step 2、子層設定：欄數、margin gutter
    // margin、padding，務必加上『單位』才能計算！   
    .col{
        @include flex-xs-equal(1, 0px);
        @include flex-sm-equal(2, $m-gutter);
        @include flex-md-equal(2, $m-gutter);
        @include flex-lg-equal(2, $m-gutter);
        @include gutter();
    }
}

// 自由搭配
.flex-8-4{
    @extend %flex_set;
    .col{
        @include flex-xs(12, 0px);
        @include flex-sm(6, $m-gutter);
        @include flex-md(8, $m-gutter);
        @include flex-lg(8, $m-gutter);
        @include gutter();

        &:nth-child(2){
            @include flex-xs(12, 0px);
            @include flex-sm(6, $m-gutter);
            @include flex-md(4, $m-gutter);
            @include flex-lg(4, $m-gutter);
        }
    }
}

```
### 3、漸層
:::warning
原始設定：：../sass/common/mixins/<span class="focus2">_gradient.scss</span>
:::
```sass=
@include gradient(#07c, #06f, vertical);      // 水平
@include gradient(#07c, #06f, horizontal);    // 垂直
@include gradient(#07c, #06f, diagonal);      // 對角線
@include gradient(#07c, #06f, circle);        // 圓形
```
### 4、文字刪節號
:::warning
原始設定：：../sass/common/mixins/<span class="focus2">_text-overflow.scss</span>
:::
```sass=
@include text-overflow;                        // 單行
@include text-line(2,23px);                    // 多行（行數、行高）
```
### 5、清除 li 格式
:::warning
原始設定：：../sass/common/mixins/<span class="focus2">_li-reset.scss</span>
:::
```sass=
@include li-reset;                            // 清除li預設
@include img-responsive;                      // 圖片
```
### 6、圖片比例
:::warning
原始設定：../sass/common/mixins/<span class="focus2">_image.scss</span>
:::
```sass=
@include aspect-ratio(4,3);                   // 圖片比例，4:3
```

<div class="box">
    <h3>附加說明</h3>
    <ol>
        <li>上述檔案，全部引用至../sass/common/<span class="focus2">_mixin.scss</span></li>
</ol>
</div>


<style>
/* 顏色設定 <span class="blue"></span>*/
.title{
    font-size: 26px; color: #fff;
    background:#00469C; display:inline-block;
    padding: 10px 20px 10px 30px;
    border-radius: 4px;
}
.sub-title{ font-size: 20px; color: #00469C; }
.box{
    padding: 1em 2em;
    background:#f5f5f5;
    margin: 10px 0;
    border: solid 1px #aaa;
}

.focus { color: #B20050; }
.focus2 {
    color: #222; border: solid 1px #c8c8c8;
    display: inline-block;
    padding: 2px 10px; margin: 0 4px;
    border-radius: 4px;
    background: #fff;
}
.link{ font-size: 20px; color: #B20050;}
.ui-infobar{ max-width:95%; }
.markdown-body{ max-width:95%; }
</style>