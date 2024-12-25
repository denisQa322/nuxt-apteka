<script setup lang="ts">
import Info from "~/components/info-block/info.vue";
import GoToCatalogue from "~/components/goToCatalogue.vue";
import Mission from "~/components/mission.vue";

import goToImageOne from "@/assets/images/thorne-img.png";
import goToImageTwo from "@/assets/images/сosmeticsBabyProducts.png";

const goToCatalogue = [
  {
    goToHeader: "Лекарственные средства",
    goToText: "Качесво проверенное временем",
    goToImage: `${goToImageOne}`,
    goToLink: "/",
  },
  {
    goToHeader: "Товары для мамы и малыша",
    goToText: "С заботой о самом важном",
    goToImage: `${goToImageTwo}`,
    goToLink: "/",
  },
];
</script>

<template>
  <Info />
  <GoToCatalogue
    :go-to-header="goToCatalogue[0].goToHeader"
    :go-to-text="goToCatalogue[0].goToText"
    :go-to-image="goToCatalogue[0].goToImage"
    :go-to-link="goToCatalogue[0].goToLink"
  />

  <GoToCatalogue
    :go-to-header="goToCatalogue[1].goToHeader"
    :go-to-text="goToCatalogue[1].goToText"
    :go-to-image="goToCatalogue[1].goToImage"
    :go-to-link="goToCatalogue[1].goToLink"
  />
  <Mission />
</template>

<style scoped lang="scss"></style>
