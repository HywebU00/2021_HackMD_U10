# SASS 架構
###### tags: `HyUI` `Lize`

:::warning
SASS架構簡介：
全站的美容設計寶典。
詳細架構：[SASS架構（gitmind）](https://gitmind.com/app/doc/e332040020):arrow_right:
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

## 架構內容
1. **<span class="focus">[_variable.scss](#item-1):arrow_down:</span>**：全站樣式定義
3. **<span class="focus">[sass](#item-2):arrow_down:</span>**：模組
4. **<span class="focus">[page](#item-3):arrow_down:</span>**：特殊頁面
5. **<span class="focus">hyui.scss</span>**：將所需設定，從以上三項中 import 至 <span class="focus2">hyui.scss</span>，產出最終的CSS

![SASS架構](https://i.imgur.com/j5QimXA.png)

---

### <span class="title" id="item-1">_variable.scss</span>
:::warning
全站的基本定義，顏色、字型、格線系統
:::

<iframe height="265" style="width: 100%;" scrolling="no" title="_variable" src="https://codepen.io/Lize/embed/ExWaZXp?height=265&theme-id=dark&default-tab=css" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/Lize/pen/ExWaZXp'>_variable</a> by Lize wu
  (<a href='https://codepen.io/Lize'>@Lize</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

---
### <span class="title" id="item-2">sass</span>
:::warning
分成三個資料夾：共通 common、 元件 element、 模組 modual
詳細架構：[SASS架構（gitmind）](https://gitmind.com/app/doc/e332040020):arrow_right:
:::
#### <span class="sub-title">1、共通 common</span>
* <span class="focus">mixins 資料夾：</span>基礎物件設定或算式，內含 extend、mixin 設定。
* <span class="focus">網頁基本設定：</span>mediaquery、格線系統 grid、reset、瀏覽器修正...等。

<div class="box">
<h3>附加說明</h3>
<ol>
    <li><span class="focus2">客製MIXIN</span> 引用 <span class="focus">mixins 資料夾</span> 內的設定，引用項目依需求而定。</li>
    <li><span class="focus2">_grid</span> 引用 <span class="focus">mixins 資料夾</span> 的 <span class="focus2">_flex-set.scss</span> 設定</li>
    <li>hyui-flex 目前有 <span class="focus2">_bootstrap-grid</span> 與 <span class="focus2">_flex-set</span> 兩支格線系統。</li>
</ol>
</div>

---
*  [**<span class="focus">hyui flex extend / mixin 引用列表</span>**](/jf1_RTDUTVaQRlk3J1Gc1w?view) :arrow_right:
---

![共通](https://i.imgur.com/NFrmp4K.jpg)


#### <span class="sub-title">2、元件 element</span>
* 文字、語言、按鈕、麵包屑...等，共11組元件。

![元件](https://i.imgur.com/NaRpBj0.png)


#### <span class="sub-title">3、模組 modual</span>
* header、menu、固定側邊欄...等，目前共18個模組。

![模組2](https://i.imgur.com/Y50CqEg.png)


### <span class="title" id="item-3">page</span>
:::warning
客製（mp）、固定應用（cp、sitemap...等）頁面。
新增的樣式，建議寫入 <span class="focus2">_template</span> 
:::

![頁面](https://i.imgur.com/b7xN6WA.png)
