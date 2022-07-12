<template>
  <div id="test">
  <img :src="require('@/assets/logo.png')" alt="картинка" height="20">
    <div id="list">
    <a href="">Корзина: {{cartcount}}</a><br>
    <a href="">Закладки: {{bmarkcount}}</a><br>
    <a href="">Резерв: {{rescount}}</a><br>
    </div>
  </div>
</template>

<script>
export default {
  name: "user-block",
  //required:true полезный параметр у пропа
  props: {
    cartcount: {type: Number, default: 0},
    bmarkcount: {type: Number, default: 0},
    rescount: {type: Number, default: 0},
  }
}

//TODO: это странно, но когда я отцентрировал текст - отцентрировалась и картинка
</script>

<style scoped>
a {
  font-family: sans-serif;
  font-size: 14px;
  color: #ffffff;
  margin-right: 30px;
}
#list {
  display:inline-block;
  text-align: left;
  vertical-align: middle;
}
img {
  vertical-align: middle
}
</style>