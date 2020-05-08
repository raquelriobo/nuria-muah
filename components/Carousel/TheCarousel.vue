<template lang="pug">
  v-carousel(
              cycle
              hide-delimiters
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
  name: "TheCarousel",
  data() {
    return {
      items: [
        {
          src: require("~/assets/images/bysummer2.jpg"),
        },
        {
          src: require("~/assets/images/combine2.jpg"),
        },
        {
          src: require("~/assets/images/cross2.jpg"),
        },
        {
          src: require("~/assets/images/mariamorena2.jpg"),
        },
        {
          src: require("~/assets/images/modevintage2.jpg"),
        },
        {
          src: require("~/assets/images/sandseason1.jpg"),
        },
        {
          src: require("~/assets/images/theinvasores2.jpg"),
        },
        {
          src: require("~/assets/images/tipi2.jpg"),
        },
        {
          src: require("~/assets/images/twobythesea2.jpg"),
        },
      ],
    };
  },
};
</script>

<style>
@media (min-width: 540px) {
  .v-image__image--cover {
    background-size: contain !important;
  }
}
</style>
