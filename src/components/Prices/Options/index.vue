<template>
  <div class="prices__content-options-wrapper">
    <div v-for="item in pricesOptions" :key="item.name" class="prices__content-options">
      <div v-if="item.active === true">
        <Switch @click="console()"></Switch>
        <div class="prices__content-text">
          <div class="prices__content-text-header">{{item.name}}</div>
          <GradientRectangle></GradientRectangle>
          <div class="prices__content-text-desqr">{{item.desqr}}</div>
        </div>
        <Counter></Counter>
      </div>
      <div v-else class="prices__content-options">
        <Switch state="disabled"></Switch>
        <div class="prices__content-text">
          <div class="prices__content-text-header">{{item.name}}</div>
          <GradientRectangle></GradientRectangle>
          <div class="prices__content-text-desqr">{{item.desqr}}</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Switch from "@/components/UI/Switch";
import Counter from "@/components/UI/Counter";

export default {
  name: "index",
  components: {Counter, Switch},
  props: {
    pricesOptions: {
      type: Array,
      default: ''
    }
  },
  methods: {
    console () {
      console.log(123)
    }
  }
}
</script>

<style lang="scss" scoped>
@import "style";
</style>