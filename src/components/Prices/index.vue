<template>
  <div class="prices__wrapper" id="price">
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
            <Options :pricesOptions="pricesOptions"></Options>
          </div>
          <div class="prices__content-table-prices-period col-6">
            <h3>Subscription Period</h3>
            <Periods :pricesPeriods="pricesPeriods"></Periods>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Options from "@/components/Prices/Options";
import Periods from "@/components/Prices/Periods";

export default {
  name: "Prices",
  components: {
    Options,
    Periods
  },
  data() {
    return {
      pricesOptions: [
        {name: 'AUTO PROMOTION', desqr: 'Auto view and interact with stories', active: true},
        {name: 'AUTO LIKING', desqr: 'Auto liking other people\'s posts', active: true},
        {name: 'DIRECT MESSAGES', desqr: 'Manage your chats in one solution', active: true},
        {name: 'COMMENT TRACKER', desqr: 'Manage your comments in one solution', active: true},
        {name: 'SCHEDULED POSTING', desqr: 'Automatic posting at the right time', active: true},
        {name: 'HASHTAG GENERATOR', desqr: 'Drive the traffic to the page', active: true}
      ],
      pricesPeriods: [
        {name: '1 WEEK', currency: '$', price: '19', price2: '.97',},
        {name: '1 MONTH', currency: '$', price: '29', price2: '.97', sale: '29.99', isPopular: true},
        {name: '3 MONTHS', currency: '$', price: '49', price2: '.97', sale: '29.99'},
        {name: '6 MONTHS', currency: '$', price: '129', price2: '.97', sale: '29.99'},
        {name: '1 YEAR', currency: '$', price: '229', price2: '.97', sale: '29.99'},
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import "style";
</style>