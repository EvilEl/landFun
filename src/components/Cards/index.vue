<template >
  <div class="card">
    <div class="card__container _container">
      <div class="card__column">
        <a href="/" class="card__item" v-for="card in cardData" :key="card.type">
          <div class="card__body">
            <div class="card__body-tarif">{{card.type}}</div>
            <div class="card__body-price">
              <span class="card__body-price-dol">$</span>
              {{card.price}}
              <span class="card__body-price-mon">/mo</span>
            </div>
            <div class="card__body-psd card__body-text">{{card.psd}}</div>
            <div class="card__body-support card__body-text">{{card.support}}</div>
            <div class="card__body-install card__body-text">{{card.insstall}}</div>
            <div class="card__body-element card__body-text">{{card.element}}</div>
          </div>
          <div class="card__button">
            <UiButton class="card__btn" :widthButton="138" :heightButton="49" title="Subscribe" />
          </div>
        </a>
      </div>
    </div>
  </div>
</template>
<script>
import UiButton from "../Ui/UiButton.vue";
export default {
  components: { UiButton },
  data: () => ({
    cardData: [
      {
        type: "Freelancer",
        price: "19",
        psd: "5 Psd fles included",
        support: "24 hours free support",
        install: "Multiple features installed",
        element: "100 Elements PSD + Al",
      },
      {
        type: "Corporate",
        price: "24",
        psd: "5 Psd fles included",
        support: "24 hours free support",
        install: "Multiple features installed",
        element: "100 Elements PSD + Al",
      },
      {
        type: "Agency",
        price: "25",
        psd: "5 Psd fles included",
        support: "24 hours free support",
        install: "Multiple features installed",
        element: "100 Elements PSD + Al",
      },
      {
        type: "Enterprise",
        price: "15",
        psd: "5 Psd fles included",
        support: "24 hours free support",
        install: "Multiple features installed",
        element: "100 Elements PSD + Al",
      },
    ],
  }),
};
</script>
<style lang="scss">
.card {
  padding: 79px 0 49px 0;
  background: #2c353e;
  &__column {
    display: flex;
    & > *:not(:last-child) {
      margin-right: 85px;
    }
  }
  &__item {
    display: block;
    text-decoration: none;
    flex: 0 1 18.1%;
    &:hover {
      .card__btn {
        .ui-btn {
          background: rgb(144, 100, 112);
        }
      }
    }
  }
  &__body {
    max-width: 206px;
    & > *:not(:last-child) {
      margin-bottom: 15px;
    }
    &-tarif {
      font-style: normal;
      font-weight: 600;
      font-size: 21px;
      line-height: 150%;
      color: #ffffff;
    }
    &-price {
      display: flex;
      font-size: 38px;
      font-weight: 400;
      line-height: calc(45 / 38 * 100%);
      color: #ffffff;
      align-self: center;
      &-dol {
        display: inline-block;
        font-size: 16px;
        line-height: 160%;
        color: #ffffff;
      }
      &-mon {
        display: inline-block;
        font-weight: normal;
        font-size: 16px;
        line-height: 160%;
        color: #ffffff;
        align-self: flex-end;
      }
    }
    &-psd {
      font-family: Work Sans;
      font-style: normal;
      font-weight: normal;
      font-size: 16px;
      line-height: 160%;
      color: #ffffff;
      opacity: 0.7;
    }
    &-text {
      font-style: normal;
      font-weight: normal;
      font-size: 16px;
      line-height: 160%;
      color: #ffffff;
      opacity: 0.7;
    }
  }
  &__button {
    margin-top: 20px;
  }
  &__btn {
    .ui-btn {
      background: none;
      border: 2px solid rgba(255, 255, 255, 0.3);
      border-radius: 12px;
      &:hover {
        background: red;
      }
    }
  }
}
</style>