<template>
  <div>
    <Header />
    <slot />
    <Footer />
  </div>
</template>

<script setup lang="ts">
import Footer from "~/components/footer/footer.vue";
import Header from "~/components/header/header.vue";
</script>
<style scoped></style>
