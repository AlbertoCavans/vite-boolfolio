<script>
/* import MyComponent from "./components/MyComponent.vue" */
import AppHeader from "./components/AppHeader.vue";
/* import ProjectList from "./components/ProjectList.vue"; */

export default {
  data() {
    return {
      title: "Vite Boolfolio frontend",
    };
  },

  components: { AppHeader /* ProjectList */ },

  // components: {
  // MyComponent,
  // }
};
</script>

<template>
  <app-header />
  <div class="container mt-5 pb-5">
    <h1>{{ title }}</h1>

    <router-view></router-view>
  </div>
</template>

<style lang="scss">
@use "./scss/general.scss" as *;
</style>
