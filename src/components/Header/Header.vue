<template>
  <div class="header__wrapper">
    <div class="header__content">
      <img src="../../images/logo.png">
      <nav>
        <a href="#">Products</a>
        <a href="#">Why INSOCIAL?</a>
        <a href="#">Pricing</a>
        <a href="#">About</a>
        <a href="#">Contact Us</a>
      </nav>
      <div class="btns">
        <a href="#">SIGN IN</a>
        <MyButton href="#">GET STARTED</MyButton>
      </div>
    </div>
  </div>
</template>

<script>

import MyButton from "@/components/UI/MyButton";
export default {
  name: 'Header',
  components: {MyButton},
}
</script>

<style lang="scss" scoped>
 .header__wrapper {
   height: 80px;
   display: flex;
   align-items: center;
   justify-content: center;
   box-shadow: 0px 2px 8px rgba(3, 3, 3, 0.15);
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
 nav a {
   font-size: 16px;
   font-weight: 600;
 }

 nav a:first-child:after {
   margin-left: 15px;
   margin-right: 4px;
   content: url('../../icons/header-arrow.png');
 }
nav a:not(:last-child) {
 margin-right: 33px;
}

nav a:last-child {
  margin-right: 56px;
}

img {
 margin-right: 48px;
}
.btns a {
  color: $primary;
}
button {
  width: 197px;
  height: 54px;
}
</style>
