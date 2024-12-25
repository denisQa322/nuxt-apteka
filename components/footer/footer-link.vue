<script lang="ts" setup>
defineProps({
  linkText: {
    type: String,
    required: true,
  },
  linkUrl: {
    type: String,
    required: false,
  },
});
</script>

<template>
  <div class="footer-second-column-link">
    <NuxtLink :to="linkUrl">
      <img src="../../assets/icons/arrow.svg" alt="" />
      <span>{{ linkText }}</span>
    </NuxtLink>
  </div>
</template>

<style lang="scss" scoped>
@use "@/assets/styles/tovw.scss" as *;

.footer-second-column-link {
  a {
    color: #ffffff;
    cursor: pointer;
    text-decoration: none;
    img {
      width: toVw(13px);
      height: toVw(13px);
      rotate: -90deg;
      margin-right: toVw(10px);
      transition: transform 0.4s ease;
    }
    span {
      font-size: toVw(17px);
    }
  }
  &:hover img {
    transform: translateY(toVw(10px));
  }
}
</style>
