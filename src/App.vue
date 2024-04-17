<script>
/* import MyComponent from "./components/MyComponent.vue" */

export default {
  data() {
    return {
      title: "Vite Boolfolio frontend",
    };
  },

  // components: {
  // MyComponent,
  // }
};
</script>

<template>
  <h1>{{ title }}</h1>
</template>

<style lang="scss">
@use "./scss/general.scss" as *;
</style>
