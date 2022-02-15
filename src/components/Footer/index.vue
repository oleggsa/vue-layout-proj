<template>
  <div class="footer__wrapper" id="footer">
    <div class="footer__content">
      <div class="footer__content-logo">
        <div class="footer__content-logo-img"><img src="../../images/footer-logo.png" alt="logo"></div>
        <div class="footer__content-logo-text">
          Insocial is not endorsed or certified by<br>
          Instagram. All Instagram TM logos and<br>
          trademarks displayed on this<br>
          application are property of Instagram.<br>
          Service provider:###########
        </div>
      </div>
      <div class="footer__content-products">Products
        <div class="footer__content-products-list" v-for="item in products" :key="item">
          <a :href="item.link">
            {{item.name}}
          </a>
        </div>
      </div>
      <div class="footer__content-about">About
        <div class="footer__content-about-list" v-for="item in about" :key="item">
          <a :href="item.link">
            {{item.name}}
          </a>
        </div>
      </div>
      <div class="footer__content-support">Support
        <div class="footer__content-support-list" v-for="item in support" :key="item">
          <a :href="item.link">
            {{item.name}}
          </a>
        </div>
      </div>
      <div class="footer__content-contacts">Get In Touch
        <div class="footer__content-contacts-list" v-for="item in getInTouch" :key="item">
          <img :src="item.icon" alt="icon">
          {{item.name}}<span>{{item.email}}</span>
        </div>
        <div class="footer__content-contacts-chat">
          <img src="../../icons/footer-4.png" alt="chat">
          LIVE CHAT
        </div>
        <div class="footer__content-contacts-schedule">
          Mon - Fri, 8:00 AM - 10.00 PM EST<br>
          Sat - Sun, 9:00 AM - 4:00 PM EST
        </div>
        <div class="footer__content-contacts-methods">
          <img v-for="item in payMethods" :key="item" :src="item" alt="pay">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "index",
  data() {
    return {
      products: [
        {name: 'Auto liking', link: '/liking'},
        {name: 'Direct messages', link: '/dir-mes'},
        {name: 'Schedule posting', link: '/posting'},
        {name: 'Comment tracker', link: '/tracker'},
        {name: 'Hashtag generator', link: '/hashtag'},
        {name: 'Infulence search', link: '/search'}
      ],
      about: [
        {name: 'Why INSOCIAL?', link: '/why'},
        {name: 'Our Team', link: '/team'},
        {name: 'Prices', link: '/prices'},
        {name: 'Careers', link: '/career'},
      ],
      support: [
        {name: 'FAQ', link: '/faq'},
        {name: 'Contact us', link: '/contact-us'},
        {name: 'Privacy policy', link: '/policy'},
        {name: 'Terms of service', link: '/terms'},
      ],
      getInTouch: [
        {name: 'General:', email: 'contact@insocial.io', icon: require('@/icons/footer-1.png')},
        {name: 'Media:', email: 'media@insocial.io', icon: require('@/icons/footer-2.png')},
        {name: 'Support:', email: 'support@insocial.io', icon: require('@/icons/footer-3.png')},
      ],
      payMethods: [
        require('@/icons/footer-5.png'),
        require('@/icons/footer-6.png'),
        require('@/icons/footer-7.png'),
        require('@/icons/footer-8.png')
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import "style";
</style>