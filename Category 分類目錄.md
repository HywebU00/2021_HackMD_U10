# Category / 分類目錄

###### tags: `HyUI`

檔案名稱：sass/element/_category.scss

<iframe height="265" style="width: 100%;" scrolling="no" title="Category / 分類目錄" src="https://codepen.io/u00hyui/embed/poNmBqz?height=265&theme-id=dark&default-tab=html,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/u00hyui/pen/poNmBqz'>Category / 分類目錄</a> by u00hyui
  (<a href='https://codepen.io/u00hyui'>@u00hyui</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

### 範例：可加入數量統計狀態

可於連結內，放置<font color="#EE428B">span</font>標籤，讓程式帶入筆數數值即可。

## HTML範本
```htmlmixed=
<div class="category">
    <ul>
        <li><a href="#">標籤1 <span>10</span></a></li>
        <li><a href="#">標籤2 <span>5</span></a></li>
        <li><a href="#">標籤3 <span>4</span></a></li>
        <li><a href="#">標籤4 <span>6</span></a></li>
        <li><a href="#">標籤5 <span>12</span></a></li>
        <li><a href="#">標籤6 <span>9</span></a></li>
        <li><a href="#">標籤7 <span>5</span></a></li>
        <li><a href="#">標籤8 <span>2</span></a></li>
    </ul>
</div>
```

## JQuery設定:round_pushpin:
```javascript=
/*-----------------------------------*/
/////////// category active  //////////
/*-----------------------------------*/
$('.category').find('a').off().click(function(event) {
    $(this).parent('li').siblings().find('a').removeClass('active');
    $(this).addClass('active');
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
