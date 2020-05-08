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
  name: "CarouselTipi",
  data() {
    return {
      items: [
        {
          src: require("~/assets/images/tipi/tipi1.jpg"),
        },
        {
          src: require("~/assets/images/tipi/tipi2.jpg"),
        },
        {
          src: require("~/assets/images/tipi/tipi3.jpg"),
        },
        {
          src: require("~/assets/images/tipi/tipi4.jpg"),
        },
      ],
    };
  },
};
</script>
