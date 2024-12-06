<template>
  <article class="prose dark:prose-invert">
    <ContentDoc />
  </article>
</template>
<script setup>
import { useRoute } from "vue-router";
const route = useRoute();
console.log(route.params.slug);
</script>
