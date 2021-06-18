# Tooltip 提示框（Lize）
###### tags: `HyUI` `Lize`

:::warning
檔案名稱：sass / element / <span class="focus2">_tooltip.scss</span>
:::
* 項目、文字的提示文字
```htmlmixed=
<span tooltip="上方的tooltop說明文字">上</span>
<span tooltip="左方的tooltop說明文字" flow="down">下</span>
<span tooltip="下方的tooltop說明文字" flow="left">左</span>
<span tooltip="右方的tooltop說明文字" flow="right">右</span>

<ul>
    <li>用中不新過不石<b tooltip="上方的tooltop說明文字">上方的tooltop</b>到各風講都給報</li>
    <li>用中不新過不石<b tooltip="下方的tooltop說明文字" flow="down">下方的tooltop</b>到各風講都給報</li>
    <li>用中不新過不石<b tooltip="左方的tooltop說明文字" flow="left">左方的tooltop</b>到各風講都給報</li>
    <li>用中不新過不石<b tooltip="右方的tooltop說明文字" flow="right">右方的tooltop</b>到各風講都給報</li>
</ul>
```

<iframe height="265" style="width: 100%;" scrolling="no" title="Tooltip / 提示框" src="https://codepen.io/Lize/embed/BaWvdMB?height=265&theme-id=dark&default-tab=html,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/Lize/pen/BaWvdMB'>Tooltip / 提示框</a> by Lize wu
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