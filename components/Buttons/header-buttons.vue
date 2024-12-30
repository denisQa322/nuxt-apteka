<script lang="ts" setup>
defineProps({
  iconSrc: {
    type: String,
    required: true,
  },
  iconAlt: {
    type: String,
    requried: true,
  },
  buttonLink: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="button">
    <NuxtLink :to="buttonLink">
      <img :src="iconSrc" :alt="iconAlt" />
    </NuxtLink>
  </div>
</template>

<style lang="scss" scoped></style>
