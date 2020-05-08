<template lang="pug">
  v-carousel( cycle
              hide-delimiters
              show-arrows-on-hover)
    v-carousel-item(v-for='(item,i) in items', 
                    :key="i",
                    :src= "item.src"
                    reverse-transition='fade-transition'
                    transition='fade-transition')
</template>

<script>
export default {
  name: "CarouselAdvertising",
  data() {
    return {
      items: [
        {
          src: require("~/assets/images/mariamorena/maria1.jpg"),
        },
        {
          src: require("~/assets/images/mariamorena/maria2.jpg"),
        },
        {
          src: require("~/assets/images/mariamorena/maria3.jpg"),
        },
        {
          src: require("~/assets/images/mariamorena/maria4.jpg"),
        },
        {
          src: require("~/assets/images/mariamorena/maria5.jpg"),
        },
        {
          src: require("~/assets/images/mariamorena/maria6.jpg"),
        },
        {
          src: require("~/assets/images/mariamorena/maria7.jpg"),
        },
        {
          src: require("~/assets/images/mariamorena/maria8.jpg"),
        },
        {
          src: require("~/assets/images/mariamorena/maria9.jpg"),
        },
        {
          src: require("~/assets/images/mariamorena/maria10.jpg"),
        },
        {
          src: require("~/assets/images/mariamorena/maria11.jpg"),
        },
        {
          src: require("~/assets/images/mariamorena/pub1.jpg"),
        },
        {
          src: require("~/assets/images/mariamorena/pub2.jpg"),
        },
        {
          src: require("~/assets/images/mariamorena/pub3.jpg"),
        },
        {
          src: require("~/assets/images/mariamorena/pub4.jpg"),
        },
        {
          src: require("~/assets/images/mariamorena/pub5.jpg"),
        },
      ],
    };
  },
};
</script>
