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
  name: "CarouselTwoBy",
  data() {
    return {
      items: [
        {
          src: require("~/assets/images/twobythesea/sea1.jpg"),
        },
        {
          src: require("~/assets/images/twobythesea/sea2.jpg"),
        },
        {
          src: require("~/assets/images/twobythesea/sea3.jpg"),
        },
        {
          src: require("~/assets/images/twobythesea/sea4.jpg"),
        },
        {
          src: require("~/assets/images/twobythesea/sea5.jpg"),
        },
        {
          src: require("~/assets/images/twobythesea/sea6.jpg"),
        },
        {
          src: require("~/assets/images/twobythesea/sea7.jpg"),
        },
        {
          src: require("~/assets/images/twobythesea/sea8.jpg"),
        },
        {
          src: require("~/assets/images/twobythesea/sea9.jpg"),
        },
        {
          src: require("~/assets/images/twobythesea/sea10.jpg"),
        },
        {
          src: require("~/assets/images/twobythesea/sea11.jpg"),
        },
        {
          src: require("~/assets/images/twobythesea/sea12.jpg"),
        },
        {
          src: require("~/assets/images/twobythesea/sea13.jpg"),
        },
        {
          src: require("~/assets/images/twobythesea/sea14.jpg"),
        },
        {
          src: require("~/assets/images/twobythesea/sea15.jpg"),
        },
        {
          src: require("~/assets/images/twobythesea/sea16.jpg"),
        },
        {
          src: require("~/assets/images/twobythesea/sea17.jpg"),
        },
        {
          src: require("~/assets/images/twobythesea/sea18.jpg"),
        },
        {
          src: require("~/assets/images/twobythesea/sea19.jpg"),
        },
      ],
    };
  },
};
</script>
