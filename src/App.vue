<template>
  <div id="headbar1">
    <header-item text="Бесплатная доставка в 557 магазинов сети"></header-item>
    <header-item text="> 85000 пунктов самовывоза по всей России"></header-item>
    <header-item text="8 (800) 444-8-444 – круглосуточно"></header-item>
    <header-item text="Обратная связь"></header-item>
  </div>
  <div id="headbar2">
    Твой адрес
    <header-item text="Адреса магазинов"></header-item>
    <header-item text="Доставка и оплата"></header-item>
    <header-item text="Бонусная программа"></header-item>
    <header-item text="Партнёрская программа"></header-item>
    <header-item text="Войти"></header-item>
    <hr><br>
    <div id="headbar3">
      <img alt="Vue logo" src="./assets/logo.png" height="100">
    </div>
    <div id="headbar3">
      <input v-model="search" placeholder="Поиск" height="50px" style="border-radius: 5px "/>
    </div>
    <div id="headbar3">
      <button><img src=""></button>
    </div>
    <div id="headbar3">
      <user-block></user-block>
    </div>
  </div>
  <div id="headbar4">
    тест
    <header-item text="Книги"></header-item>
    <header-item text="Канцтовары"></header-item>
    <header-item text="Сувениры"></header-item>
    <header-item text="Игры и игрушки"></header-item>
    <header-item text="Творчество"></header-item>
    <header-item text="Распродажа"></header-item>
    <header-item text="Акции"></header-item>
    <header-item text="Подборки"></header-item>
    <header-item text="Читай-журнал"></header-item>
    <header-item text="Книжные циклы"></header-item>
    <hr><br>
  </div>
  <div id="bannerspanel">
    <promo-block></promo-block>
  </div>
  <div id="collections">
    <main-page-collection></main-page-collection>
    <main-page-collection></main-page-collection>
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import HeaderItem from "@/components/header-item";
import UserBlock from "@/components/user-block";
import PromoBlock from "@/components/promo-block";
import MainPageCollection from "@/components/main-page-collection";

export default {
  name: 'App',
  components: {
    MainPageCollection,
    PromoBlock,
    UserBlock,
    HeaderItem
    //HelloWorld
  },
  data() {
    return {
      search: ''
    }

  }
}

//TODO: почему когда я задал style тегу collections, то он уехал налево???
//TODO: как раскидать по сторонам элементы headbar3? и вообще как правильно балансировать элементы
//TODO: как сделать чтобы здесь задать цвет текста, которым будут выводиться headbar-ы?
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#headbar1 {
  font-family: Avenir, Helvetica, Arial Rounded MT Bold, sans-serif;
  color : white;
  background: blue;
  height: 25px;
}
#headbar2 {
  font-family: Avenir, Helvetica, Arial Rounded MT Bold, sans-serif;
  color : white;
  background: cornflowerblue;
}
#headbar3 {
  display:inline-block;
  vertical-align: middle
}
#headbar4 {
  font-family: Avenir, Helvetica, Arial Rounded MT Bold, sans-serif;
  color : black;
  background: white;
  margin-top: 5px;
  margin-bottom: 5px;
}
#bannerspanel {
  margin-top: 50px;
}
#collections {
  width: 1300px;
  margin-left: auto;
  margin-right: auto;
}
</style>