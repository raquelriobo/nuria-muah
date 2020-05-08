<template lang="pug">
  v-row.d-sm-flex.justify-space-around
    v-col(v-for="(item, i) in items" 
          :key="i")
      v-card.center(width="500" tile hover=true)
        nuxt-link(:to="item.to" tag="span" style="cursor: pointer")                            
          v-img.center(max-width="500"
                      :src= "item.src")
          h2 {{ item.title }} 
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          title: "WOMEN & MEN",
          src: require("~/assets/images/sandseason1.jpg"),
          to: "/works/editorialsWomen&Men",
        },
        {
          title: "KIDS",
          src: require("~/assets/images/tipi1.jpg"),
          to: "/works/editorialsKids",
        },
      ],
    };
  },
};
</script>

<style scoped>
.center {
  margin: 0 auto;
}
</style>
