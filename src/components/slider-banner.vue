<template>
  <a :href="link[bannerArrayIndex]">
    <img :src="pic[bannerArrayIndex]" height="300">
  </a>
</template>

<script>
export default {
  name: "slider-banner",
  data() {
    return {
      pic: [require("@/assets/banner1.jpg"), require("@/assets/logo.png"), require("@/assets/banner2.png"), require("@/assets/banner3.png") ],
      link: [],
      arrayindex: 0,
    }
  },
  // эта штука увеличивает счётчик каждые 10 секунд
  mounted() {
    setInterval(() => {
      this.arrayindex++
      if (this.arrayindex > 3) this.arrayindex = 0
    }, 10000)
  },
  computed: {
    bannerArrayIndex() {
      return this.arrayindex
    }
  }
}

// TODO: почему не отображаются картинки, даже стандартное лого??
</script>

<style scoped>
a {
  width: 500px
}
</style>