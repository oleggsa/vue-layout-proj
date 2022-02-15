<template>
  <div class="copyright__wrapper">
    <div class="copyright__content">
      <div class="copyright__socials">
        <img v-for="item in socials" :key="item" :src="item" alt="socials">
      </div>
      <div class="copyright__text">
        Copyright © 2020-2021, INSOCIAL LLC. All Rights Reserved
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "index",
  data() {
    return {
      socials: [
          require('@/icons/footer-twitter.png'),
          require('@/icons/footer-insta.png'),
          require('@/icons/footer-facebook.png'),
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import "style";
</style>