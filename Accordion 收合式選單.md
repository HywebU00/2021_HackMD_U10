# Accordion 收合式選單

###### tags: `HyUI`

檔案名稱：sass/modual/_accordion.scss

## HTML範本1
<iframe height="350" style="width: 100%;" scrolling="no" title="Accordion 收合式選單" src="https://codepen.io/u00hyui/embed/mdEZoEr?height=265&theme-id=dark&default-tab=html,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/u00hyui/pen/mdEZoEr'>Accordion 收合式選單</a> by u00hyui
  (<a href='https://codepen.io/u00hyui'>@u00hyui</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>


```htmlmixed=
<div class="accordion">
  <ul>
    <li>
      <a href="#" title="">第一項說明</a>
      <div class="accordion-content">直麼後大得股的要會使成事公人策公！我古車未書！上工題向案校立詩為色能狀計氣卻力沒時臺地是了養、後天連意市風怕著數往發民文手好，費的而西成曾給理必事後生包，就雄一過電流人住完是成；識愛作流：數關與不個性，還行案！住像印以排傷顧向樓事不音受差，重飯就孩他政的給滿綠不受東心斷來前現模微。</div>
    </li>
    <li>
      <a href="#" title="">第二項說明</a>
      <div class="accordion-content">國影自談王不美一文實別合屋？府性元這子一知於料的親到。一用技年不得就資公，也星樣團怎英班水灣個種決以因世書發定很功行何，下飯通反代命假到一不離護麼錯絕懷旅元人。弟新過，道給仍覺裡水國、醫灣了可實界一上德字什心成但創大品隨品。難但所雜笑事禮年專阿戲經愛眾背起，間自個；獎小業美有義交安辦一則龍足，年開多！景唱而賽用出說建樣以經，哥中每去已識著門家故破人而老動工我簡的利管人早什。葉禮名交，都說為一失到就招投高畫。月錢產，機力燈自體日關工車之土庭，件年真經書？</div>
    </li>
    <li>
      <a href="#" title="">第三項說明</a>
      <div class="accordion-content">員無的出從身岸前命想總來到爾八片品每單起關開因打實的爭己正新軍者常創的他現都對位家走許曾東們前草信車我……但機這等意故灣態一員見訴活老見以的無又，一定市不公，也列為吃媽像天對是修送教這原人地樹多相為的物立子進，館企！</div>
    </li>
  </ul>
</div>
```

## JQuery設定:round_pushpin:
```javascript=
/*-----------------------------------*/
//////////// Accordion設定 ////////////
/*-----------------------------------*/
$('.accordion').each(function() {
    $(this).find('.accordion-content').hide();
    var _accordionItem = $(this).children('ul').children('li').children('a');
    _accordionItem.each(function() {
        function accordion(e) {
            $(this).parent('li').siblings().children('a').removeClass('active');
            $(this).toggleClass('active');
            $(this).parent('li').siblings().children('.accordion-content').slideUp();
            $(this).next('.accordion-content').slideToggle();
            e.preventDefault();
        }
        $(this).click(accordion);
        $(this).keyup(accordion);
    });
});
```
## HTML範本2-使用button寫法
<iframe height="400" style="width: 100%;" scrolling="no" title="Accordion 收合式選單-button按鈕" src="https://codepen.io/u00hyui/embed/JjWYJrp?height=265&theme-id=dark&default-tab=css,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/u00hyui/pen/JjWYJrp'>Accordion 收合式選單-button按鈕</a> by u00hyui
  (<a href='https://codepen.io/u00hyui'>@u00hyui</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

```htmlmixed=
<!--Accordion  start-->
<div class="accordionqa">
  <!-- accordionblock  start-->
  <div class="accordionblock">
    <button type="button" class="Q"><span>Q.</span>雇主可否解僱欲申請復職之育嬰留停受僱者?</button>
    <div class="A">
      <span>A.</span>
      <div class="Ablock">
        <p>受僱者於育嬰留職停薪期滿後，申請復職時，除有下列情形之一，並經主管機關同意者外，雇主不得拒絕：</p>
        <ol>
          <li> 歇業、<em>23</em>虧損或業務緊縮者。</li>
          <li> 雇主依法變更組織、解散或轉讓者。</li>
          <li> 不可抗力暫停工作在一個月以上者。</li>
          <li> 業務性質變更，有減少受僱者之必要，又無適當工作可供安置者。</li>
        </ol>
        <p>雇主因前項各款原因未能使受僱者復職時，應於三十日前通知之，並應依法定標準發給資遣費或退休金。</p>
      </div>
    </div>
  </div>
  <!-- accordionblock  end-->
  <!-- accordionblock  start-->
  <div class="accordionblock">
    <button type="button" class="Q btn-green">Q. 雇主可否解僱懷孕婦女、分娩婦女或育嬰留停受僱者?</button>
    <div class="A">
      <span>A.</span>
      <div class="Ablock">
        <p>性別工作平等法第11條第2項規定：「工作規則、勞動契約或團體協約，不得規定或事先約定受僱者有結婚、懷孕、分娩或育兒之情事時，應行離職或留職停薪；亦不得以其為解僱之理由。」倘雇主違反上開規定，依該法第11條第3項規定，其規定或約定無效；勞動契約之終止不生效力。</p>
      </div>
    </div>
  </div>
  <!-- accordionblock  end-->
  <!-- accordionblock  start-->
  <div class="accordionblock">
    <button type="button" class="Q  btn-orange">Q.勞工職業災害醫療期間，不得終止契約，又雇主在何種情況下可以合法與勞工終止契約？</button>
    <div class="A">
      <span>A.</span>
      <div class="Ablock">
        <p>勞工於職業災害醫療期間雇主不能與勞工終止勞動契約，法律之禁止規定，旨為保護勞工權益，但勞工若有惡意行為則不在保護範圍之內，諸如無正當理由之曠職等。又據職業災害勞工保護法第<em>23</em>條規定，以下三種情形者，雇主依法給付資遣費或退休金後，可以合法終止勞動契約為：</p>
        <p>雇主因天災、事變或其他不可抗力原因，致事業不能繼續且經主管機關核准者。</p>
        <p>雇主歇業或重大虧損經主管機關核准者。</p>
        <p>職業災害勞工治療終止，經公立醫院診斷確定心神喪失或身體殘廢不堪勝任工作者。</p>
      </div>
    </div>
  </div>
  <!-- accordionblock  end-->
</div>
<!--Accordion  end-->
```

## JQuery設定
```javascript=
$(".accordionblock").each(function() {
    var _accordionItem2 = $(this).children(".Q");
    _accordionItem2.each(function() {
        function accordion2(e) {
            $(this).next(".A").slideToggle();
            $(this).parent().siblings().children(".A").slideUp();
            $(this).parent().siblings().children(".Q").removeClass("turnicon");
            $(this).toggleClass("turnicon");
            e.preventDefault();
        }
        $(this).click(accordion2);
        $(this).keyup(accordion2);
    });
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
