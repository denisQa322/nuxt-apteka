<script lang="ts" setup>
import firstScreenMenuItem from "./first-screen-menu-item.vue";
import LekarstvaIcon from "@/assets/icons/lekarstva.svg";
import IzdeliyaIcon from "@/assets/icons/izdeliya.svg";
import TechnikaIcon from "@/assets/icons/technika.svg";
import GigienaIcon from "@/assets/icons/gigiena.svg";
import BadyIcon from "@/assets/icons/bady.svg";
import PharmamaIcon from "@/assets/icons/pharmama.svg";
import IntimIcon from "@/assets/icons/intim.svg";
import SliderImg from "@/assets/images/slider-img-1.jpeg";

const items = [
  {
    itemLink: "/",
    itemName: "Лекарственные средства",
    iconSrc: LekarstvaIcon,
  },
  {
    itemLink: "/",
    itemName: "Изделия медицинского назначения",
    iconSrc: IzdeliyaIcon,
  },
  {
    itemLink: "/",
    itemName: "Медтехника",
    iconSrc: TechnikaIcon,
  },
  {
    itemLink: "/",
    itemName: "Красота и гигиена",
    iconSrc: GigienaIcon,
  },
  {
    itemLink: "/",
    itemName: "Витамины и БАДы",
    iconSrc: BadyIcon,
  },
  {
    itemLink: "/",
    itemName: "PharMama",
    iconSrc: PharmamaIcon,
  },
  {
    itemLink: "/",
    itemName: "Интим отдел 18+",
    iconSrc: IntimIcon,
    itemBackgroundColor: "#e269cd",
  },
];
</script>

<template>
  <div class="first-screen-wrapper">
    <div class="first-screen container">
      <ul class="first-screen-menu">
        <firstScreenMenuItem
          v-for="(item, index) in items"
          :key="index"
          :item-link="item.itemLink"
          :item-name="item.itemName"
          :icon-src="item.iconSrc"
          :item-background-color="item.itemBackgroundColor"
        />
      </ul>
      <div class="first-screen-slider">
        <div class="first-screen-slider-images">
          <img :src="SliderImg" alt="" />
        </div>
        <div class="first-screen-slider-buttons"></div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "@/assets/styles/tovw.scss" as *;

.first-screen-wrapper {
  margin-top: toVw(20px);
  padding-bottom: toVw(25px);
  .first-screen {
    display: flex;
    gap: toVw(80px);
    &-menu {
      display: flex;
      flex-direction: column;
      padding: toVw(20px);
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    }
    &-slider {
      &-images {
        img {
          width: toVw(1150px);
        }
      }
    }
  }
}
</style>
