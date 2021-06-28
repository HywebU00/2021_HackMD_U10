# Flex grid system
###### tags: `HyUI` `Lize`

:::warning
格線系統：以<span class="focus2">flex</span>為計算基礎，主要功能是分割欄位。
檔案名稱：sass / common / <span class="focus2">_grid-flex.scss</span>
:::

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
<!-- ## 標題
:::warning
簡介
:::
```sass=
.a{
    text-align: center;
}
```
```htmlmixed=
<a>123</a>
``` -->
## flex grid system
flex grid system 分割方式有兩種：
1. 『<span class="focus">[均分（equal）](#item-1):arrow_down:</span>』
2. 『<span class="focus">[自由分配](#item-2):arrow_down:</span>』
3. 『<span class="focus">[混合運用](#item-3):arrow_down:</span>』


### <span class="title" id="item-1">均分（equal）</span>
:::warning
每欄<b class="focus">欄寬都相同</b>，目前預設2-12欄均分，未來可能會調降最多欄數。

算式：<span class="focus2">100% ÷ 欄數</span>
:::

```sass=
// step 0、設定共用的 margin gutter
$m-gutter: 4px;

.papa{
    // step 1、父層啟動flex
    @extend %flex_set;
    
    // step 2、子層設定欄寬，可設定斷點
    .col{
        @include flex-xs-equal(1, 0px);
        @include flex-sm-equal(2, $m-gutter);
        @include flex-md-equal(4, $m-gutter);
        @include flex-lg-equal(8, $m-gutter);
        @include gutter();
    }
}
```
<iframe height="500" style="width: 100%;" scrolling="no" title="flex grid system equal" src="https://codepen.io/u00hyui/embed/dyWyGar?defaultTab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/dyWyGar">
  flex grid system equal</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

---
### <span class="title" id="item-2">自由分配</span>
:::warning
每欄<b class="focus">欄寬不相同，加總等於12</b>。
可應用在<span class="focus2">3+9</span>、<span class="focus2">4+8</span>、<span class="focus2">5+7</span>、<span class="focus2">3+6+3</span>    ...等非均分的分割。
算式：<span class="focus2">(100% ÷ 12) × 欄數</span>
:::

```sass=
// step 0、設定共用的 margin gutter
$m-gutter: 4px;

.flex-8-4{
    // step 1、父層啟動flex
    @extend %flex_set;
    
    // step 2、子層設定欄寬，可設定斷點
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
<iframe height="500" style="width: 100%;" scrolling="no" title="flex grid system" src="https://codepen.io/u00hyui/embed/abWbdeR?defaultTab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/abWbdeR">
  flex grid system</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

---
### <span class="title" id="item-3">混合運用</span>
:::warning
均分Ｘ自由分配
:::

```sass=
// step 0、設定共用的 margin gutter
$m-gutter: 4px;

// 綜合
.mix-equal-2{
    .Flex-set{
        // step 1、父層啟動flex
        @extend %flex_set;
        // step 2、子層設定欄寬，可設定斷點
        .col{
            @include flex-xs-equal(1, 0px);
            @include flex-sm-equal(2, $m-gutter);
            @include flex-md-equal(2, $m-gutter);
            @include flex-lg-equal(2, $m-gutter);
            padding: 1em;
        }
    }

    .inner-4-8{
        // step 1、父層啟動flex
        @extend %flex_set;
        // step 2、子層設定欄寬，可設定斷點
        div{
            @include flex-xs(12, 0px);
            @include flex-sm(4, $m-gutter);
            @include flex-md(4, $m-gutter);
            @include flex-lg(4, $m-gutter);

            &:last-child{
                @include flex-xs(12, 0px);
                @include flex-sm(8, $m-gutter);
                @include flex-md(8, $m-gutter);
                @include flex-lg(8, $m-gutter);
            }
        }
    }
}
```
<iframe height="500" style="width: 100%;" scrolling="no" title="flex grid system mix" src="https://codepen.io/u00hyui/embed/eYWYZZK?defaultTab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/eYWYZZK">
  flex grid system mix</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

<div class="box">
    <h3>附加說明</h3>
    <ol>
        <li>二個數值代表順序為：<span class="focus2">欄數</span>、<span class="focus2">margin gutter</span></li>
        <li>數值後面，<span class="focus">務必加上單位（%、px、em）</span>，數值為『0』一樣要加單位。</li>
    <li>margin gutter的數值是<span class="focus2">雙側的總和</span>，</br>例如：$m-gutter: 20px，欄寬左右各扣除10px，以<span class="focus2">space-between</span>達成對齊的效果</li>
    <li>flex grid算式複雜，須配合斷點更改欄數，故 flex grid 的斷點採用<span class="focus2">min-width</span>，極小尺寸為<span class="focus2"><span class="focus">screen-xs-flex: 320px</span></span></li>
</ol>
</div>

