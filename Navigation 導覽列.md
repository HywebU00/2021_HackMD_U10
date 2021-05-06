# Navigation 導覽列

###### tags: `HyUI`

檔案名稱：sass/_header.scss
檔案名稱：sass/_menu.scss

導覽列由 <font color="#EE428B">nav.navigaton</font> 包覆，預設內含 <font color="#EE428B">導覽連結</font>、<font color="#EE428B">字型大小</font>、<font color="#EE428B">語言選擇</font>，字型大小設定由<font color="#009ee7">hyui.js</font>    判斷，預設為中字型。

## HTML範本
```htmlmixed=
<!-- navigation Start -->
<nav class="navigation" role="navigation" aria-label="Site">
    <!-- 新增div navlist -->
    <div class="navlist">
        <ul>
            <li><a href="#">回首頁</a></li>
            <li><a href="#">網站導覽</a></li>
            <li><a href="#">English</a></li>
            <li><a href="#">常見問答</a></li>
        </ul>
    </div>
    <!-- font_size -->
    <div class="font_size">
        <span>字型大小：</span>
        <!-- 英文用<span>font-size：</span> -->
        <ul>
            <li><a href="#" class="small">小</a></li>
            <li><a href="#" class="medium">中</a></li>
            <li><a href="#" class="large">大</a></li>
        </ul>
    </div>
    <!-- language -->
    <div class="language">
        <a href="#">語言選擇</a>
        <ul>
            <li><a href="#">繁體中文</a></li>
            <li><a href="#">简体中文</a></li>
            <li><a href="#">ENGLISH</a></li>
        </ul>
    </div>
</nav>
<!-- navigation End -->
```



<style>
.ui-infobar{
max-width:95%;
}
.markdown-body{
max-width:95%;
}
</style>
