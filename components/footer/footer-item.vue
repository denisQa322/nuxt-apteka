<script lang="ts" setup>
defineProps({
  iconSrc: {
    type: String,
    required: true,
  },
  headerText: {
    type: String,
    required: true,
  },
  infoText: {
    type: String,
    required: true,
  },
  linkUrl: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="footer-item">
    <div class="footer-item-icon">
      <img :src="iconSrc" alt="" />
    </div>
    <div class="footer-item-info">
      <div class="footer-item-info-header">
        <p>{{ headerText }}</p>
      </div>
      <div class="footer-item-info-text">
        <NuxtLink :to="linkUrl">{{ infoText }}</NuxtLink>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
@use "@/assets/styles/tovw.scss" as *;

.footer-item {
  display: flex;
  gap: toVw(14px);
  align-items: center;
  &-icon {
    margin-right: toVw(15px);
  }
  &-info {
    display: flex;
    flex-direction: column;
    gap: toVw(15px);
    font-size: toVw(17px);
    &-header {
      font-weight: 800;
      p {
        margin: 0;
      }
    }
    &-text {
      a {
        text-decoration: none;
        color: #ffffff;
        cursor: pointer;
      }
    }
  }
}
</style>
