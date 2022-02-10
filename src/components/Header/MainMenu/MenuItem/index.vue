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
.list-item {
  list-style-type: none;
  margin-right: 32px;
  &-link {
    font-size: 16px;
    font-weight: 600;
    & img {
      margin-left: 17px;
    }
  }
}

.dropdown {
  position: relative;
  display: inline-block;
  margin-right: 36px;
  &-subitem img {
    width: 24px;
    height: 24px;
    vertical-align: middle;
    margin-right: 12px;
  }
  &-content {
    opacity: 0;
    visibility: hidden;
    position: absolute;
    top: 49px;
    left: -20px;
    background-color: #ffffff;
    min-width: 252px;
    box-shadow: 0 2px 8px rgba(3, 3, 3, 0.15);
    z-index: 1;
    border-radius: 8px;
    transition-property: opacity, visibility;
    transition-delay: 0.3s;
    & li {
      list-style-type: none;
      & a {
        color: $primary;
        padding: 16px 12px 16px 19px;
        text-decoration: none;
        display: block;
        font-weight: bold;
        font-size: 15px;
        margin-left: -3px;
      }
    }
  }
}

.dropdown:hover .dropdown-content {
  opacity: 1;
  visibility: visible;
  transition-delay: 0s;
}
</style>