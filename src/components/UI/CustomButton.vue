<template>
  <button v-if="type === 'primary'" class="button-success">
    <a href="#" class="button-success-text"><slot></slot></a>
  </button>
  <button v-else-if="type === 'secondary'" class="button-secondary">
    <a href="#"><slot></slot></a>
  </button>
</template>

<script>
export default {
  name: "MyButton",
  props: {
    type: {
      type: String,
      default: 'primary'
    }
  }
}
</script>

<style lang="scss" scoped>
  .button {
    &-success {
      display: inline-block;
      background-color: $secondary;
      width: 100px;
      height: 30px;
      border-radius: 8px;
      font-weight: bold;
      border: 2px dashed #07166C;
      font-size: 18px;

      &:hover {
        border: 2px solid $primary;
        transition: 0.2ms all;
      }
      &-text {
        color: $primary;
      }
    }
    &-secondary {
      font-weight: bold;
      font-size: 18px;
      margin: 16px 16px 16px 20px;
      border: none;
      background: none;
    }
  }
</style>