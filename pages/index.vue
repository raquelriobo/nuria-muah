<template lang="pug">
  v-layout
    v-flex.text-center
      v-img.center(max-width="500"
            :src= "item.src")
      blockquote.blockquote {{item.quote}}
        footer
          small
            em
            | — {{item.title}}
      TheCarousel
</template>

<script>
import TheCarousel from "@/components/Carousel/TheCarousel";

export default {
  components: { TheCarousel },
  data() {
    return {
      item: {
        title: "Nuria Riobó",
        quote: "“Welcome to my world, expression of beauty and creativity.”",
        src: require("~/assets/images/logo.jpg")
      }
    };
  }
};
</script>

<style scoped>
.center {
  margin: 0 auto;
}
</style>
