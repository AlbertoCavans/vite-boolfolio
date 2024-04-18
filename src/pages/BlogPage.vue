<script>
import ProjectList from "../components/ProjectList.vue";

export default {
  data() {
    return {
      title: "Hello world",
    };
  },

  components: { ProjectList },
};
</script>

<template>
  <project-list />
</template>

<style lang="scss" scoped></style>
