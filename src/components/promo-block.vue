<template>
  <slider-banner></slider-banner>
  <a id="minibanner" href="">
    <div id="block">
      Лучшие из лучших<br>
      <img :src="require('@/assets/logo.png')" width="150"><br>
      Подборка лучших книг<br>
      На основании продаж интернет-магазина<br>
    </div>
  </a>
  <div id="outerlist">
    <a id="minibanner" href="">
      <img :src="require('@/assets/logo.png')" width="50">
      <div id="list">
        Для любителей ярких красок<br>
        Подборка товаров по цветам радуги<br>
      </div>
    </a> <br>
    <a id="minibanner" href="">
      <img :src="require('@/assets/logo.png')" width="50">
      <div id="list">
        Книжный дозор<br>
        Делитесь впечатлениями, получайте бонусы<br>
      </div>
    </a> <br>
    <a id="minibanner" href="">
      <img :src="require('@/assets/logo.png')" width="50">
      <div id="list">
        Игра "Книжный филворд"<br>
        Скидка 15% за победу<br>
      </div>
    </a> <br>
  </div>
</template>

<script>
import SliderBanner from "@/components/slider-banner";

export default {
  name: "promo-block",
  components: {
    SliderBanner,
  }
}

//TODO: Почему если делаю тег list, то всё нормально комбится, a outerlist перестаёт комбиться
//TODO: У БЛОКА list ИСЧЕЗЛО ПОДЧЁРКИВАНИЕ ОТ ТЕГА а ЧО БЛИН
</script>

<style scoped>
#list {
  display:inline-block;
  color: black;
}
a {
  display:inline-block;
}
#block {
  width: 200px;
}
#minibanner {
  margin-left: 30px;
  margin-bottom: 30px;
  border: darkgrey solid 1px;
}
#outerlist {
  width: 200px;
  display:inline-block;
}
</style>