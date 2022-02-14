<template>
  <div class="prices__period-wrapper">
    <div v-for="item in pricesPeriods" :key="item.name">
      <div class="prices__period" :class="{ 'prices__period-popular-border': item.isPopular}">
        <input id="radio" type="radio" name="radio">
        <div class="prices__period-header">{{item.name}}</div>
        <div v-if="item.isPopular" class="prices__period-popular-label">POPULAR</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "index",
  props: {
    pricesPeriods: {
      type: Array
    }
  }
}
</script>

<style lang="scss" scoped>
@import "style";
</style>