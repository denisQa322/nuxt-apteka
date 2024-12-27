<script lang="ts" setup>
import FooterItem from "./footer-item.vue";
import FooterLink from "./footer-link.vue";
import FooterColumn from "./footer-column.vue";

import locationIcon from "@/assets/icons/location.svg";
import phoneIcon from "@/assets/icons/phone.svg";
import emailIcon from "@/assets/icons/email.svg";
import clockIcon from "@/assets/icons/clock.svg";

const footerHeaders = [
  { footerHeader: "Общая информация" },
  { footerHeader: "Для покупателя" },
  { footerHeader: "Полезные статьи" },
];

const footerItems = [
  {
    iconSrc: locationIcon,
    headerText: "Адрес",
    infoText:
      "Алматы, проспект Суюнбая 2, корпус 4 (за торговым\n центром Мерей)",
    linkUrl: "/contacts",
  },
  {
    iconSrc: phoneIcon,
    headerText: "Телефон",
    infoText: "+7 (705) 255 25 25",
    linkUrl: "tel:+7 (705) 255 25 25",
  },
  {
    iconSrc: emailIcon,
    headerText: "Email",
    infoText: "info@keremetprojects.com",
    linkUrl: "mailto: info@keremetprojects.com",
  },
  {
    iconSrc: clockIcon,
    headerText: "Режим работы",
    infoText: "Круглосуточно",
    linkUrl: "/contacts",
  },
];

const secondColumn = [
  { linkText: "Адреса аптек", linkUrl: "/contacts" },
  { linkText: "Новости / блог", linkUrl: "/articles" },
  { linkText: "Вакансии / карьера", linkUrl: "/career" },
];

const thirdColumn = [
  {
    linkText: "Личный кабинет",
    linkUrl: "/account",
  },
  {
    linkText: "Доставка/ как сделать заказ",
    linkUrl: "/order",
  },
  {
    linkText: "Условия возврата и обмена",
    linkUrl: "/return",
  },
  {
    linkText: "Бонусы",
    linkUrl: "/bonuses",
  },
];
</script>

<template>
  <footer>
    <div class="container">
      <FooterColumn>
        <div class="footer-column-logo">
          <NuxtLink to="/">
            <img src="../../assets/images/logo-footer.svg" alt="" />
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
      </FooterColumn>
      <FooterColumn :footer-header="footerHeaders[0].footerHeader">
        <ul class="footer-column-links">
          <FooterLink
            v-for="(item, index) in secondColumn"
            :key="index"
            :linkText="item.linkText"
            :linkUrl="item.linkUrl"
          />
        </ul>
      </FooterColumn>
      <FooterColumn :footer-header="footerHeaders[1].footerHeader">
        <ul class="footer-column-links">
          <FooterLink
            v-for="(item, index) in thirdColumn"
            :key="index"
            :linkText="item.linkText"
            :linkUrl="item.linkUrl"
          />
        </ul>
      </FooterColumn>
      <FooterColumn :footer-header="footerHeaders[2].footerHeader">
        <h2 class="footer-column-text">Скоро ожидается</h2>
      </FooterColumn>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
@use "@/assets/styles/tovw.scss" as *;

footer {
  width: toVw(1920px);
  background-color: #575a5b;
  padding: toVw(45px);
  color: #ffffff;
  .container {
    display: flex;
    gap: toVw(90px);
    .footer-column {
      margin: 0;
      &-logo {
        margin-bottom: toVw(45px);
        a {
          img {
            width: toVw(395px);
            height: toVw(98px);
          }
        }
      }
    }
    .footer-first-column-items {
      display: flex;
      flex-direction: column;
      gap: toVw(25px);
    }
    .footer-column {
      &-links {
        display: flex;
        flex-direction: column;
        gap: toVw(25px);
      }

      &-text {
        font-size: toVw(27px);
        font-weight: 400;
      }
    }
  }
}
</style>
