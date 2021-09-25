<template >
  <div class="specialist">
    <div class="specialist__container _container">
      <div class="specialist__box">
        <h3 class="specialist__name">Johnatan Doe</h3>
        <div class="specialist__profile">Marketing Specialist</div>
        <div class="specialist__subtitle">
          To make your web design company famous in the little
          we are here to provide you as many as catchy and useful
          web design company will surely help your company.
        </div>
        <div class="specialist__button">
          <button class="specialist__btn">Learn More</button>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style lang="scss">
.specialist {
  padding-top: 159px;
  &__box {
    max-width: 449px;
  }
  &__name {
    font-style: normal;
    font-weight: 700;
    font-size: 38px;
    line-height: calc(45 / 38 * 100%);
    color: #252626;
    margin-bottom: 10px;
  }
  &__profile {
    font-weight: 500;
    font-size: 16px;
    line-height: 160%;
    color: #707273;
    margin-bottom: 20px;
  }
  &__subtitle {
    font-style: normal;
    font-weight: normal;
    font-size: 16px;
    line-height: 160%;
    margin-bottom: 35px;
    color: #707273;
    max-width: 217px;
  }
  &__button {
  }
  &__btn {
    background: none;
    min-height: 49px;
    min-width: 149px;
    max-width: 160px;
    display: flex;
    justify-content: center;
    align-items: center;
    border: 1px solid rgba(53, 175, 191, 0.2);
    border-radius: 6px;
    font-weight: 500;
    font-size: 16px;
    line-height: 120%;
    color: #35afbf;
    transition: all 0.2s ease;
    &:hover {
      background: #35afbf;
      color: #fff;
    }
  }
}
</style>