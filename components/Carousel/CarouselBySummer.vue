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
  name: "CarouselBySummer",
  data() {
    return {
      items: [
        {
          src: require("~/assets/images/bysummer/sum1.jpg"),
        },
        {
          src: require("~/assets/images/bysummer/sum2.jpg"),
        },
        {
          src: require("~/assets/images/bysummer/sum3.jpg"),
        },
        {
          src: require("~/assets/images/bysummer/sum4.jpg"),
        },
        {
          src: require("~/assets/images/bysummer/sum5.jpg"),
        },
        {
          src: require("~/assets/images/bysummer/sum6.jpg"),
        },
        {
          src: require("~/assets/images/bysummer/sum7.jpg"),
        },
        {
          src: require("~/assets/images/bysummer/sum8.jpg"),
        },
        {
          src: require("~/assets/images/bysummer/sum9.jpg"),
        },
        {
          src: require("~/assets/images/bysummer/sum10.jpg"),
        },
        {
          src: require("~/assets/images/bysummer/sum11.jpg"),
        },
        {
          src: require("~/assets/images/bysummer/sum12.jpg"),
        },
        {
          src: require("~/assets/images/bysummer/sum13.jpg"),
        },
        {
          src: require("~/assets/images/bysummer/sum14.jpg"),
        },
        {
          src: require("~/assets/images/bysummer/sum15.jpg"),
        },
        {
          src: require("~/assets/images/bysummer/sum16.jpg"),
        },
        {
          src: require("~/assets/images/bysummer/sum17.jpg"),
        },
        {
          src: require("~/assets/images/bysummer/sum18.jpg"),
        },
      ],
    };
  },
};
</script>
