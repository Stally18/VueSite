<template>
  <div id="test"><a href="">Новинки литературы</a><br></div>
  <collection-book></collection-book>
  <collection-book></collection-book>
  <collection-book></collection-book>
  <collection-book></collection-book>
  <collection-book></collection-book>
</template>

<script>
import CollectionBook from "@/components/collection-book";

export default {
  name: "main-page-collection",
  components: {CollectionBook},
  props: {
    id: Number,
    // или же String
  },
  data() {
    return {
      books: [],
      // массив книжек, который мы передадим в v-for компоненту collection-book
    }
  }
}

// TODO: по хорошему, на основной странице должен вызываться этот элемент с конкретным id
// или сразу названию, и это название будет подставляться в шапку блока
// и по нему же будут выбираться книги из бд, и book уже будет вызываться для выбранных книг
</script>

<style scoped>
#test {
  text-align: left;
  margin-top: 50px;
}
</style>