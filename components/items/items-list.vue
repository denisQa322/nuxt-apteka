<script lang="ts" setup>
import ItemCard from "./item-card.vue";

import itemImg from "@/assets/images/artrosila.jpg";

defineProps({
  headerName: {
    type: String,
    required: true,
  },
});

const items = [
  {
    itemLink: "/",
    itemImg: `${itemImg}`,
    itemName: "АртроСила капс 400мг №40 упак",
    itemPrice: "4 975 ₸",
  },
  {
    itemLink: "/",
    itemImg: `${itemImg}`,
    itemName: "АртроСила капс 400мг №40 упак",
    itemPrice: "4 975 ₸",
  },
  {
    itemLink: "/",
    itemImg: `${itemImg}`,
    itemName: "АртроСила капс 400мг №40 упак",
    itemPrice: "4 975 ₸",
  },
  {
    itemLink: "/",
    itemImg: `${itemImg}`,
    itemName: "АртроСила капс 400мг №40 упак",
    itemPrice: "4 975 ₸",
  },
  {
    itemLink: "/",
    itemImg: `${itemImg}`,
    itemName: "АртроСила капс 400мг №40 упак",
    itemPrice: "4 975 ₸",
  },
];
</script>

<template>
  <div class="items container">
    <div class="items-header">
      {{ headerName }}
    </div>
    <div class="items-list">
      <ItemCard
        v-for="(item, index) in items"
        :key="index"
        :itemLink="item.itemLink"
        :itemImg="item.itemImg"
        :itemName="item.itemName"
        :itemPrice="item.itemPrice"
      />
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "@/assets/styles/tovw.scss" as *;
.items {
  margin-bottom: toVw(25px);
  &-header {
    font-size: toVw(37px);
    font-weight: 600;
    margin-bottom: toVw(15px);
  }
  &-list {
    display: flex;
    gap: toVw(10px);
  }
}
</style>
