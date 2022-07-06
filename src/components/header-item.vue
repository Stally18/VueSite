<template>
  <a href=""><img :src="img"> {{ text }}</a>
</template>

<script>
export default {
  name: "header-item",
  props: {
    text: String,
    img: String,
  }
}

// :alt="text"
//TODO: как сделать шрифт жирным? и убрать подчёркивание от тега a
//TODO: как сделать промежуток в центре?
//TODO: сделать аргумент image, чтобы использовать для первой шапки?
//TODO: как сделать, чтобы высота блока была больше, чем высота шрифта?
</script>

<style scoped>
a {
  font-family: sans-serif;
  font-size: 14px;
  text-align: center;
  margin-right: 30px;
}
</style>