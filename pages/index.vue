<script setup lang="ts">
import Info from "~/components/info-block/info.vue";
import GoToCatalogue from "~/components/go-to-catalogue.vue";
import Mission from "~/components/mission.vue";
import FirstScreen from "~/components/first-screen/first-screen.vue";

import goToImageOne from "@/assets/images/thorne-img.png";
import goToImageTwo from "@/assets/images/сosmeticsBabyProducts.png";
import ItemsList from "~/components/items/items-list.vue";

const headerNames = [
  { headerName: "Новые продукты" },
  { headerName: "Хиты продаж" },
  { headerName: "Распродажа товаров" },
];

const goToCatalogue = [
  {
    goToHeader: "Лекарственные средства",
    goToText: "Качесво проверенное временем",
    goToImage: goToImageOne,
    goToLink: "/",
  },
  {
    goToHeader: "Товары для мамы и малыша",
    goToText: "С заботой о самом важном",
    goToImage: goToImageTwo,
    goToLink: "/",
  },
];
</script>

<template>
  <FirstScreen />
  <Info />
  <ItemsList :headerName="headerNames[0].headerName" />
  <GoToCatalogue
    :go-to-header="goToCatalogue[0].goToHeader"
    :go-to-text="goToCatalogue[0].goToText"
    :go-to-image="goToCatalogue[0].goToImage"
    :go-to-link="goToCatalogue[0].goToLink"
  />
  <ItemsList :header-name="headerNames[1].headerName" />

  <GoToCatalogue
    :go-to-header="goToCatalogue[1].goToHeader"
    :go-to-text="goToCatalogue[1].goToText"
    :go-to-image="goToCatalogue[1].goToImage"
    :go-to-link="goToCatalogue[1].goToLink"
  />
  <ItemsList :header-name="headerNames[2].headerName" />
  <Mission />
</template>

<style scoped lang="scss"></style>
