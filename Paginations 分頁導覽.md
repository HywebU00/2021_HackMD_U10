# Paginations / 分頁導覽
###### tags: `HyUI`

檔案名稱：sass/modual/_paginations.scss

## HTML範本1
<iframe height="265" style="width: 100%;" scrolling="no" title="Paginations / 分頁導覽1" src="https://codepen.io/u00hyui/embed/JjWobWJ?height=265&theme-id=dark&default-tab=html,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/u00hyui/pen/JjWobWJ'>Paginations / 分頁導覽1</a> by u00hyui
  (<a href='https://codepen.io/u00hyui'>@u00hyui</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

```htmlmixed=
<!-- Pagination -->
<div class="pagination">
    <form action="">
        <div class="form_inline">
            <div class="total"> 共<span>308</span>筆資料，第<span>1/18</span>頁，每頁顯示 <select name="" id="" aria-label="每頁顯示">
                    <option value="">10</option>
                    <option value="">20</option>
                    <option value="">30</option>
                    <option value="">40</option>
                </select> 筆， <input type="button" value="確定" class="btn btn-submit">
            </div>
        </div>
    </form>
    <ul class="page">
        <li class="first"><a href="#" title="第一頁">第一頁 </a></li>
        <li class="prev"><a href="#" title="回上一頁">回上一頁 </a></li>
        <li class="active"><a href="#">1</a></li>
        <li><a href="#">2</a></li>
        <li><a href="#">3</a></li>
        <li><a href="#">4</a></li>
        <li><a href="#">5</a></li>
        <li><a href="#">6</a></li>
        <li><a href="#">7</a></li>
        <li><a href="#">8</a></li>
        <li><a href="#">9</a></li>
        <li><a href="#">10</a></li>
        <li class="next"><a href="#" title="下一頁">下一頁 </a></li>
    </ul>
</div>
```

## HTML範本2

<iframe height="265" style="width: 100%;" scrolling="no" title="Paginations / 分頁導覽2" src="https://codepen.io/u00hyui/embed/zYZxowN?height=265&theme-id=dark&default-tab=html,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/u00hyui/pen/zYZxowN'>Paginations / 分頁導覽2</a> by u00hyui
  (<a href='https://codepen.io/u00hyui'>@u00hyui</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>


```htmlmixed=
<div class="pagination">
    <div class="total"> 共<span>308</span>筆資料，第<span>1/18</span>頁，</div>
    <div class="items">每頁顯示 <a href="#">20</a> <a href="#">40</a> <a href="#">60</a> 筆 </div>
    <ul class="page">
        <li class="first"><a href="#" title="第一頁">第一頁</a></li>
        <li class="prev"><a href="#" title="回上一頁">回上一頁 </a></li>
        <li class="active"><a href="#">1</a></li>
        <li class="xs_hidden"><a href="#">2</a></li>
        <li class="xs_hidden"><a href="#">3</a></li>
        <li class="xs_hidden"><a href="#">4</a></li>
        <li class="xs_hidden"><a href="#">5</a></li>
        <li class="next"><a href="#" title="下一頁">下一頁</a></li>
        <li class="last"><a href="#" title="最後一頁">最後一頁</a></li>
    </ul>
</div>
```

<style>
.ui-infobar{
max-width:95%;
}
.markdown-body{
max-width:95%;
}
</style>