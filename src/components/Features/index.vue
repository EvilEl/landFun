<template>
  <div class="features">
    <div class="features__container _container">
      <div class="features__content">
        <div class="features__title title">Best features in the world</div>
        <div class="features__subtitle subtitle">
          Capture more customers wd recall. Whether you need a tising or as a tagline for you. Capture more
          <br />customers wd recall. Whether you need a tising or as a tagline for you.
        </div>
      </div>
      <div class="features__column">
        <div
          class="features__item"
          v-for="card in feuaturesData"
          :key="card.title"
          :class="{'features__item--margin':isFeauturesData}"
        >
          <div class="features__body">
            <div class="features__img _img">
              <img :src="require(`@/assets/features/${card.icon}`)" alt />
            </div>
            <div class="features__box">
              <div class="features__box-title title__column">{{card.title}}</div>
              <div class="features__box-subtitle subtitle__column">{{card.subTitile}}</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  computed: {
    isFeauturesData() {
      return this.feuaturesData.length > 3;
    },
  },
  data: () => ({
    feuaturesData: [
      {
        icon: "1.png",
        title: "Sleek and smooth animation",
        subTitile:
          "Powerful creations for the practice safe design creations for the prac.",
      },
      {
        icon: "2.png",
        title: "Crafted with detail",
        subTitile:
          "Powerful creations for the practice safe design creations for the prac.",
      },
      {
        icon: "3.png",
        title: "Save your time",
        subTitile:
          "Powerful creations for the practice safe design creations for the prac.",
      },
      {
        icon: "4.png",
        title: "Responsive on any device",
        subTitile:
          "Powerful creations for the practice safe design creations for the prac.",
      },
      {
        icon: "5.png",
        title: "Easy to customize",
        subTitile:
          "Powerful creations for the practice safe design creations for the prac.",
      },
      {
        icon: "6.png",
        title: "Quickly effective support",
        subTitile:
          "Powerful creations for the practice safe design creations for the prac.",
      },
    ],
  }),
};
</script>
<style lang="scss">
.features {
  padding: 120px 0;
  &__content {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin-bottom: 60px;
    & > *:not(:last-child) {
      margin-bottom: 20px;
    }
  }
  &__img {
    max-width: 80px;
    height: 80px;
  }
  &__title {
    max-width: 491px;
  }
  &__subtitle {
    max-width: 768px;
  }
  &__column {
    display: flex;
    flex-wrap: wrap;
    margin: 0 -37.5px;
  }
  &__item {
    flex: 0 1 33.3333%;
    position: relative;
    padding: 0 37.5px;
    &--margin {
      &:nth-child(n) {
        margin-bottom: 50px;
      }
      &:nth-last-child(1),
      &:nth-last-child(2),
      &:nth-last-child(3) {
        margin-bottom: 0;
      }
    }
    &::before {
      content: "";
      position: absolute;
      bottom: 0;
      left: 0;
      width: calc(100% - 240px / 2);
      left: calc(50% - 260px / 2);
      background: linear-gradient(
        90deg,
        rgba(53, 175, 191, 0) 0%,
        rgba(53, 175, 191, 0.83) 49.65%,
        rgba(53, 175, 191, 0) 100%
      );
      height: 2px;
    }
  }
  &__body {
    height: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding-bottom: 30px;

    & > *:not(:last-child) {
      margin-bottom: 30px;
    }
  }
  &__box {
    flex: 1 1 auto;
    & > *:not(:last-child) {
      margin-bottom: 15px;
    }
    &-title {
    }
    &-subtitle {
      width: 316px;
    }
  }
}
</style>