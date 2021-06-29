# Table / 表格
###### tags: `HyUI`
:::warning
檔案名稱：sass / modual / <span class="focus2">_table.scss</span>
:::
1. **<span class="focus">[基本表格樣式](#item-1):arrow_down:</span>**
2. **<span class="focus">[支援響應式條列式重新排版表格](#item-2):arrow_down:</span>**
3. **<span class="focus">[固定左邊表頭，資料可水平捲動](#item-3):arrow_down:</span>**

---



## <span style="font-size:2em;margin-right:.2em;color:#21BAFF;" id="item-1">01. </span>基本表格樣式

<iframe height="300" style="width: 100%;" scrolling="no" title="基本表格樣式" src="https://codepen.io/u00hyui/embed/PomoQLj?defaultTab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/PomoQLj">
  基本表格樣式</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

```html=
<table>
  <thead>
    <tr>
      <th>...</th>
      <th>...</th>
      <th>...</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
  </tbody>
</table>
```

### td有hover效果

table加上<span class="focus3">table_hover</span>的classname

<iframe height="300" style="width: 100%;" scrolling="no" title="基本表格樣式 - td有hover效果" src="https://codepen.io/u00hyui/embed/mdmdLgN?defaultTab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/mdmdLgN">
  基本表格樣式 - td有hover效果</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

```html=
<table class="table_hover">
```

### td有間隔不同背景色

table加上<span class="focus3">table_sprite</span>的classname

<iframe height="350" style="width: 100%;" scrolling="no" title="基本表格樣式 - td有間隔不同背景色" src="https://codepen.io/u00hyui/embed/zYwYJOo?defaultTab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/zYwYJOo">
  基本表格樣式 - td有間隔不同背景色</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>


```html=
<table class="table_sprite">
```

### 範例：一般內容式表格

<iframe height="300" style="width: 100%;" scrolling="no" title="範例：一般內容式表格" src="https://codepen.io/u00hyui/embed/poPoOvv?defaultTab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/poPoOvv">
  範例：一般內容式表格</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

--- 

## <span style="font-size:2em;margin-right:.2em;color:#21BAFF;" id="item-2">02. </span>支援響應式條列式重新排版表格

使用<span class="focus3">before</span>取代<span class="focus3">th</span>，在<span class="focus3">table</span>上一層使用<span class="focus">**`<div class="table_list"></div>`**</span>將<span class="focus3">table</span>包覆住，即可於手機版重新排版表格樣式。

<iframe height="500" style="width: 100%;" scrolling="no" title="響應式條列式重新排版表格" src="https://codepen.io/u00hyui/embed/eYWYLNz?defaultTab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/eYWYLNz">
  響應式條列式重新排版表格</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

```html=
<div class="table_list">
    <table>
      <thead>
        <tr>
          <th>編號</th>
          <th>據點</th>
          <th>地址</th>
          <th>電話</th>
          <th>傳真</th>
          <th>信箱</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>01</td>
          <td>...</td>
          <td>...</td>
          <td>...</td>
          <td>...</td>
          <td>...</td>
        </tr>
        <tr>
          <td>02</td>
          <td>...</td>
          <td>...</td>
          <td>...</td>
          <td>...</td>
          <td>...</td>
        </tr>
        <tr>
          <td>03</td>
          <td>...</td>
          <td>...</td>
          <td>...</td>
          <td>...</td>
          <td>...</td>
        </tr>
      </tbody>
    </table>
</div>
```

## <span style="font-size:2em;margin-right:.2em;color:#21BAFF;" id="item-3">03. </span>固定左邊表頭，資料可水平捲動

適用於左側有<span class="focus3">th</span>的資料，在手機版可做成固定<span class="focus3">th</span>，其餘td可橫向水平捲動，在<span class="focus3">table</span>最外層請用<span class="focus3">fix_th_tablediv</span>包覆。

<iframe height="300" style="width: 100%;" scrolling="no" title="固定左邊表頭，資料可水平捲動表格" src="https://codepen.io/u00hyui/embed/GRmRXqw?defaultTab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/GRmRXqw">
  固定左邊表頭，資料可水平捲動表格</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

```html=
<div class="fix_th_table">
    <table>
        <tr>
            <th>th 1</th>
            <th>th 2</th>
            <th>th 3</th>
            <th>th 4</th>
            <th>th 5</th>
            <th>th 6</th>
        </tr>
        <tr>
            <th>th A</th>
            <td>td 資料</td>
            <td>td 資料</td>
            <td>td 資料</td>
            <td>td 資料</td>
            <td>td 資料</td>
        </tr>
        <tr>
            <th>th B</th>
            <td>td 資料</td>
            <td>td 資料</td>
            <td>td 資料</td>
            <td>td 資料</td>
            <td>td 資料</td>
        </tr>
        <tr>
            <th>th C</th>
            <td>td 資料</td>
            <td>td 資料</td>
            <td>td 資料</td>
            <td>td 資料</td>
            <td>td 資料</td>
        </tr>
    </table>
</div>
```
## JQuery設定:round_pushpin:
按照專案經驗，在客戶資料上稿常常出現表格會撐出畫面或是破圖的情況，這部分可以使用預設提供之JQuery設定，讓文章內容頁面的表格自動產生響應式橫向捲軸，以防止畫面跑版。<br/>
目前判斷如果<span class="focus3">table</span>父層沒有<span class="focus3">.tablie_list</span>或是<span class="focus3">.fix_th_table</span>的table，一律在<span class="focus">寬度小於545px</span>時，<span class="focus3">table</span>套用<span class="focus3">scroltable();</span>的外掛
```javascript=
/*------------------------------------*/
///////table 加上響應式 scroltable-wrapper/////
//*------------------------------------*/
$('table').each(function(index, el) {
    //判斷沒有table_list
    if ($(this).parents('.table_list').length == 0 && $(this).parents('.fix_th_table').length == 0) {
        $(this).scroltable();
    }
});
// tablearrow arrow，為了設定箭頭
$('.scroltable-nav-left').append('<div class="tablearrow_left" style="display:none;"></div>');
$('.scroltable-nav-right').append('<div class="tablearrow_right"  style="display:none;"></div>');
// 固定版頭
function table_Arrow() {
    if ($('table').parents('.table_list').length == 0 && $('table').parents('.fix_th_table').length == 0) {
        if ($('.scroltable-wrapper').length > 0) {
            var stickyArrowTop = Math.floor($('.scroltable-wrapper').offset().top),
                thisScroll = Math.floor($(this).scrollTop());
            if (thisScroll > stickyArrowTop - 230) {
                $('.scroltable-wrapper .tablearrow_left').css('display', 'block');
                $('.scroltable-wrapper .tablearrow_left').css({ "top": thisScroll - stickyArrowTop + 220 }, 100, 'easeOutQuint');
                $('.scroltable-wrapper .tablearrow_right').css('display', 'block');
                $('.scroltable-wrapper .tablearrow_right').css({ "top": thisScroll - stickyArrowTop + 220 }, 100, 'easeOutQuint');
            } else {
                $('.scroltable-wrapper .tablearrow_left').css({
                    top: '10px',
                    display: 'none'
                });
                $('.scroltable-wrapper .tablearrow_right').css({
                    top: '10px',
                    display: 'none'
                });
            }
        }
    }
}
$(window).scroll(function(event) {
    table_Arrow();
});
// /*------------------------------------*/
// //////////table 加上 data-title//////////
// /*------------------------------------*/
function rwdTable() {
    $('.table_list').find('table').each(function() {
        var $row = $(this).find('tr');
        rowCount = $row.length;
        for (var n = 1; n <= rowCount; n++) {
            $(this).find('th').each(function(index) {
                var thText = $(this).text();
                $row.eq(n).find('td').eq(index).attr('data-title', thText);
            });
        }
    });
}
rwdTable();
```

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
    color: #222; 
    border: solid 1px #c8c8c8;
    display: inline-block;
    padding: 2px 10px; margin: 0 4px;
    border-radius: 4px;
    background: #fff;
}
.focus3{
    display: inline-block;
    background: #f1f1f1;
    padding: 0.1em 0.8em;
    border: 1px solid #f1f1f1;
    margin: 0px 5px;
    line-height: 1.35em;
    border-radius: 4px;
    color: #B20050;
    margin-top: 2px;
    font-size: 15px;
    font-weight: bold;
}
.link{ font-size: 20px; color: #B20050;}
.ui-infobar{ max-width:95%; }
.markdown-body{ max-width:95%; }
</style>