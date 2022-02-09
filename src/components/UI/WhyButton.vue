<template>
  <div class="why__content-button">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "WhyButton"
}
</script>

<style lang="scss" scoped>
  .why__content-button {
    position: relative;
    height: 60px;
    width: 527px;
    margin-top: 12px;
    border-radius: 16px;
    background: #F8F8F8;
    color: #696969;
    font-weight: 600;
  }
</style>