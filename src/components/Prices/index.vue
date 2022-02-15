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
            <div class="prices__content-table-prices-period-button">
              <CustomButton><img src="../../icons/prices-cart.png" alt="cart">ORDER</CustomButton>
            </div>
          </div>
        </div>
        <div class="prices__promocode">
          <div class="prices__promocode-content">
            Enter Promo Code
          </div>
        </div>
        <div class="prices__border-bottom"></div>
        <div class="prices__features">
          <div class="prices__features-title">FULL FEATURES LIST</div>
          <div class="prices__features-content">
            <Features :features="features"></Features>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Options from "@/components/Prices/Options";
import Periods from "@/components/Prices/Periods";
import CustomButton from "@/components/UI/CustomButton";
import Features from "@/components/Prices/Features";

export default {
  name: "Prices",
  components: {
    Options,
    Periods,
    CustomButton,
    Features
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
        {id: 1, name: '1 WEEK', currency: '$', price: '19', price2: '.97',},
        {id: 2, name: '1 MONTH', currency: '$', price: '29', price2: '.97', sale: '29.99', isPopular: true},
        {id: 3, name: '3 MONTHS', currency: '$', price: '49', price2: '.97', sale: '29.99'},
        {id: 4, name: '6 MONTHS', currency: '$', price: '129', price2: '.97', sale: '29.99'},
        {id: 5, name: '1 YEAR', currency: '$', price: '229', price2: '.97', sale: '29.99'},
      ],
      features: [
        {name: 'View stories', icon: require('@/icons/prices-footer-1.png')},
        {name: 'Guess correct answer', icon: require('@/icons/prices-footer-2.png')},
        {name: 'Direct Chat for all Accounts', icon: require('@/icons/prices-footer-3.png')},
        {name: 'Comments tracking for all Accounts', icon: require('@/icons/prices-footer-4.png')},
        {name: 'Vote for the best variant', icon: require('@/icons/prices-footer-5.png')},
        {name: 'Answer custom text', icon: require('@/icons/prices-footer-6.png')},
        {name: 'Stories and Gallery Posting', icon: require('@/icons/prices-footer-7.png')},
        {name: 'Hashtag Management', icon: require('@/icons/prices-footer-8.png')},
        {name: 'Rate in percentage\n', icon: require('@/icons/prices-footer-9.png')},
        {name: 'Tag your contacts', icon: require('@/icons/prices-footer-10.png')},
        {name: 'Drive 10X Traffic to Your Page', icon: require('@/icons/prices-footer-11.png')},
        {name: 'Smart Analytics Instruments', icon: require('@/icons/prices-footer-12.png')},
        {name: 'Follow the countdown', icon: require('@/icons/prices-footer-13.png')},
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import "style";
</style>