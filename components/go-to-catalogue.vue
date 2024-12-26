<script lang="ts" setup>
defineProps({
  goToHeader: {
    type: String,
    required: true,
  },
  goToText: {
    type: String,
    required: true,
  },
  goToLink: {
    type: String,
    required: true,
  },
  goToImage: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="go-to-catalogue container">
    <div class="go-to-catalogue-info">
      <div class="go-to-catalogue-info-header">
        {{ goToHeader }}
      </div>
      <div class="go-to-catalogue-info-text">
        {{ goToText }}
      </div>
      <div class="go-to-catalogue-info-button">
        <NuxtLink to="/">ПЕРЕЙТИ В КАТАЛОГ</NuxtLink>
      </div>
    </div>
    <div class="go-to-catalogue-img">
      <img :src="goToImage" alt="" />
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "@/assets/styles/tovw.scss" as *;

.go-to-catalogue {
  padding: toVw(40px);
  background: url("../assets/images/backgroundGoTo.svg");
  background-size: cover;
  background-repeat: no-repeat;
  display: flex;
  justify-content: space-between;
  margin-bottom: toVw(20px);
  &-info {
    color: #ffffff;
    &-header {
      font-size: toVw(37px);
      margin-bottom: toVw(16px);
    }
    &-text {
      font-size: toVw(17px);
      margin-bottom: toVw(36px);
    }
    &-button {
      a {
        font-size: toVw(17px);
        padding: toVw(20px) toVw(40px);
        width: toVw(300px);
        background-color: #ffffff;
        border-radius: toVw(5px);
        color: black;
        cursor: pointer;
        text-decoration: none;
      }
    }
  }
  &-img {
    img {
      width: toVw(300px);
      height: toVw(240px);
    }
  }
}
</style>
