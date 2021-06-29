# Forms / 表單

###### tags: `HyUI`

:::warning
檔案名稱：sass / modual / <span class="focus2">_form.scss</span>
:::

1. **<span class="focus">[文字表單](#item-1):arrow_down:</span>**
2. **<span class="focus">[核取與單選](#item-2):arrow_down:</span>**
3. **<span class="focus">[下拉選單](#item-3):arrow_down:</span>**
4. **<span class="focus">[檔案瀏覽 or 上傳檔案](#item-4):arrow_down:</span>**
5. **<span class="focus">[有icon的input](#item-5):arrow_down:</span>**
6. **<span class="focus">[表單排版範例](#item-6):arrow_down:</span>**

---

注意 :zap: 
* 表單外層以 <span class="focus">**`<div class="flex-form"></div>`**</span>包覆，css<span class=focus>不寫在<form></span>上
* 為符合無障礙標準須加上<span class="focus">**`<label></label>`**</span>，但是不想要在畫面上出現文字時，加上classname  <span class="focus3">**label_hidden**</span>隱藏label文字

---

## <span style="font-size:2em;margin-right:.2em;color:#21BAFF;" id="item-1">01. </span>文字表單

### 預設文字表單
<iframe height="200" style="width: 100%;" scrolling="no" title="預設文字表單" src="https://codepen.io/u00hyui/embed/KKWLymN?defaultTab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/KKWLymN">
  預設文字表單</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

### 預設密碼表單
<iframe height="200" style="width: 100%;" scrolling="no" title="預設密碼表單" src="https://codepen.io/u00hyui/embed/QWpRQQX?defaultTab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/QWpRQQX">
  預設密碼表單</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

### 預設組合範例
<iframe height="350" style="width: 100%;" scrolling="no" title="預設組合範例" src="https://codepen.io/u00hyui/embed/KKWLQbw?defaultTab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/KKWLQbw">
  預設組合範例</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

### 預設組合範例 - 行內設定

加上Classname<span class="focus3">form_inline</span>設定行內樣式

<iframe height="300" style="width: 100%;" scrolling="no" title="預設組合範例 - 行內設定" src="https://codepen.io/u00hyui/embed/zYZQWOz?defaultTab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/zYZQWOz">
  預設組合範例 - 行內設定</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

### 多行文字表單
<iframe height="250" style="width: 100%;" scrolling="no" title="多行文字表單" src="https://codepen.io/u00hyui/embed/WNpBJRX?defaultTab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/WNpBJRX">
  多行文字表單</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

### 多行文字表單 - 行內設定
<iframe height="200" style="width: 100%;" scrolling="no" title="多行文字表單 - 行內設定" src="https://codepen.io/u00hyui/embed/ZEeNoeq?defaultTab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/ZEeNoeq">
  多行文字表單 - 行內設定</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

## <span style="font-size:2em;margin-right:.2em;color:#21BAFF;" id="item-2">02. </span>核取與單選

### 預設核取方塊
<iframe height="200" style="width: 100%;" scrolling="no" title="預設核取方塊" src="https://codepen.io/u00hyui/embed/LYWKMMY?defaultTab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/LYWKMMY">
  預設核取方塊</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

### 預設核取方塊 - 行內設定
<iframe height="200" style="width: 100%;" scrolling="no" title="預設核取方塊 - 行內設定" src="https://codepen.io/u00hyui/embed/RwpzOrb?defaultTab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/RwpzOrb">
  預設核取方塊 - 行內設定</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

### 預設單選方塊
<iframe height="200" style="width: 100%;" scrolling="no" title="預設單選方塊" src="https://codepen.io/u00hyui/embed/MWpMRwE?defaultTab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/MWpMRwE">
  預設單選方塊</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

### 預設單選方塊 - 行內設定
<iframe height="200" style="width: 100%;" scrolling="no" title="預設單選方塊 - 行內設定" src="https://codepen.io/u00hyui/embed/BaWgEKK?defaultTab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/BaWgEKK">
  預設單選方塊 - 行內設定</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

## <span style="font-size:2em;margin-right:.2em;color:#21BAFF;" id="item-3">03. </span>下拉選單

<iframe height="200" style="width: 100%;" scrolling="no" title="下拉選單" src="https://codepen.io/u00hyui/embed/zYZVXqa?defaultTab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/zYZVXqa">
  下拉選單</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

### 下拉選單 - 行內設定
<iframe height="200" style="width: 100%;" scrolling="no" title="下拉選單 - 行內設定" src="https://codepen.io/u00hyui/embed/MWpMRer?defaultTab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/MWpMRer">
  下拉選單 - 行內設定</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

## <span style="font-size:2em;margin-right:.2em;color:#21BAFF;" id="item-4">04. </span>檔案瀏覽 or 上傳檔案

### 單個檔案上傳
<iframe height="200" style="width: 100%;" scrolling="no" title="單個檔案上傳" src="https://codepen.io/u00hyui/embed/ExWBJge?defaultTab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/ExWBJge">
  單個檔案上傳</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

### 多個檔案上傳
<iframe height="200" style="width: 100%;" scrolling="no" title="多個檔案上傳" src="https://codepen.io/u00hyui/embed/MWpMRpQ?defaultTab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/MWpMRpQ">
  多個檔案上傳</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>


## JQuery設定:round_pushpin:
```javascript=

    $(document).on('change', '.check_file', function() {
        var names = [];
        var length = $(this).get(0).files.length;
        for (var i = 0; i < $(this).get(0).files.length; ++i) {
            names.push($(this).get(0).files[i].name);
        }
        // $('input[name=file]').val(names);
        if (length > 2) {
            var fileName = names.join(', ');
            $(this).closest('.upload_grp').find('.upload_file').attr("value", length + " files selected");
        } else {
            $(this).closest('.upload_grp').find('.upload_file').attr("value", names);
        }
    });
```

## <span style="font-size:2em;margin-right:.2em;color:#21BAFF;" id="item-5">05. </span>有Icon的input 

在需帶有icon的<span class="focus3"><input></span>外層包覆<span class="focus">**`<div class="input-i"></div>`**</span>

<iframe height="200" style="width: 100%;" scrolling="no" title="有icon表單" src="https://codepen.io/u00hyui/embed/xxqoNRG?defaultTab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/xxqoNRG">
  有icon表單</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

## <span style="font-size:2em;margin-right:.2em;color:#21BAFF;" id="item-6">06. </span>表單排版範例

### 格線式表單
<iframe height="500" style="width: 100%;" scrolling="no" title="格線式表單" src="https://codepen.io/u00hyui/embed/poeXBVL?defaultTab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/poeXBVL">
  格線式表單</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

### 多欄、格線式表單 1
<iframe height="500" style="width: 100%;" scrolling="no" title="多欄、格線式表單 1" src="https://codepen.io/u00hyui/embed/GRWbbjw?defaultTab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/GRWbbjw">
  多欄、格線式表單 1</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

### 多欄、格線式表單 2
<iframe height="500" style="width: 100%;" scrolling="no" title="格線式表單 - 多欄、顯示label" src="https://codepen.io/u00hyui/embed/gOmNNmq?defaultTab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/gOmNNmq">
  格線式表單 - 多欄、顯示label</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

### 多層次表單
<iframe height="500" style="width: 100%;" scrolling="no" title="多層次表單" src="https://codepen.io/u00hyui/embed/gOmNNoy?defaultTab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/gOmNNoy">
  多層次表單</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
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