<template>
  <div class="prices__period-wrapper">
    <label v-for="item in pricesPeriods" :key="item.id">
      <div
          class="prices__period"
          :class="{ 'prices__period-popular-border': item.isPopular,
          'prices__period-chosen': currentItem === item.id}"
          @click="changeCurrentItem(item.id)"
      >
          <input id="radio" type="radio" name="radio">
          <div class="prices__period-header">{{item.name}}</div>
          <div v-if="item.isPopular" class="prices__period-popular-label">POPULAR</div>
          <div class="prices__period-price">
            <div v-if="item.sale" class="prices__period-sale">
              <sup>{{item.currency}}</sup>{{item.sale}}
            </div>
            <span>{{item.currency}}</span>{{item.price}}<span>{{item.price2}}</span>
          </div>
      </div>
    </label>
  </div>
</template>

<script>
export default {
  name: "index",
  data() {
    return {
      currentItem: ''
    }
  },
  props: {
    pricesPeriods: {
      type: Array
    }
  },
  methods: {
    console(item) {
      console.log(item)
    },
    changeCurrentItem(id) {
      this.currentItem = id;
    }
  }
}
</script>

<style lang="scss" scoped>
@import "style";
</style>