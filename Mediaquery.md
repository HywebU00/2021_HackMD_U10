# Mediaquery
###### tags: `HyUI`
檔案名稱：sass/common/mixins/_mediaquery.scss
檔案名稱：sass/common/_mixin.scss

## 選擇優雅降級(Graceful Degradation)的開發流程
>目前大部分的網站規格是以IE9+、FireFox、Chrome以及Safari為主流瀏覽器，且UI設計師產出之mockup大部分以PC版本作為風格確認，因此先以主流瀏覽器為測試對象，再往下兼容行動版以及各種不同瀏覽器的呈現。[color=#009ee7]

![](https://i.imgur.com/7de2I7B.jpg)
### 如何自訂自己的斷點
可在 <font color="#EE428B">_variable.scss</font> 自訂斷點，預設是以 <font color="#EE428B">1400px</font> 、 <font color="#EE428B">992px</font> 、 <font color="#EE428B">768px</font> 、 <font color="#EE428B">576px</font> 為分界

```sass=
//mediaquery breakpoint
$screen-lg:        1400px !default;        //電腦
$screen-md:        992px  !default;        //平板
$screen-sm:        768px  !default;        //手機 
$screen-xs:        576px  !default;        //極小尺寸
```
### SCSS設定

針對不同的瀏覽器寬度斷點設定，HyUI提供快速套用變數的 <font color="#EE428B">mixin</font> ，供開發者直覺地且輕易地在樣式表分別寫出不同的效果

<font color="#ff0000">請注意順序，如果是使用HyUI預設斷點mixin是由較寬螢幕至最小寬度依序設定，避免被覆蓋。</font>
```sass=
.wrapper {
  margin: 0 auto;
  width: 100%; 
  @include screen('desktop') {
      width: 90%; }
  @include screen('notebook') {
      width: 85%; }
  @include screen('tablet') {
      width: 55%; }
  @include screen('mobile') {
      width: 85%; }
  @include screen('xs_mobile') {
      width: 85%; } 
}
```
### CSS輸出
```css=
.wrapper {
    margin: 0 auto;
    width: 100%; }
@media screen and (min-width: 1400px) {
    .wrapper {width: 90%; } }
@media screen and (max-width: 1399px) {
    .wrapper {width: 85%; } }
@media screen and (max-width: 991px) {
    .wrapper {width: 55%; } }
@media screen and (max-width: 767px) {
    .wrapper {width: 85%; } }
@media screen and (max-width: 575px) {
    .wrapper {width: 85%; } }
```


<style>
.ui-infobar{
max-width:95%;
}
.markdown-body{
max-width:95%;
}
</style>