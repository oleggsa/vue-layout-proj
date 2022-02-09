<template>
  <div class="why__content-button why__btn-active">
    <div class="why__content-button-active">
      <div class="why__content-button-active-mark">
      </div>
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "WhyButtonActive"
}
</script>

<style lang="scss" scoped>
.why__content-button-active {
  position: relative;
  height: 60px;
  width: 527px;
  margin-top: 12px;
  border-radius: 16px;
  background: #F8F8F8;
  color: #07166C;

  &-mark {
    position: absolute;
    width: 12px;
    height: 60px;
    background-color: #38D89A;
    border-radius: 16px 0 0 16px;
  }
}
</style>