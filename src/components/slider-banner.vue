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
      pic: ["src/assets/banner1.jpg", "src/assets/logo.png", "src/assets/banner2.png", "src/assets/banner3.png" ],
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

</style>