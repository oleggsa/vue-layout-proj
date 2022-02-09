<template>
  <div class="rectangle"></div>
</template>

<script>
export default {
  name: "GradientRectangle"
}
</script>

<style lang="scss" scoped>
  .rectangle {
    width: 100%;
    background: linear-gradient(135deg, #00FF5B 0%, #0046DC 100%);
  }
</style>