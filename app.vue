<script setup lang="ts"></script>

<template>
  <div>
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>

<style scoped lang="scss">
@use "@/assets/styles/tovw.scss" as *;

template {
  width: toVw(1920px);
}
</style>
