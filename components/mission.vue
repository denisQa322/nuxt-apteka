<script lang="ts" setup></script>

<template>
  <section class="misson">
    <div class="mission-container">
      <div class="mission-header">Наша миссия</div>
      <div class="mission-description">
        Аптечная сеть «Аптечный Дом» - это многопрофильные центры здоровья и
        красоты, где наша высококвалифицированная команда поможет закрыть
        потребность клиента в заботе о самом ценном – здоровье.
      </div>
      <div class="mission-text">
        <div class="mission-text-header">Сеть аптек «Аптечный дом»</div>
        <span>Аптечный Дом – Здоровье с доставкой до дверей </span>
        <div class="mission-text-description">
          <span>«Аптечный Дом»</span> - это сеть аптек, которая заботится о
          вашем здоровье и делает покупку медикаментов удобной и безопасной. Мы
          предлагаем широкий ассортимент сертифицированных препаратов и
          осуществляем массовую доставку прямо к вашим дверям в Алматы.
        </div>
        <div class="mission-text-why-dom">
          <div class="mission-text-why-dom-header">
            Почему выбрают «Аптечный Дом»?
          </div>
          <ul class="mission-text-why-dom-list">
            <li>
              <span>Широкий ассортимент:</span>у нас вы найдете все необходимое
              — от лекарств и товаров для здоровья до медицинской техники и
              косметики.
            </li>
            <li>
              <span>Круглосуточный заказ и доставка:</span>забудьте в очереди —
              заказывайте лекарства и медицинские товары онлайн в любое время
              суток. Доставка по Алматы день в день!
            </li>
            <li>
              <span>Только сертифицированные препараты:</span>весь ассортимент
              соответствует строгим стандартам качества и срокам годности.
            </li>
            <li>
              <span>Удобные варианты оплаты:</span>оплачивайте онлайн, наличными
              или картой при получении — как вам удобно.
            </li>
          </ul>
        </div>
        <div class="mission-text-goods">
          <div class="mission-text-goods-header">Наш ассортимент</div>
          <span>В «Аптечном Доме» вы всегда найдете: </span>
          <ul class="mission-text-goods-list">
            <NuxtLink to="/"
              >Медикаменты для лечения и профилактики заболеваний</NuxtLink
            >
            <NuxtLink to="/">Витамины и БАДы для поддержания здоровья</NuxtLink>
            <NuxtLink to="/"
              >Товары для матери и ребенка — от детского питания до уходовой
              косметики</NuxtLink
            >
            <NuxtLink to="/"
              >Косметика и средства гигиены для всей семьи</NuxtLink
            >
            <NuxtLink to="/"
              >Медицинскую технику для домашнего использования (термометры,
              тонометры и др.)</NuxtLink
            >
          </ul>
        </div>
        <div class="mission-text-general-info">
          <p>
            Работа о здоровье стала проще с «Аптечным Домом»! Не тратьте время
            на поиски — мы рядом и готовы помочь вам 24/7. Сделайте заказ прямо
            сейчас и получайте лекарства быстро, удобно и безопасно!
          </p>
          <span>Аптечный Дом — всегда рядом, когда важно. </span>
        </div>
      </div>
      <div class="mission-img">
        <img src="../assets/images/apteka.png" alt="apteka" />
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@use "@/assets/styles/tovw.scss" as *;
.mission {
  .container {
    .mission-header {
    }
    .mission-description {
    }
    .mission-text {
      &-header {
      }
      &-description {
      }
      &-why-dom {
        &-header {
        }
        &-list {
          li {
            span {
            }
          }
        }
      }
      &-goods {
        &-header {
        }
        &-list {
        }
      }
      &-general-info {
        p {
        }
        span {
        }
      }
    }
    .mission-img {
      width: toVw(660px);
      height: toVw(400px);
    }
  }
}
</style>
