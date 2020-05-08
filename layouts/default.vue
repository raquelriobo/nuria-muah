<template lang="pug">
  v-app
    TheNavigation
    v-content
      v-container
        nuxt
    v-footer(padless app)
      v-row(justify='center', no-gutters)
        v-btn(icon href="https://www.instagram.com/nuriariobomuah/?hl=es" color='black', text, rounded)
          v-icon mdi-instagram
        v-col.pt-0.py-2.text-center(cols='12')
          span © {{ new Date().getFullYear() }} - Nuria Riobó | Designed by Raquel Riobó
</template>

<script>
import TheNavigation from "@/components/Navigation/TheNavigation";

export default {
  components: {
    TheNavigation,
  },
};
</script>

<style>
html {
  font-family: "Open Sans", sans-serif;
}
h2 {
  font-family: "Courier New", Courier, monospace;
  line-height: 2;
}
p {
  font-family: "Courier New", Courier, monospace;
  font-size: 1.2rem;
  line-height: 2;
}

body {
  margin: 0;
}
</style>
