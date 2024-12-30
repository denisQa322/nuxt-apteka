<script lang="ts" setup>
import LocationIcon from "@/assets/icons/location.svg";
import CallIcon from "@/assets/icons/phone.svg";
import ProfileIcon from "@/assets/icons/profile.svg";
import FavoriteIcon from "@/assets/icons/favorite-grey.svg";
import CartIcon from "@/assets/icons/cart-grey.svg";

import Buttons from "~/components/Buttons/header-buttons.vue";

const buttons = [
  { iconSrc: ProfileIcon, iconAlt: "Профиль", buttonLink: "/account" },
  { iconSrc: FavoriteIcon, iconAlt: "Избранное", buttonLink: "/favorite" },
  { iconSrc: CartIcon, iconAlt: "Корзина", buttonLink: "/cart" },
];
</script>

<template>
  <header>
    <div class="container">
      <div class="header">
        <div class="header-top">
          <div class="header-top-city">
            <img :src="LocationIcon" alt="" />
            Ваш город: <span>Алматы</span>
          </div>
          <ul class="header-top-menu">
            <li><NuxtLink to="/">Каталог</NuxtLink> <img src="" alt="" /></li>
            <li><NuxtLink to="/contacts">Контакты</NuxtLink></li>
            <li><NuxtLink to="/order">Доставка</NuxtLink></li>
            <li><NuxtLink to="/return">Условия возврата и обмена</NuxtLink></li>
          </ul>
          <div class="header-top-call">
            <a href="tel:+7 (705) 255 25 25"
              ><img :src="CallIcon" alt="" />Связаться с нами</a
            >
          </div>
        </div>
        <div class="header-bottom">
          <div class="header-bottom-logo">
            <NuxtLink to="/">
              <img src="@/assets/icons/header-logo.svg" alt="" />
            </NuxtLink>
          </div>
          <div class="header-bottom-search">
            <input type="text" placeholder="Поиск товара..." />
          </div>
          <ul class="header-bottom-buttons">
            <Buttons
              v-for="(button, index) in buttons"
              :key="index"
              :icon-src="button.iconSrc"
              :icon-alt="button.iconAlt"
              :button-link="button.buttonLink"
            />
          </ul>
          <div class="header-bottom-cart">
            <p>Моя корзина</p>
            <span> ₸</span>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use "@/assets/styles/tovw.scss" as *;

.header {
  display: flex;
  flex-direction: column;
  &-top {
    display: flex;
    justify-content: space-between;
    border-bottom: 1px solid #e1dfdf;
    padding: toVw(20px) 0;
    &-city {
      display: flex;
    }
    &-menu {
      display: flex;
      gap: 100px;
    }
  }
  &-bottom {
    display: flex;

    padding: toVw(20px) 0;
    justify-content: space-between;
  }
}
</style>
