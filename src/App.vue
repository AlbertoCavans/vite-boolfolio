<script>
/* import MyComponent from "./components/MyComponent.vue" */
import axios from "axios";

export default {
  data() {
    return {
      title: "Vite Boolfolio frontend",
      projects: [],
    };
  },

  created() {
    axios.get("http://http://127.0.0.1:8000/api/projects").then((response) => {
      this.projects = response.data.data;
    });
  },

  // components: {
  // MyComponent,
  // }
};
</script>

<template>
  <div class="container">
    <h1>{{ title }}</h1>
  </div>
</template>

<style lang="scss">
@use "./scss/general.scss" as *;
</style>
