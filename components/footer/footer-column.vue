<script lang="ts" setup>
defineProps({
  footerHeader: {
    type: String,
    required: false,
  },
});
</script>

<template>
  <div class="footer-column">
    <h2 v-if="footerHeader" class="footer-column-header">
      {{ footerHeader }}
    </h2>
    <slot />
  </div>
</template>

<style lang="scss" scoped>
@use "@/assets/styles/tovw.scss" as *;

.footer-column {
  &-header {
    font-size: toVw(25px);
    margin-top: toVw(40px);
    margin-bottom: toVw(75px);
  }
}
</style>
