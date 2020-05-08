<template lang="pug">
  v-layout
    v-flex.text-center
      v-col
        h1 Advertising
        CarouselAdvertising
</template>

<script>
import CarouselAdvertising from "@/components/Carousel/CarouselAdvertising";

export default {
  components: {
    CarouselAdvertising
  }
};
</script>

<style scoped>
.v-image__image--contain {
  background-size: contain;
}
</style>
