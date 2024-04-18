<script>
export default {
  props: { pagination: Array },
};
</script>

<template>
  <nav aria-label="Page navigation example" class="my-3">
    <ul class="pagination">
      <li
        @click="$emit('change-page', link.url)"
        :class="{
          active: link.active,
          disabled: !link.url,
        }"
        class="page-item"
        v-for="link in pagination"
      >
        <a class="page-link" href="#" v-html="link.label"></a>
      </li>
    </ul>
  </nav>
</template>

<style lang="scss" scoped></style>
