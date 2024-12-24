<script lang="ts" setup>
import FooterItem from "./footer-item.vue";

import locationIcon from "@/assets/images/location.svg";
import phoneIcon from "@/assets/images/phone.svg";
import emailIcon from "@/assets/images/email.svg";
import clockIcon from "@/assets/images/clock.svg";

const footerItems = [
  {
    iconSrc: `${locationIcon}`,
    headerText: "Адрес",
    infoText: "Алматы, проспект Суюнбая 2, корпус 4(за торговым центром Мерей)",
    linkUrl: "#",
  },
  {
    iconSrc: `${phoneIcon}`,
    headerText: "Телефон",
    infoText: "+7 (705) 255 25 25",
    linkUrl: "tel:+7 (705) 255 25 25",
  },
  {
    iconSrc: `${emailIcon}`,
    headerText: "Email",
    infoText: "info@keremetprojects.com",
    linkUrl: "mailto: info@keremetprojects.com",
  },
  {
    iconSrc: `${clockIcon}`,
    headerText: "Режим работы",
    infoText: "Круглосуточно",
    linkUrl: "#",
  },
];
</script>

<template>
  <section class="container">
    <footer>
      <div class="footer-first-column">
        <div class="footer-first-column-logo">
          <NuxtLink to="/">
            <img src="" alt="" />
          </NuxtLink>
        </div>
        <div class="footer-first-column-items">
          <FooterItem
            v-for="(item, index) in footerItems"
            :key="index"
            :iconSrc="item.iconSrc"
            :headerText="item.headerText"
            :infoText="item.infoText"
            :linkUrl="item.linkUrl"
          />
        </div>
      </div>
    </footer>
  </section>
</template>

<style lang="scss" scoped>
.footer-first-column {
  &-logo {
  }
  &-items {
    display: flex;
    flex-direction: column;
    gap: 25px;
  }
}
</style>
