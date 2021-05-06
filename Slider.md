# Slider
###### tags: `HyUI`

檔案名稱：sass/_slick.scss

HyUI使用 <font color="#009ee7">slick</font> 的輪播模組，目前hyUI <font color="#EE428B">vendor</font> 內含 <font color="#EE428B">slick</font>已經有加入客製化設定，如需要最新版，請到 <font color="#009ee7">slick</font>官網下載。

## 請在網頁中匯入slick 外掛
slick屬於外掛，故放在 <font color="#EE428B">vendor</font> 資料夾裡，包括所有的圖檔、js、css

### 匯入外掛CSS
```htmlmixed=
<link rel="stylesheet" type="text/css" href="vendor/slick/slick.css"/>
<link rel="stylesheet" type="text/css" href="vendor/slick/slick-theme.css"/>
```
### 匯入JS
```htmlmixed=
<script type="text/javascript" src="vendor/slick/slick.min.js"></script>
```
### Slick的基本設定
使用設定以slick官方文件為準。
```javascript =
$(document).ready(function(){
  $('.your-class').slick({
    arrows: true,                       //左右箭頭
    autoplay: false,                    //自動播放
    autoplaySpeed: 3000,                //自動播放秒數
    dots: false,                        //顯示圓點
    dotsClass:  'slick-dots',           //原點css
    draggable: true,                    //滑鼠可以拖曳
    infinite: true,                     //無限輪播
    pauseOnHover: true,                 //滑鼠移過後暫停自動撥放
    pauseOnDotsHover: false,            //滑鼠移過圓點後暫停自動撥放
    rtl: false,                         //改變輪播方向
    slidesToShow: 1,                    //一次顯示幾張
    slidesToScroll: 1,                  //一次輪播幾張
    vertical: false                     //改成垂直方向
  });
});
```

# 01.大圖輪播範例
本版本輪播圖檔可使用 <font color="#EE428B">obect-fit</font> 設定，故上稿內容不限尺寸，皆可正常呈現。



<style>
.ui-infobar{
max-width:95%;
}
.markdown-body{
max-width:95%;
}
</style>