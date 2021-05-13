# Modal 彈出對話框
###### tags: `HyUI`

檔案名稱：sass/modual/_modal.scss

此燈箱模組為示範範例。頁面需要觸發的連結按鈕，以及燈箱區塊設定，使用以下的程式碼範例，可自行修改所需樣式，可於 <font color="#EE428B">scss</font> 修改 <font color="#EE428B">顏色</font> 、 <font color="#EE428B">大小</font> 、 <font color="#EE428B">動畫效果</font> ...等。

<iframe height="450" style="width: 100%;" scrolling="no" title="Modal 彈出對話框" src="https://codepen.io/u00hyui/embed/JjWGaWa?height=265&theme-id=dark&default-tab=js,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/u00hyui/pen/JjWGaWa'>Modal 彈出對話框</a> by u00hyui
  (<a href='https://codepen.io/u00hyui'>@u00hyui</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

## HTML範本
```htmlmixed=
<button type="button" id="openModal" class="btn">開啟視窗</button>
<!--視窗-->
<div id="modal1" class="modal">
    <!--     div內的內容可以自行設定 -->
    <h2>標題</h2>
    <p>內文</p>
</div>
```

## JQuery設定

```javascript=
/*-----------------------------------*/
/////////////modal設定/////////////
/*-----------------------------------*/
$(function () {
  $("#modal1").hide(); //先隱藏視窗
  $(".modal").after('<div class="modal_overlay"></div>'); //新增透明底
  $(".modal").prepend('<button type="button" class="close">關閉</button>'); //新增關閉按鈕
  $(".modal_overlay").hide(); //隱藏透明底
  //按鈕動作
  $("#openModal").click(function (e) {
    $(".modal_overlay").fadeIn(100);
    $(".modal").fadeIn(100);
    $("body").addClass("noscroll");
    e.preventDefault();
  });
  //關閉function
  function closeModal() {
    $("#modal1").hide();
    $(".modal_overlay").hide();
    $("body").removeClass("noscroll");
  }
  //點選關閉按鈕及透明底都可關閉
  $(".modal_overlay").click(closeModal);
  $(".modal .close").click(closeModal);
});
```
<style>
.ui-infobar{
max-width:95%;
}
.markdown-body{
max-width:95%;
}
</style>