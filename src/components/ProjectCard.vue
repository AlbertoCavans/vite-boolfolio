<script>
/* import MyComponent from "./components/MyComponent.vue" */

export default {
  props: { project: Object },
  computed: {
    abstract() {
      const description = this.project.description;
      return description.length > 40
        ? description.substr(0, 40) + "..."
        : description;
    },
  },
};
</script>

<template>
  <div class="col">
    <div class="card h-100">
      <img
        class="card-img-top"
        alt="..."
        :src="project.img ? project.img : 'https://placehold.co/600x400'"
      />
      <div class="card-body">
        <h5 class="card-title">{{ project.name_project }}</h5>
        <p>
          <strong
            class="text-white py-1"
            :style="'background-color: ' + project.type.color"
            >Type project: </strong
          >{{ project.type.label }}
        </p>
        <p class="card-text">{{ abstract }}</p>
        <a href="#" class="btn btn-primary">Go somewhere</a>
      </div>
      <div class="card-footer">
        <span
          v-for="technology in project.technologies"
          class="text-white mx-1 p-1"
          :style="'background-color: ' + technology.color_label"
          >{{ technology.name }}</span
        >
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
