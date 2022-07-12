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

// TODO: чтобы выровнять название+автор, увы, нужен новый класс :(
</script>

<style scoped>
a {
  font-size: 14px;
}

#card {
  position: relative;
  display:inline-block;
  width: 210px;
  margin-top: 30px;
  margin-left: 50px;
  transition: all 0.1s ease-in-out;
}

#card::after {
  content: '';
  position: absolute;
  z-index: -1;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  opacity: 0;
  border-radius: 5px;
  box-shadow: 0 5px 10px rgba(0,0,0,0.3);
  transition: opacity 0.1s ease-in-out;
}

#card:hover::after {
  opacity: 1;
}
</style>