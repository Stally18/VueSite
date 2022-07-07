<template>
  <div id="test">
  <img src="" alt="картинка">
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

//TODO: почему text-align не работает для тега а но работает для div
//TODO: почему ничего не работает для выравнивания картинки
</script>

<style scoped>
a {
  font-family: sans-serif;
  font-size: 14px;
  text-align: left;
  color: #ffffff;
  margin-right: 30px;
}
#list {
  display:inline-block;
  text-align: left;
}
img {
  vertical-align: middle
}
</style>