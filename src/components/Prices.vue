<template>
  <div class="prices__wrapper">
    <div class="prices__content">
      <div class="prices__content-header">
        <div class="prices__content-header-header">
          <h1>OUR PRICES</h1>
          <GradientRectangle></GradientRectangle>
        </div>
        <div class="prices__content-header-desqr">
          <p>Smart investment in the Insocial tools will help you to become a trusted influencer or set up an Instagram shop.</p>
        </div>
      </div>
      <div class="prices__content-table">
        <div class="prices__content-table-prices row">
          <div class="prices__content-table-prices-plan col-6">
            <h3 class="prices__content-table-prices-plan-header">Setup Your Plan</h3>
            <p class="prices__content-table-prices-plan-desqr">Accounts</p>
            <div class="prices__content-table-prices-plan-row" v-for="item of 6">
              <Switch></Switch>
              <div class="prices__content-table-prices-plan-row-text">
                <h3>AUTO PROMOTION</h3>
                <GradientRectangle></GradientRectangle>
                <p>Auto view and interact with stories</p>
              </div>
              <Counter></Counter>
            </div>
          </div>
          <div class="prices__content-table-prices-period col-6">
            <h3>Subscription Period</h3>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Prices",

}
</script>

<style lang="scss" scoped>
.prices {
  &__wrapper {
    height: 770px;
    margin-top: 133px;
    background: url("../images/prices-background.png") no-repeat center 95px;
  }
  &__content {
    margin: 0 140px;
    &-header {
      text-align: center;
      &-header {
        display: inline-block;
        & .rectangle {
          height: 4px;
          margin-top: 2px;
        }
        & h1 {
          font-size: 36px;
          font-weight: 600;
          color: $primary;
        }
      }
      &-desqr {
        font-size: 18px;
        color: $primary;
        margin-top: 2px;
      }
    }
    &-table {
      width: 1040px;
      height: 646px;
      background-color: #ffffff;
      margin-top: 49px;
      margin-left: 60px;
      box-shadow: 0 2px 8px rgba(3, 3, 3, 0.15);
      border-radius: 8px;
      &-prices {
        padding-top: 15px;
        padding-left: 24px;
        &-plan h3,
        &-period h3 {
          font-weight: 500;
          font-size: 24px;
          color: $primary
        }
        &-plan {
          position: relative;
          &-header,
          &-desqr {
            display: inline-block;
          }
          &-header {
            margin-bottom: 5px;
          }
          &-desqr {
            position: absolute;
            right: 46px;
            top: 5px;
            color: $primary
          }
          &-row {
            margin-top: 4px;
            margin-left: 12px;
            & .switch {
              top: -16px;
            }
            &-text {
              width: 248px;
              height: 41px;
              margin-left: 32px;
              display: inline-block;
              & h3 {
                font-weight: 600;
                font-size: 18px;
              }
              & .rectangle {
                height: 1px;
              }
              & p {
                margin-top: 1px;
                font-size: 12px;
                color: $primary;
              }
            }
          }
        }
      }
    }
  }
}
</style>