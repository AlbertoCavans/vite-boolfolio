<script>
/* import MyComponent from "./components/MyComponent.vue" */
import AppHeader from "./components/AppHeader.vue";
import ProjectCard from "./components/ProjectCard.vue";

export default {
  data() {
    return {
      title: "Vite Boolfolio frontend",
    };
  },

  components: { AppHeader, ProjectCard },

  // components: {
  // MyComponent,
  // }
};
</script>

<template>
  <app-header />
  <div class="container">
    <h1>{{ title }}</h1>

    <project-card />
  </div>
</template>

<style lang="scss">
@use "./scss/general.scss" as *;
</style>
