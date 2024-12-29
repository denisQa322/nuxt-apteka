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
  hoverIconSrc:{
    type: String,
    required: false
  }
});
</script>

<template>
  <li :style="{ backgroundColor: itemBackgroundColor }" class="menu-item">
    <NuxtLink class="menu-item-link" :to="itemLink">
      <div class="visible-on-hover">
            <img :src="hoverIconSrc" alt="">
      </div>
      <div class="always-visible">
        <img :src="iconSrc" alt="" />
      </div>
      {{ itemName }}
    </NuxtLink>
  </li>
</template>

<style lang="scss" scoped>
@use "@/assets/styles/tovw.scss" as *;

.menu-item {
  border-bottom: 1px solid grey;
  &-link {
    padding: toVw(26px);
    display: flex;
    align-items: center;
    height: toVw(85px);
    font-size: toVw(19px);
    font-weight: 600;
    color: #000000;
    img {
      width: toVw(50px);
      margin-right: toVw(20px);
    }
    .visible-on-hover{
      display: none;
    }
    &:hover{
      background-color: #f2f8f5;
    }
  }
  &:nth-last-child(1) {
    border-bottom: none;
    &:hover{

      .always-visible{
        display: none;
      }
      .visible-on-hover{
        display: block;
        width: toVw(50px);
        margin-right: toVw(20px);
      }
      }
  }
}
</style>
