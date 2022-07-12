<template>
  <a href="">
    <img :src="img">
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