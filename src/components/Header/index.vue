<template>
  <header class="header__wrapper" :class="{'header__wrapper-sticky': isSticky}">
    <div class="header__content">
      <Logo/>
      <MainMenu/>
      <div class="header__buttons">
        <CustomButton href="#" type="secondary">SIGN IN</CustomButton>
        <CustomButton href="#" type="primary">GET STARTED</CustomButton>
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
@import "style";
</style>
