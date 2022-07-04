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
</script>

<style scoped>
a {
  font-family: sans-serif;
  font-size: 14px;
  text-align: center;
  color: #ffffff;
  margin-right: 30px;
}
</style>