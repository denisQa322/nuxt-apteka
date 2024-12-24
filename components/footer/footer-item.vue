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
.footer-item {
  display: flex;
  gap: 14px;
  align-items: center;
  &-icon {
    margin-right: 15px;
    img {
      width: 15px;
      height: 15px;
    }
  }
  &-info {
    display: flex;
    flex-direction: column;
    gap: 15px;
    font-size: 14px;
    &-header {
      font-weight: 800;
      p {
        margin: 0;
      }
    }
    &-text {
      a {
        text-decoration: none;
        color: black;
        cursor: pointer;
      }
    }
  }
}
</style>
