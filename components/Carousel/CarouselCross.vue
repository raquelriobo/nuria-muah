<template lang="pug">
  v-carousel( cycle
              hide-delimiter-background
              :show-arrows="false")
    v-carousel-item(
                    v-for='(item,i) in items', 
                    :key="i",
                    :src= "item.src"
                    reverse-transition='fade-transition'
                    transition='fade-transition')
</template>

<script>
export default {
  name: "CarouselCross",
  data() {
    return {
      items: [
        {
          src: require("~/assets/images/cross/cross1.jpg"),
        },
        {
          src: require("~/assets/images/cross/cross2.jpg"),
        },
        {
          src: require("~/assets/images/cross/cross3.jpg"),
        },
        {
          src: require("~/assets/images/cross/cross4.jpg"),
        },
      ],
    };
  },
};
</script>
