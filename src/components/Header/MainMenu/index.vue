<template>
  <nav class="menu__items-list">
    <ul v-for="item in linkList" :key="item.title">
      <MenuItem :linkListItem="item"></MenuItem>
    </ul>
  </nav>
</template>

<script>
import MenuItem from "@/components/Header/MainMenu/MenuItem";
export default {
  name: "MainMenu",
  components: {
    MenuItem
  },
  data(){
    return{
      linkList: [
        {title: 'Products', link: '/products', subitem: [
            {title: 'AUTO PROMOTION', link: '/auto-promotion', icon: require('@/icons/header-submenu-auto_promo.png')},
            {title: 'AUTO LIKING', link: '/auto-liking', icon: require('@/icons/header-sub-active_liking.png')},
            {title: 'DIRECT MESSAGES', link: '/direct-messages', icon: require('@/icons/header-sub-active_messages.png')},
            {title: 'SCHEDULE POSTING', link: '/schedule-posting', icon: require('@/icons/header-sub-active_posting.png')},
            {title: 'COMMENT TRACKER', link: '/comment-tracker', icon: require('@/icons/header-sub_comment.png')},
            {title: 'HASHTAG GENERATOR', link: '/hashtag-generator', icon: require('@/icons/header-sub-hashtag.png')},
          ]},
        {title: 'Why INSOCIAL?', link: '#why'},
        {title: 'Pricing', link: '#price'},
        {title: 'About', link: '/about'},
        {title: 'Contact Us', link: '/contact'}
      ]
    }
  }
}
</script>

<style scoped>
@import 'style.scss';
</style>