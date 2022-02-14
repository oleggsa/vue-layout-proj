<template>
  <div class="why__wrapper" id="why">
    <div class="why__content-wrapper">
      <div class="why__content-header">
        <h1>Why INSOCIAL?</h1>
        <GradientRectangle/>
      </div>
      <p class="why__content-desqr">Our Instagram marketing services are made for growth.<br>
        Must-have for business, influencers, digital marketing specialists</p>
      <div class="why__content-btn-group">
        <WhyButton :whyOptions="whyOptions"></WhyButton>
      </div>
      <MyButton>GET STARTED</MyButton>
    </div>
  </div>
</template>

<script>


export default {
  name: "Why",
  data() {
    return {
      whyOptions: [
        {id: 1, name: 'AUTO PROMOTION', desqr: 'Auto view stories and interact with them',
          iconActive: require('@/icons/auto_promo.png'),
          icon: require('@/icons/why-1.png'),
          device: require('@/images/promotion-device.png'),
          position: {top: '-8px', left: '712px'}},
        {id: 2, name: 'AUTO LIKING', desqr: 'Liking other people\'s posts',
          iconActive: require('@/icons/auto_liking.png'),
          icon: require('@/icons/why-2.png'),
          device: require('@/images/liking-device.png'),
          position: {top: '-80px', left: '712px'}},
        {id: 3, name: 'DIRECT MESSAGES', desqr: 'Organize your chats and add tags for your customers',
          iconActive: require('@/icons/messages.png'),
          icon: require('@/icons/why-3.png'),
          device: require('@/images/messages-device.png'),
          position: {top: '-166px', left: '524px'}},
        {id: 4, name: 'SCHEDULE POSTING', desqr: 'Plan Instagram posts and Stories',
          iconActive: require('@/icons/posting.png'),
          icon: require('@/icons/why-4.png'),
          device: require('@/images/posting-device.png'),
          position: {top: '-251px', left: '637px'}},
        {id: 5, name: 'COMMENT TRACKER', desqr: 'Track your comments and reply faster',
          iconActive: require('@/icons/comment.png'),
          icon: require('@/icons/why-5.png'),
          device: require('@/images/comment-device.png'),
          position: {top: '-324px', left: '630px'}},
        {id: 6, name: 'HASHTAG GENERATOR', desqr: 'Generate hashtags for social media automatically',
          iconActive: require('@/icons/hashtag.png'),
          icon: require('@/icons/why-6.png'),
          device: require('@/images/hashtag-device.png'),
          position: {top: '-397px', left: '637px'}},
      ]
    }
  },


}
</script>

<style lang="scss" scoped>
@import "style";
</style>