<template lang="pug">
  v-carousel( cycle
              hide-delimiter-background
              :show-arrows="false")
    v-carousel-item(v-for='(item,i) in items', 
                    :key="i",
                    :src= "item.src"
                    reverse-transition='fade-transition'
                    transition='fade-transition')
</template>

<script>
export default {
  name: "CarouselVintage",
  data() {
    return {
      items: [
        {
          src: require("~/assets/images/vintage/vintage1.jpg"),
        },
        {
          src: require("~/assets/images/vintage/vintage2.jpg"),
        },
        {
          src: require("~/assets/images/vintage/vintage3.jpg"),
        },
        {
          src: require("~/assets/images/vintage/vintage4.jpg"),
        },
        {
          src: require("~/assets/images/vintage/vintage5.jpg"),
        },
        {
          src: require("~/assets/images/vintage/vintage6.jpg"),
        },
        {
          src: require("~/assets/images/vintage/vintage7.jpg"),
        },
        {
          src: require("~/assets/images/vintage/vintage8.jpg"),
        },
        {
          src: require("~/assets/images/vintage/vintage9.jpg"),
        },
      ],
    };
  },
};
</script>
