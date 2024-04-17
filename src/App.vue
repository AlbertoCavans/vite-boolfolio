<script>
/* import MyComponent from "./components/MyComponent.vue" */
import axios from "axios";
import { api, store } from "./store";

import AppHeader from "./components/AppHeader.vue";

export default {
  data() {
    return {
      store,
      title: "Vite Boolfolio frontend",
    };
  },

  components: { AppHeader },

  created() {
    axios.get(api.baseUrl + "projects").then((response) => {
      store.projects = response.data.data;
    });
  },

  // components: {
  // MyComponent,
  // }
};
</script>

<template>
  <app-header />
  <div class="container">
    <h1>{{ title }}</h1>

    <div v-for="project in store.projects">
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
