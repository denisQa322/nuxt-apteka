<script lang="ts" setup></script>

<template>
  <div class="mission">
    <div class="container">
      <div class="mission-header">Наша миссия</div>
      <div class="mission-description">
        Аптечная сеть «Аптечный Дом» - это многопрофильные центры здоровья и
        красоты, где наша высококвалифицированная команда поможет закрыть
        потребность клиента в заботе о самом ценном – здоровье.
      </div>
      <div class="mission-info-and-img">
        <div class="mission-general-info">
          <div class="mission-general-info-text">
            <div>Сеть аптек «Аптечный дом»</div>
          </div>
          <div class="mission-general-info-description">
            <div>Аптечный Дом – Здоровье с доставкой до дверей</div>
            <p>
              <span> «Аптечный Дом»</span>— это сеть аптек, которая заботится о
              вашем здоровье и делает покупку медикаментов удобной и безопасной.
              Мы предлагаем широкий ассортимент сертифицированных препаратов и
              осуществляем массовую доставку прямо к вашим дверям в Алматы.
            </p>
          </div>
          <div class="mission-general-info-why">
            <div class="mission-general-info-why-text">
              Почему выбирают «Аптечный Дом»?
            </div>
            <ul class="mission-general-info-why-description">
              <li>
                <span>Широкий ассортимент:</span> у нас вы найдете все
                необходимое — от лекарств и товаров для здоровья до медицинской
                техники и косметики.
              </li>
              <li>
                <span>Круглосуточный заказ и доставка:</span> забудьте в очереди
                — заказывайте лекарства и медицинские товары онлайн в любое
                время суток. Доставка по Алматы день в день!
              </li>
              <li>
                <span>Только сертифицированные препараты:</span> весь
                ассортимент соответствует строгим стандартам качества и срокам
                годности.
              </li>
              <li>
                <span>Удобные варианты оплаты:</span> оплачивайте онлайн,
                наличными или картой при получении — как вам удобно.
              </li>
            </ul>
          </div>
          <div class="mission-general-info-stock">
            <div>Наш ассортимент</div>
            <ol>
              В «Аптечном Доме» вы всегда найдете:
              <li>
                <NuxtLink to="/"
                  >Медикаменты для лечения и профилактики заболеваний
                </NuxtLink>
              </li>
              <li>
                <NuxtLink to="/"
                  >Витамины и БАДы для поддержания здоровья</NuxtLink
                >
              </li>
              <li>
                <NuxtLink to="/"
                  >Товары для матери и ребенка — от детского питания до уходовой
                  косметики
                </NuxtLink>
              </li>
              <li>
                <NuxtLink to="/"
                  >Косметика и средства гигиены для всей семьи
                </NuxtLink>
              </li>
              <li>
                <NuxtLink to="/"
                  >Медицинскую технику для домашнего использования (термометры,
                  тонометры и др.)
                </NuxtLink>
              </li>
            </ol>
          </div>
          <p class="mission-general-info-work">
            Работа о здоровье стала проще с «Аптечным Домом»! Не тратьте время
            на поиски — мы рядом и готовы помочь вам 24/7. Сделайте заказ прямо
            сейчас и получайте лекарства быстро, удобно и безопасно!
          </p>
          <div class="mission-general-info-comment">
            Аптечный Дом — всегда рядом, когда важно.
          </div>
        </div>
        <div class="mission-img">
          <img src="../assets/images/apteka.png" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "@/assets/styles/tovw.scss" as *;

.mission {
  margin-bottom: toVw(50px);
  .container {
    padding-top: toVw(25px);
    border-top: 1px solid #e7e7e7;
    .mission-header {
      font-size: toVw(24px);
      font-weight: 600;
      margin-bottom: toVw(10px);
    }
    .mission-description {
      font-size: toVw(16px);
      margin-bottom: toVw(30px);
    }
    .mission-info-and-img {
      display: flex;
      justify-content: space-between;
      align-items: center;
      .mission-general-info {
        &-text {
          font-size: toVw(24px);
          margin-bottom: toVw(20px);
          font-weight: 600;
        }
        &-description {
          div {
            font-size: toVw(24px);
            margin-bottom: toVw(20px);
            font-weight: 600;
          }
          p {
            font-size: toVw(18px);
            margin-bottom: toVw(40px);
            span {
              font-weight: 600;
            }
          }
        }
        &-why {
          &-text {
            font-weight: 600;
            font-size: toVw(24px);
            margin-bottom: toVw(20px);
          }
          &-description {
            list-style-type: none;
            font-size: toVw(18px);
            display: flex;
            flex-direction: column;
            gap: toVw(10px);
            margin-bottom: toVw(40px);
            li {
              span {
                font-weight: 600;
              }
            }
          }
        }
        &-stock {
          margin-bottom: toVw(40px);
          div {
            font-weight: 600;
            font-size: toVw(24px);
            margin-bottom: toVw(20px);
          }
          ol {
            font-size: toVw(24px);
            display: flex;
            flex-direction: column;
            gap: toVw(10px);
            li {
              margin-left: toVw(25px);
              a {
                margin-top: toVw(20px);
                color: #000000;
                cursor: pointer;
              }
            }
          }
        }
        &-work {
          font-size: toVw(18px);
          margin-bottom: toVw(20px);
        }
        &-comment {
          font-weight: 600;
          font-size: toVw(24px);
        }
      }
      .mission-img {
        img {
          width: toVw(660px);
          height: toVw(400px);
          border-radius: toVw(29px) 0;
          box-shadow: toVw(26px) toVw(24px) 0 toVw(7px) #e7e7e7;
        }
      }
    }
  }
}
</style>
