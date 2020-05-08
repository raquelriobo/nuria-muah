<template lang="pug">
  v-row.d-sm-flex.justify-space-around.align-center
    v-col
        v-img.center(max-width="500"
                    :src= "item.src")
    v-col
      v-card.center(width="500" flat tile)
        v-card-text
          h2
              | My makeup technique involves creating a flawless and fresh feel on all faces, 
              | I like all things, the light, frost, shiny, dewy, the new and scandalous.
              br
              | Now I am willing to travel and face new projects. My works were published in magazines such Elle, Cosmopolitan, Neo2, La Vanguardia ...
              br
              br
              b We talk?
        v-card-actions
          v-btn.center(:to="item.to" outlined tag="span" style="cursor: pointer") SEE MY WORKS!
</template>

<script>
export default {
  data() {
    return {
      item: {
        title: "ADVERTISING",
        src: require("~/assets/images/maria2.jpg"),
        to: "/works/advertising",
      },
    };
  },
};
</script>

<style scoped>
.center {
  margin: 0 auto;
}
</style>
