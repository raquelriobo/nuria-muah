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
  name: "CarouselSand",
  data() {
    return {
      items: [
        {
          src: require("~/assets/images/sandseason/season1.jpg"),
        },
        {
          src: require("~/assets/images/sandseason/season2.jpg"),
        },
        {
          src: require("~/assets/images/sandseason/season3.jpg"),
        },
        {
          src: require("~/assets/images/sandseason/season4.jpg"),
        },
        {
          src: require("~/assets/images/sandseason/season5.jpg"),
        },
        {
          src: require("~/assets/images/sandseason/season6.jpg"),
        },
        {
          src: require("~/assets/images/sandseason/season7.jpg"),
        },
        {
          src: require("~/assets/images/sandseason/season8.jpg"),
        },
        {
          src: require("~/assets/images/sandseason/season9.jpg"),
        },
        {
          src: require("~/assets/images/sandseason/season10.jpg"),
        },
        {
          src: require("~/assets/images/sandseason/season11.jpg"),
        },
      ],
    };
  },
};
</script>
