<template>
  <button>
    <a href="#"><slot></slot></a>
  </button>
</template>

<script>
export default {
  name: "MyButton",
}
</script>

<style lang="scss" scoped>
  button {
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
  }
  a {
    color: $primary;
  }
</style>