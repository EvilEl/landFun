<template >
  <div class="services">
    <div class="services__container _container">
      <div class="services__content main-content">
        <h2 class="services__title title">We provide great services</h2>
        <div class="services__subtitle subtitle">
          We help people to think independent. Be the boss of your brand and be the
          <br />storyteller. An appropriate approach.
        </div>
      </div>
      <div class="services__column">
        <div class="services__item" v-for="card in servicesData" :key="card.title">
          <div class="services__body">
            <div class="services__body-image _img">
              <img :src="require(`@/assets/services/${card.img}`)" alt="Web Design" />
            </div>
            <div class="services__body-content">
              <div class="services__body-title title__column">{{card.title}}</div>
              <div class="services__body-subtitle subtitle__column">{{card.subtitle}}</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data: () => ({
    servicesData: [
      {
        title: "Web Design",
        subtitle: "Powerful creations for the practice safe design.",
        img: "1.png",
      },
      {
        title: "Identity & Branding",
        subtitle: "Powerful creations for the practice safe design.",
        img: "2.png",
      },
      {
        title: "Print and Packaging",
        subtitle: "Powerful creations for the practice safe design.",
        img: "3.png",
      },
      {
        title: "Content Writing",
        subtitle: "Powerful creations for the practice safe design.",
        img: "4.png",
      },
    ],
  }),
};
</script>
<style lang="scss">
.services {
  padding-top: 119px;
  &__content {
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin-bottom: 59px;
  }
  &__title {
    font-style: normal;
    font-weight: 700;
    font-size: 38px;
    line-height: calc(45 / 38 * 100%);
    color: #252626;
    @media (max-width: 720px) {
      font-size: 30px !important;
    }
    @media (max-width: 400px) {
      font-size: 25px !important;
    }
  }
  &__subtitle {
    @media (max-width: 720px) {
      font-size: 14px !important;
      max-width: 280px;
    }
  }
  &__column {
    margin: 0 -15px;
    display: flex;
    @media (max-width: 992px) {
      flex-wrap: wrap;
    }
  }
  &__item {
    padding: 0 15px;
    flex: 0 1 25%;
    height: 100%;
    border-radius: 10px;
    @media (max-width: 992px) {
      flex: 0 1 50%;
    }
    @media (max-width: 540px) {
      flex: 1 1 100%;
    }
    transition: all 0.2s ease-in-out;
    &:hover {
      background: url("~@/assets/services/5.png");
      background-repeat: no-repeat;
      background-size: cover;
    }
  }
  &__body {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 34px 22px;
    height: 100%;
    &-content {
      display: flex;
      flex: 1 1 auto;
      flex-direction: column;
    }

    &-image ._img img {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
    & > *:not(:last-child) {
      margin-bottom: 15px;
    }
  }
}
</style>