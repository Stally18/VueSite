<template>
  <a href=""><img :src="img">
    <div id="text">{{ text }}</div>
  </a>
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
//TODO: как сделать шрифт жирным?????????77
//TODO: как сделать промежуток в центре?
//TODO: сделать аргумент image, чтобы использовать для первой шапки?
</script>

<style scoped>
a {
  font-family: sans-serif;
  font-size: 14px;
  text-align: center;
  margin-right: 30px;
}
#text {
  display: inline-block;
  font-weight: bold;
}
</style>