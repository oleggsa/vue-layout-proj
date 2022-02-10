<template>
  <header class="header__wrapper" :class="{'header__wrapper-sticky': isSticky}">
    <div class="header__content">
      <Logo/>
      <MainMenu/>
      <div class="btns">
        <a href="#">SIGN IN</a>
        <CustomButton href="#">GET STARTED</CustomButton>
      </div>
    </div>
  </header>
</template>

<script>

import CustomButton from "@/components/UI/CustomButton";
import Logo from "@/components/Header/Logo"
import MainMenu from "@/components/Header/MainMenu";


export default {
  name: 'Header',
  components: {Logo, MainMenu, CustomButton},
  props: {
    isSticky: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<style lang="scss" scoped>
 .header__wrapper {
   height: 80px;
   display: flex;
   align-items: center;
   justify-content: center;
   box-shadow: 0 2px 8px rgba(3, 3, 3, 0.15);

 }
 .header__wrapper-sticky {
   position: fixed;
   top: 0;
   width: 1440px;
   background: #fff;
   z-index: 1000;
 }

 .header__content{
   display: flex;
   align-items: center;
   justify-content: center;
   margin: 0 80px;
 }

.btns a {
  font-weight: bold;
  margin-right: 16px;
  font-size: 18px;
}
.btns a {
  color: $primary;
}
button {
  width: 197px;
  height: 54px;
}
</style>
