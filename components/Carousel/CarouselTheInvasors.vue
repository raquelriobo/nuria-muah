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
  name: "CarouselTheInvasors",
  data() {
    return {
      items: [
        {
          src: require("~/assets/images/invasors/invasors1.jpg"),
        },
        {
          src: require("~/assets/images/invasors/invasors2.jpg"),
        },
        {
          src: require("~/assets/images/invasors/invasors3.jpg"),
        },
        {
          src: require("~/assets/images/invasors/invasors4.jpg"),
        },
      ],
    };
  },
};
</script>
