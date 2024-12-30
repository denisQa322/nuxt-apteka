<script lang="ts" setup>
defineProps({
  iconSrc: { type: String, required: true },
  iconLink: { type: String, required: true },
  iconBackgroundColor: { type: String, required: false },
});
</script>

<template>
  <div class="button">
    <NuxtLink
      class="cart-button"
      :style="{ backgroundColor: iconBackgroundColor }"
      :href="iconLink"
    >
      <img :src="iconSrc" alt="" />
    </NuxtLink>
  </div>
</template>

<style lang="scss" scoped>
@use "@/assets/styles/tovw.scss" as *;
.button {
  .cart-button {
    border-radius: 50%;
    padding: toVw(12px);
    border: toVw(1px) solid #71bf44;
    display: flex;
    align-items: center;
    img {
      width: toVw(25px);
      height: toVw(25px);
    }
  }
}
</style>
