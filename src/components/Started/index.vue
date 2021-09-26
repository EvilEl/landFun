<template>
  <div class="started">
    <div class="started__container _contaienr">
      <h2 class="started__title title">
        People have tried to predict the
        future since
        <br />the dawn of time.
      </h2>
      <UiButton class="started__button" @click="acceptStarted" />
    </div>
  </div>
</template>
<script>
import UiButton from "@/components/Ui/UiButton";
export default {
  components: { UiButton },
  methods: {
    acceptStarted() {
      alert("modal is open");
    },
  },
};
</script>
<style lang="scss">
.started {
  padding: 120px 0;
  @media (max-width: 500px) {
    padding: 60px 0;
  }
  &__container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
  &__title {
    max-width: 854px;
    text-align: center;
    @media (max-width: 920px) {
    }
  }
  &__button {
    margin-top: 35px;
  }
}
</style>