<template >
  <div class="hero">
    <div class="hero__container _container">
      <div class="creative">
        <div class="creative__title">
          <span>Make</span>
          a Creative solutions for your Creative
          <span>ideas.</span>
        </div>
        <div class="creative__subtitle">
          We are here to give you effective ideas.
          We help the brands to become what they want.
        </div>
        <div class="creative__button button">
          <UiButton />
        </div>
      </div>
      <!-- <div class="hero__image _img">
        <img class="hero__img" :src="require('@/assets/main/hero/1.png')" alt />
        <div class="icon__image-him _img">
          <img :src="require('@/assets/main/hero/2.png')" alt />
        </div>
        <div class="icon__image-comp _img">
          <img :src="require('@/assets/main/hero/3.png')" alt />
        </div>
        <div class="icon__image-writ _img">
          <img :src="require('@/assets/main/hero/4.png')" alt />
        </div>
        <div class="icon__image-dip _img">
          <img :src="require('@/assets/main/hero/5.png')" alt />
        </div>
      </div>-->
    </div>
    <div class="hero__image-bg">
      <img :src="require('@/assets/main/1.jpg')" alt />
    </div>
  </div>
</template>
<script>
import UiButton from "@/components/Ui/UiButton";

export default {
  components: { UiButton },
};
</script>
<style lang="scss">
.hero {
  padding: 239px 0 189px 0;
  position: relative;
  z-index: 1;
  &__image-bg {
    width: 100%;
    height: 100%;
    // position: absolute !important;
    top: 0;
    left: 0;
  }
  &__container {
    display: flex;
    position: relative;
    z-index: 1;
  }
  .creative {
    & > *:not(:last-child) {
      margin-bottom: 30px;
    }
    max-width: 523px;
    width: 100%;
    &__title {
      font-weight: 800;
      font-size: 51px;
      line-height: 125%;
      color: #252626;
      & span {
        color: #32a3b2;
      }
    }
    &__subtitle {
      font-weight: 400;
      font-size: 21px;
      line-height: 160%;
      color: #707273;
    }
    &__button {
      max-width: 190px;
      width: 100%;
      max-height: 62px;
      height: 100%;
    }
  }

  &__image {
    position: relative;
  }
}
.icon__image {
  position: relative;
  &-him {
    position: absolute;
    top: 0;
    left: 0;
  }
}
.hero__image-bg img {
  position: absolute;
  top: 0%;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>