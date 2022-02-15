<template>
  <div class="features__item" v-for="item in features" :key="item.name">
    <img :src="item.icon" alt="feature">{{item.name}}</div>
</template>

<script>
export default {
  name: "index",
  props: {
    features: {
      type: Array
    }
  }
}
</script>

<style lang="scss" scoped>
.features__item {
  margin: 5px;
  font-size: 12px;
  color: $primary;
  width: 24%;
  & img {
    vertical-align: -4px;
    margin-right: 8px;
  }
}
</style>