<script>
import axios from "axios";
import { api } from "../store";
import ProjectCard from "../components/ProjectCard.vue";

export default {
  data() {
    return {
      project: null,
    };
  },

  components: { ProjectCard },

  created() {
    const projectSlug = this.$route.params.slug;
    axios.get(api.baseUrl + `projects/${projectSlug}`).then((response) => {
      this.project = response.data;
    });
  },
};
</script>

<template>
  <!-- <h2>Project Details: {{ $route.params.slug }}</h2> -->
  <div class="row">
    <project-card v-if="project" :project="project" :isDetail="true" />
  </div>
</template>

<style lang="scss" scoped></style>
