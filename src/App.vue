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
    <br>
    <div id="headbar3">
      <img alt="Vue logo" src="./assets/logo.png" height=100>
    </div>
    <div id="headbar3">
      <input v-model="search" placeholder="Поиск"/>
    </div>
    <div id="headbar3">
      <button><img src=""></button>
    </div>
    <div id="headbar3">
      <user-block></user-block>
    </div>
  </div>
  <HelloWorld msg="Welcome to Your Vue.js App"/>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import HeaderItem from "@/components/header-item";
import UserBlock from "@/components/user-block";

export default {
  name: 'App',
  components: {
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

//TODO: перенести все хардкод-строки в data? передавать массив строк, который там в цикле фор обработается
//TODO: КАК ОТЦЕНТРИРОВАТЬ ВЕРТИКАЛЬНО БЛИН
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
}
#headbar2 {
  font-family: Avenir, Helvetica, Arial Rounded MT Bold, sans-serif;
  color : white;
  background: cornflowerblue;
  vertical-align: center;
}
#headbar3 {
  display:inline-block;
  vertical-align: center;
}
</style>