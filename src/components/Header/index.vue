<template >
  <div class="header">
    <div class="header__container _container">
      <div class="header__wrapper">
        <a class="header__logo logo _img" href="/">
          <img
            class="header__image logo__image"
            :src="require('@/assets/header/Logo.png')"
            alt="maker"
          />
        </a>
        <nav class="menu">
          <ul class="menu__list">
            <li class="header__item menu__item">
              <a href="#" class="header__link menu__link">Home</a>
            </li>
            <li class="header__item menu__item">
              <a href="#" class="header__link menu__link">Services</a>
            </li>
            <li class="header__item menu__item">
              <a href="#" class="header__link menu__link">About</a>
            </li>
            <li class="header__item menu__item">
              <a href="#" class="header__link menu__link">The Team</a>
            </li>
            <li class="header__item menu__item">
              <a href="#" class="header__link menu__link">Pricing</a>
            </li>
            <li class="header__item menu__item">
              <a href="#" class="header__link menu__link">Contact</a>
            </li>
          </ul>
        </nav>
        <div class="header__button button">
          <UiButton :widthButton="120" :heightButton="49" title="Sign Up" />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import UiButton from "../Ui/UiButton.vue";

export default {
  components: { UiButton },
};
</script>
<style lang="scss">
.header {
  position: absolute;
  width: 100%;
  top: 0;
  left: 0;
  z-index: 50;
  padding-top: 34px;

  &__container {
  }
  &__logo {
    min-height: 37px;
    position: relative;
    padding-right: 190px;
  }
  @media (max-width: 1066px) {
    padding-right: 100px;
  }
  &__wrapper {
    display: flex;
    align-items: center;
  }
  &__list {
    margin: 0 -22px;
  }
  &__item {
    position: relative;
    list-style: none;
    padding: 2px 2px;
    transition: all 0.2s ease-in-out;
    padding: 0 22px;
  }
  &__item &__link:hover {
    color: #35afbf;
  }
  &__link:hover::before {
    content: "";
    position: absolute;
    bottom: 0;
    left: 0;
    height: 2px;
    width: 100%;
    background: #35afbf;
  }
  &__link {
    position: relative;
    padding: 0 2px;
    text-decoration: none;
    display: block;
    font-style: normal;
    font-weight: normal;
    font-size: 16px;
    line-height: 160%;
    color: #969999;
    height: 100%;
    transition: all 0.2s ease-in-out;
  }
  &__button {
    height: 49px;
    width: 120px;
  }
}
</style>