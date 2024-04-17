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

    <div v-for="project in projects">
      <ul>
        <li><strong>Title: </strong>{{ project.name_project }}</li>
        <li><strong>Description: </strong>{{ project.description }}</li>
      </ul>
    </div>
  </div>
</template>

<style lang="scss">
@use "./scss/general.scss" as *;
</style>
