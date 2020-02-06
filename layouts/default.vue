<template>
  <div>
    <app-nav />
    <nuxt />
  </div>
</template>


<script>
import AppNav from "~/components/AppNav.vue";

export default {
  components: {
    AppNav
  }
};
</script>

<style>
html {
  font-family: 'Roboto Slab', 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px; 
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  font-weight: normal;
}

h1, h2, h3 {
    font-family: 'Alfa Slab One', 'Helvetica Neue', Arial, sans-serif;
    font-size:45px;
}
*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

</style>
