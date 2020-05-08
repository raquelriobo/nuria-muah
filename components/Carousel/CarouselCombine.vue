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
  name: "CarouselCombine",
  data() {
    return {
      items: [
        {
          src: require("~/assets/images/combine/combine1.jpg"),
        },
        {
          src: require("~/assets/images/combine/combine2.jpg"),
        },
        {
          src: require("~/assets/images/combine/combine3.jpg"),
        },
        {
          src: require("~/assets/images/combine/combine4.jpg"),
        },
        {
          src: require("~/assets/images/combine/combine5.jpg"),
        },
        {
          src: require("~/assets/images/combine/combine6.jpg"),
        },
        {
          src: require("~/assets/images/combine/combine7.jpg"),
        },
      ],
    };
  },
};
</script>
