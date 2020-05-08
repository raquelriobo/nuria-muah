<template lang="pug">
  v-layout
    v-flex.text-center
      h1 Editorials
      Editorials
      br
      h1 Advertising
      Advertising
</template>

<script>
import TheCarousel from "@/components/Carousel/TheCarousel";
import Advertising from "@/components/Works/Advertising";
import Editorials from "@/components/Works/Editorials";

export default {
  components: { TheCarousel, Advertising, Editorials }
};
</script>
