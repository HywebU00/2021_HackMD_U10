# hr & divider
###### tags: `HyUI` `Lize`

:::warning
檔案名稱：sass / element / <span class="focus2">_divider.scss</span>
:::

* <span class="focus">hr</span>：分隔線
* <span class="focus">divider</span>：<div class="focus2">必須置入文字</div>的水平、垂直分隔線，無置入文字將無法顯示
* hr、divider 兩者皆內置<div class="focus2">.clearfix</div>清除浮動的設定

```htmlmixed=
<hr>
<div class="divider">水平分隔線</div>
<div class="divider-vertical">垂直分隔線</div>
```

<iframe height="500" style="width: 100%;" scrolling="no" title="hr &amp; divider / 分隔線" src="https://codepen.io/Lize/embed/PopLJgw?height=265&theme-id=dark&default-tab=css,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/Lize/pen/PopLJgw'>hr &amp; divider / 分隔線</a> by Lize wu
  (<a href='https://codepen.io/Lize'>@Lize</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

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