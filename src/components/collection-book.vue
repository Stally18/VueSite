<template>
  <div id="card">
    <a href="">
      <img :src="link"><br>
      {{title}}<br>
      {{author}}
    </a><br><br>
    {{price}}<br>
    <button><img src="">Купить</button> <button><img src=""></button>
  </div>
</template>

<script>
function getInfo() {
  // здесь происходит вытягивание данных о книге из бд по её айдишнику
}

export default {
  name: "collection-book",
  props: {
    id: Number,
  },
  data() {
    return {
      link: './assets/logo.png',
      title: 'Стальной Алхимик. Книга 16',
      author: 'Аракава Х.',
      imglink: '',
      price: '999',
    }
  },
  mounted() {
    getInfo(this.id);
  }
}
</script>

<style scoped>
#card {
  display:inline-block;
  width: 150px;
  margin-top: 30px;
  margin-left: 50px;
}
</style>