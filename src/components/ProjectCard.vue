<script>
import { api, store } from "../store";
import axios from "axios";

export default {
  data() {
    return {
      store,
    };
  },
  created() {
    axios.get(api.baseUrl + "projects").then((response) => {
      store.projects = response.data.data;
    });
  },
};
</script>

<template>
  <div class="card" v-for="project in store.projects">
    <img class="card-img-top" :src="project.img" alt="..." />
    <div class="card-body">
      <h5 class="card-title">{{ project.name_project }}</h5>
      <p class="card-text">{{ project.description }}</p>
      <a href="#" class="btn btn-primary">Go somewhere</a>
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
