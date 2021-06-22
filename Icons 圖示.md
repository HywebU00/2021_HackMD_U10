# Icons / 圖示
###### tags: `HyUI` `Lize`

:::warning
檔案名稱：sass / element / <span class="focus2">_icon.scss</span>
:::

* hyUI提供一套可快速套用的icon圖示，與<span class="focus2">@font face</span>差別在於，本圖示是用<span class="focus2">svg</span>呈現，非網路字型技術。
* icon 預設黑色，反白的icon檔名後加<span class="focus2">2</span>，例如：<span class="focus2">i_search</span>為黑色icon，<span class="focus2">i_search2</span>為白色icon
* 彩色 icon 1組 ; 黑色、白色 icon 各47組。
* svg icon 反白效果，可使用css濾鏡<span class="focus2"> filter 的 invert </span>設定。
* 如果想要改變icon的顏色、透明度、對比、亮度...等設定，可參考[CSS filter圖片濾鏡]([https://](https://www.w3schools.com/cssref/css3_pr_filter.asp))。<span class="focus">但ie不支援 filter</span>。
* 之後再補充 function share 的社群 icon
<!-- * icon 顏色反白加入 class name<span class="focus2">.invert</span>，使用濾鏡 filter 的 invert 設定，<span class="focus">但ie不支援 filter</span>，只能等ie死透再考慮使用 -->

<iframe height="500" style="width: 100%;" scrolling="no" title="Icons / 圖示" src="https://codepen.io/Lize/embed/JjWVwmX?height=265&theme-id=dark&default-tab=html,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/Lize/pen/JjWVwmX'>Icons / 圖示</a> by Lize wu
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