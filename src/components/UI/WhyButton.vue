<template>
  <div
      v-for="item in whyOptions"
      :key="item.id"
      @click="changeActiveSlide(item.id)"
  >
    <div v-if="item.id !== activeDataID" class="why__content-button">
      <img class="why__content-button-icon" :src='item.icon' :alt='item.id + "icon"'>
      <div class="why__content-button-title">
        {{item.name}}
      </div>
    </div>
    <div v-else class="why__content-button">
      <div class="why__content-button-active">
        <img class="why__content-button-active-device" :src="item.device" alt="device picture"
             :style="item.position">
        <div class="why__content-button-active-mark"></div>
        <img class="why__content-button-icon" :src='item.iconActive' :alt='item.id + "icon"'>
        <div class="why__content-button-active-title">
          {{item.name}}
        </div>
        <div class="why__content-button-active-desqr">
          {{item.desqr}}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "WhyButton",
  data () {
    return {
      activeDataID: 2
    }
  },
  props: {
    whyOptions: {
      type: Array
    }
  },
  methods: {
    changeActiveSlide(id) {
      this.activeDataID = id;
    }
  }
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
    &-active {
      color: $primary;
      &-mark {
        position: absolute;
        height: 60px;
        width: 12px;
        border-radius: 8px 0 0 8px;
        background-color: $secondary;
      }
      &-title {
        position: absolute;
        top: 8px;
        left: 112px;
        z-index: 10;
        font-weight: 600;
      }
      &-desqr {
        position: absolute;
        top: 33px;
        left: 112px;
        z-index: 10;
        font-size: 14px;
      }
      &-device {
        position: absolute;
        top: 100px;
        left: 500px;
      }
    }
    &-title {
      position: absolute;
      top: 20px;
      left: 112px;
      z-index: 10;
      font-weight: 600;
    }
    &-icon {
      margin-left: 35px;
      margin-top: 3px;
      height: 52px;
      width: 52px;
    }
  }
</style>