<template>
  <div class="footer">
    <div class="footer__container _container">
      <div class="footer__box">
        <ul class="footer__list">
          <li class="footer__list-item" v-for="item in listNav" :key="item.title">
            <a class="footer__list-link" href="#">{{item.title}}</a>
          </li>
        </ul>
        <div class="footer__social">
          <div class="footer__social-icon _img" v-for="icon in socialIcon" :key="icon.icon">
            <img :src="require(`@/assets/footer/${icon.icon}`)" alt />
          </div>
        </div>
      </div>
      <div class="footer__descript">@ A new era 2016. Awesome wireframe by Andrei Dorin</div>
    </div>
  </div>
</template>
<script>
export default {
  data: () => ({
    socialIcon: [
      {
        icon: "1.png",
      },
      {
        icon: "2.png",
      },
      {
        icon: "3.png",
      },
      {
        icon: "4.png",
      },
    ],
    listNav: [
      {
        title: "Home",
      },
      {
        title: "Privacy",
      },
      {
        title: "Terms & Conditions",
      },
      {
        title: "About us",
      },
      {
        title: "Contact us",
      },
    ],
  }),
};
</script>
<style lang="scss">
.footer {
  margin: 0;
  background: #2c353e;
  padding: 40px 0;
  &__box {
    display: flex;
    align-items: center;
  }
  &__list {
    flex: 1 1 auto;
    display: flex;
    padding: 0;
    & > *:not(:first-child) {
      margin-left: 35px;
    }
    &-item {
      list-style: none;
      max-width: 152px;
    }
    &-item:hover &-link {
      color: #3068a1;
    }
    &-link {
      text-decoration: none;
      font-size: 16px;
      line-height: 160%;
      color: #ffffff;
      transition: color 0.2s ease-in;
    }
  }
  &__social {
    display: flex;
    & > *:not(:first-child) {
      margin-left: 40px;
    }
    &-icon {
      width: 20px;
      height: 20px;
    }
  }
  &__descript {
    font-size: 12px;
    line-height: 160%;
    color: #ffffff;
    opacity: 0.6;
    max-width: 400px;
  }
}
</style>