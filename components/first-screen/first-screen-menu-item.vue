<script lang="ts" setup>
defineProps({
  itemLink: {
    type: String,
    required: true,
  },
  iconSrc: {
    type: String,
    required: true,
  },
  itemName: {
    type: String,
    required: true,
  },
  itemBackgroundColor: {
    type: String,
    required: false,
  },
});
</script>

<template>
  <li :style="{ backgroundColor: itemBackgroundColor }" class="menu-item">
    <NuxtLink class="menu-item-link" :to="itemLink">
      <img :src="iconSrc" alt="" />
      <p>{{ itemName }}</p>
    </NuxtLink>
  </li>
</template>

<style lang="scss" scoped>
@use "@/assets/styles/tovw.scss" as *;

.menu-item {
  border-bottom: 1px solid grey;
  &-link {
    padding: toVw(19px) toVw(26px);
    display: flex;
    align-items: center;
    height: toVw(88.5px);
    img {
      width: toVw(50px);
      margin-right: toVw(20px);
    }
    p {
      font-size: toVw(19px);
      font-weight: 600;
    }
  }
  &:nth-last-child(1) {
    border-bottom: none;
  }
}
</style>
