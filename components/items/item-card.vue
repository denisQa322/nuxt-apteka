<script lang="ts" setup>
defineProps({
  itemLink: {
    type: String,
    required: true,
  },
  itemImg: {
    type: String,
    required: false,
  },
  itemName: {
    type: String,
    requited: true,
  },
  itemPrice: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="item">
    <NuxtLink class="item-info" :to="itemLink">
      <div class="item-info-img">
        <img :src="itemImg" alt="" />
      </div>
      <div class="item-info-name">{{ itemName }}</div>
      <div class="item-info-price">{{ itemPrice }}</div>
    </NuxtLink>
    <div class="item-buttons">
      <div class="favourite-button">
        <a href="/">
          <img src="" alt="" />
        </a>
      </div>
      <div class="add-to-cart-button">
        <a href="/">
          <img src="" alt="" />
        </a>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "@/assets/styles/tovw.scss" as *;

.item {
  border: toVw(1px) solid #eaeaea;
  width: toVw(350px);
  padding: toVw(20px) toVw(25px);
  &-info,
  a {
    text-decoration: none;
    color: black;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-bottom: toVw(20px);
    &-img {
      margin-bottom: toVw(20px);
      img {
        width: toVw(250px);
        height: toVw(200px);
      }
    }
    &-name {
      font-size: toVw(16px);
      margin-bottom: toVw(10px);
      font-weight: 600;
    }
    &-price {
      font-size: toVw(26px);
      font-weight: 600;
      color: #71bf44;
    }
  }
  &-buttons {
    display: flex;
    justify-content: space-between;
    .favourite-button {
      width: toVw(50px);
      border-radius: 50%;
      a {
        height: toVw(50px);
        background-color: #71bf44;
      }
    }
    .add-to-cart-button {
      width: toVw(50px);
      border-radius: 50%;
      a {
        height: toVw(50px);
        background-color: #71bf44;
      }
    }
  }
}
</style>
