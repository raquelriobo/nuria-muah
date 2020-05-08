<template lang="pug">
  v-layout
    v-flex.text-center
      v-col
        h1 Tipi 
        p (Minor Republic)
        CarouselTipi
      v-col
        h1 Two By The Sea
        p (Ivi magazine)
        CarouselTwoBy
      v-col
        h1 By Summer 
        p (Petit Style)
        CarouselBySummer
</template>

<script>
import CarouselTipi from "@/components/Carousel/CarouselTipi";
import CarouselTwoBy from "@/components/Carousel/CarouselTwoBy";
import CarouselBySummer from "@/components/Carousel/CarouselBySummer";

export default {
  components: {
    CarouselTipi,
    CarouselTwoBy,
    CarouselBySummer
  }
};
</script>
