<script>
/* import MyComponent from "./components/MyComponent.vue" */

export default {};
</script>

<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-info p-3">
    <a class="navbar-brand" href="#">Boolfolio</a>
    <button
      class="navbar-toggler"
      type="button"
      data-toggle="collapse"
      data-target="#navbarNav"
      aria-controls="navbarNav"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item active">
          <router-link :to="{ name: 'home' }" class="nav-link"
            >Home</router-link
          >
        </li>
        <li class="nav-item">
          <router-link :to="{ name: 'projects.index' }" class="nav-link"
            >Blog</router-link
          >
        </li>
      </ul>
    </div>
  </nav>
</template>

<style lang="scss" scoped></style>
