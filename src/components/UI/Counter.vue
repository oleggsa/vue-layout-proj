<template>
  <div class="counter">
    <div class="counter__minus" @click="counter--"></div>
    <div class="counter__digit">{{counter}}</div>
    <div class="counter__plus" @click="counter++"></div>
  </div>
</template>

<script>
export default {
  name: 'Counter',
  data() {
    return {
      counter: 0
    }
  }

}
</script>

<style lang="scss" scoped>
div {
  display: inline-block;
}
.counter{
  width: 100px;
  height: 24px;
  margin-left: 32px;
  &__minus,
  &__plus {
    height: 24px;
    width: 24px;
    background: #F8F8F8;
    border-radius: 22px;
  }
  &__digit {
    margin: 0 10px;
    vertical-align: top;
    font-size: 16px;
    font-weight: 600;
  }
  &__minus {
    &:before {
      content: "";
      width: 8px;
      height: 1px;
      background: black;
      display: block;
      margin-top: 10px;
      margin-left: 8px;
      border-radius: 2px;
    }
  }
  &__plus {
    &:before {
      content: "";
      width: 8px;
      height: 1px;
      background: black;
      display: block;
      margin-top: 10px;
      margin-left: 7px;
      border-radius: 2px;
    }
    &:after {
      content: "";
      width: 1px;
      height: 8px;
      background: black;
      display: block;
      margin-top: -5px;
      margin-left: 11px;
      border-radius: 2px;
    }
  }
}
</style>