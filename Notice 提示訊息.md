# Notice / 提示訊息

###### tags: `HyUI`

檔案名稱：sass/modual/_notice.scss

通常用於表單輸入狀態之提示，可自由替換提示訊息之文本。

## HTML範本 - 預設格式

<iframe height="290" style="width: 100%;" scrolling="no" title="Notice / 提示訊息" src="https://codepen.io/u00hyui/embed/rNyxZdv?height=265&theme-id=dark&default-tab=html,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/u00hyui/pen/rNyxZdv'>Notice / 提示訊息</a> by u00hyui
  (<a href='https://codepen.io/u00hyui'>@u00hyui</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

```htmlmixed=
<div class="notice">這是一般提醒訊息區塊</div>
<div class="notice_info">這是一般提醒訊息區塊</div>
<div class="notice_success">您已經成功登入</div>
<div class="notice_warning">這似乎不是一個正常的Email格式</div>
<div class="notice_error">您輸入的帳號密碼有誤！</div>
```


## HTML範本 - 有關閉按鈕

<iframe height="290" style="width: 100%;" scrolling="no" title="Notice / 提示訊息- 有關閉按鈕" src="https://codepen.io/u00hyui/embed/wvJMEXz?height=265&theme-id=dark&default-tab=html,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/u00hyui/pen/wvJMEXz'>Notice / 提示訊息- 有關閉按鈕</a> by u00hyui
  (<a href='https://codepen.io/u00hyui'>@u00hyui</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

```htmlmixed=
<div class="notice">這是一般提醒訊息區塊 <a href="#" class="close"><img src="images/basic/icon_close.svg" alt=""></a>
</div>
<div class="notice_info">這是一般提醒訊息區塊 <a href="#" class="close"><img src="images/basic/icon_close.svg" alt=""></a>
</div>
<div class="notice_success">您已經成功登入 <a href="#" class="close"><img src="images/basic/icon_close.svg" alt=""></a>
</div>
<div class="notice_warning">這似乎不是一個正常的Email格式 <a href="#" class="close"><img src="images/basic/icon_close.svg" alt=""></a>
</div>
<div class="notice_error">您輸入的帳號密碼有誤！ <a href="#" class="close"><img src="images/basic/icon_close.svg" alt=""></a>
</div>
```

## JQuery設定:round_pushpin:


```javascript=
/*-----------------------------------*/
//////////// notice訊息區塊 ////////////
/*-----------------------------------*/
$('[class*="notice"] a.close').click(function(e) {
    $(this).parent('[class*="notice"]').hide();
    e.preventDefault();
});
```
:link: 範例可參考 [轉寄友人](https://hywebu00.github.io/hyui_flex/fp_template.htm) 頁面。


<style>
.ui-infobar{
max-width:95%;
}
.markdown-body{
max-width:95%;
}
</style>
