# Fixed_sidebar / 固定側邊欄

###### tags: `HyUI`
檔案名稱：sass/modual/_fixed_sidebar.scss

hyUI提供一個固定側邊欄的作法，固定特定位置，而不隨滾動欄滾動。


<iframe height="450" style="width: 100%;" scrolling="no" title="側邊選單01" src="https://codepen.io/u00hyui/embed/poPgOjZ?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/poPgOjZ">
  側邊選單01</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

## HTML範本
```htmlmixed=
<!-- fixed_sidebar start -->
<div class="fixed_sidebar_group">
  <div class="sidebar_list">
    <a href="#">
      <div class="list_img"><img src="https://hywebu00.github.io/hyui_flex/images/icon/icon_grid2.svg"></div>
      <div class="list_title">側邊第一選項</div>
    </a>
  </div>
  <div class="sidebar_list">
    <a href="#">
      <div class="list_img"><img src="https://hywebu00.github.io/hyui_flex/images/icon/icon_setting2.svg"></div>
      <div class="list_title">側邊第二選項</div>
    </a>
  </div>
  <div class="sidebar_list">
    <a href="#">
      <div class="list_img"><img src="https://hywebu00.github.io/hyui_flex/images/icon/icon_home2.svg"></div>
      <div class="list_title">側邊第三選項</div>
    </a>
  </div>
  <div class="sidebar_list">
    <a href="#">
      <div class="list_img"><img src="https://hywebu00.github.io/hyui_flex/images/icon/icon_star2.svg"></div>
      <div class="list_title">側邊第四選項</div>
    </a>
  </div>
  <div class="sidebar_list">
    <a href="#">
      <div class="list_img"><img src="https://hywebu00.github.io/hyui_flex/images/icon/icon_heart2.svg"></div>
      <div class="list_title">側邊第五選項</div>
    </a>
  </div>
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
