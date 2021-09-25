<template >
  <div
    class="ui-button"
    :class="classButton"
    :style="`max-width:${widthButton}px;height:${heightButton}px;`"
  >
    <button class="ui-btn" @click="click">{{title}}</button>
  </div>
</template>
<script>
/*
props : 
  title = Для заголовка
  widthButton:изменяет max-width
  heightButton:изменяет max-heith
methods:
  click = эмитит событие на вверх
*/
export default {
  props: {
    title: {
      type: String,
      default: () => "Get Started",
    },
    widthButton: {
      type: Number,
      default: () => 190,
    },
    heightButton: {
      type: Number,
      default: () => 62,
    },
    classButton: {
      type: String,
      default: () => "",
    },
  },
  methods: {
    click() {
      this.$emit("click");
    },
  },
};
</script>
<style lang="scss">
.ui-button {
  width: 100%;
}
.ui-btn {
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: calc(19 / 16 * 100%);
  color: #ffffff;
  background: #35afbf;
  border-radius: 6px;
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
  border: none;
  height: 100%;
  width: 100%;
  cursor: pointer;
  transition: all 0.2s ease;
}
</style>