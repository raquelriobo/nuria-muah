<template lang="pug">
  v-layout
    v-flex.text-center
      v-col
        h1 Cross 
        p (Cosmopolitan)
        CarouselCross
      v-col
        h1 Sand Season
        p  (ELLE)
        CarouselSand
      v-col
        h1 Mode Vintage
        p (Kluid Mag)
        CarouselVintage
      v-col
        h1 Combine
        p (NEO2)
        CarouselCombine
      v-col
        h1 The Invasors
        p (Croco Mag)
        CarouselTheInvasors
</template>

<script>
import CarouselCross from "@/components/Carousel/CarouselCross";
import CarouselSand from "@/components/Carousel/CarouselSand";
import CarouselVintage from "@/components/Carousel/CarouselVintage";
import CarouselCombine from "@/components/Carousel/CarouselCombine";
import CarouselTheInvasors from "@/components/Carousel/CarouselTheInvasors";

export default {
  components: {
    CarouselCross,
    CarouselSand,
    CarouselVintage,
    CarouselCombine,
    CarouselTheInvasors
  }
};
</script>
