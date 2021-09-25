<template>
  <div class="recall">
    <div class="recall__container _container">
      <div class="recall__icon">
        <img :src="require('@/assets/recall/1.png')" alt />
      </div>
      <div class="recall__text">
        “Always a pleasure to work with The Agency Creative. Such professional
        and happy people and you know
        you’ll receive a quick innovative and no fuss service.”
      </div>
      <div class="recall__box">
        <div class="recal__box-image">
          <img class="recal__box-img" :src="require('@/assets/recall/2.png')" alt />
        </div>
        <div class="recall__box-content content__recall">
          <div class="content__recall-name">Johnatan Doe</div>
          <div class="content__recall-profile">Web Designer</div>
        </div>
      </div>
    </div>
    <div class="recall__img _img">
      <img :src="require('@/assets/recall/bg.jpg')" alt />
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style lang="scss">
.recall {
  position: relative;
  padding: 100px 0;
  &__container {
    display: flex;
    align-items: center;
    flex-direction: column;
    justify-content: center;
    position: relative;
    z-index: 1;
  }
  &__img {
    position: absolute !important;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
  }
  &__icon {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  &__text {
    margin-top: 40px;
    font-style: normal;
    font-weight: 500;
    font-size: 32px;
    line-height: 140%;
    text-align: center;
    color: #4b4c4c;
  }
  &__box {
    margin-top: 35px;
    display: flex;
    align-items: center;
  }
}
.content__recall {
  margin-left: 16px;
  & > *:not(:last-child) {
    margin-bottom: 12px;
  }
  &-name {
    font-style: normal;
    font-weight: 500;
    font-size: 21px;
    line-height: 80%;
    color: #4b4c4c;
  }
  &-profile {
    font-style: normal;
    font-weight: 500;
    font-size: 12px;
    line-height: 100%;
    color: #707273;
  }
}
</style>