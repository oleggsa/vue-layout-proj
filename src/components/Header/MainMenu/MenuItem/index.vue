<template>
  <li v-if='!linkListItem.subitem' class="list-item">
    <a :href='linkListItem.link' class="list-item-link">
      {{linkListItem.title}}
    </a>
  </li>
  <li v-else class="dropdown">
      <a class="dropbtn list-item-link" :href="linkListItem.link">{{linkListItem.title}}<img src="../../../../icons/header-arrow.png" alt="arrow"/></a>
      <div class="dropdown-content">
        <ul v-for="item in linkListItem.subitem" :key="item.title">
          <li>
            <a :href="item.link" class="dropdown-subitem">
              <img :src="item.icon" :alt="item.title">
              {{ item.title }}
            </a>
          </li>
        </ul>
      </div>
    </li>
</template>

<script>
export default {
  name: "MenuItem",
  props: {
    linkListItem: {
      type: Object
    },
  },
  data() {
    return {
      clicked: false
    }
  }
}
</script>

<style lang="scss" scoped>
@import 'style';
</style>