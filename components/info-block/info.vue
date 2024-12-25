<script lang="ts" setup>
import infoItem from "./infoItem.vue";

import locationIcon from "@/assets/icons/infoLocation.svg";
import deliveryIcon from "@/assets/icons/delivery.svg";
import walletIcon from "@/assets/icons/wallet.svg";
import originalIcon from "@/assets/icons/original.svg";

const infoItems = [
  {
    infoIcon: `${locationIcon}`,
    infoHeader: "Сеть Аптек",
    infoDescription: "Мы работаем по всему Казахстану",
  },
  {
    infoIcon: `${deliveryIcon}`,
    infoHeader: "СЕРВИС ДОСТАВКИ",
    infoDescription: "Отправка в любой город Казахстана",
  },
  {
    infoIcon: `${walletIcon}`,
    infoHeader: "Удобная оплата",
    infoDescription: "Оплата при получении или на счет",
  },
  {
    infoIcon: `${originalIcon}`,
    infoHeader: "15000 наименований",
    infoDescription: "Более 15000 товаров от производителя",
  },
];
</script>

<template>
  <section class="info">
    <div class="info-block container">
      <div class="info-block-items">
        <infoItem
          v-for="(item, index) in infoItems"
          :key="index"
          :infoIcon="item.infoIcon"
          :infoHeader="item.infoHeader"
          :infoDescription="item.infoDescription"
        />
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@use "@/assets/styles/tovw.scss" as *;

.info {
  color: #ffffff;
  background-color: #575a5b;
  padding: toVw(28px);
  .info-block {
    &-items {
      display: flex;
      gap: toVw(10px);
    }
  }
}
</style>
