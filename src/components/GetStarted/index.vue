<template>
  <section class="get-started__wrapper">
    <div class="get-started__content-wrapper">
      <div class="get-started__content">
        <div class="get-started__content-title">
          MARKETING TOOLKIT <br>FOR INSTAGRAM
        </div>
        <div class="get-started__content-desqr">
          Become Instagram-famous and skyrocket sales by using pro tools. These must-have solutions
          will help you attract fans, engage with сustomers, сurate content, and grow revenue.
        </div>
        <div class="get-started__content-btns">
          <MyButton>GET STARTED</MyButton>
          <div class="get-started__second-button">
            <CustomButton type="secondary">CHECK YOUR GROWTH</CustomButton>
            <GradientRectangle></GradientRectangle>
          </div>
        </div>
      </div>
      <div class="get-started__images">
        <img class="get-started__images-icons" src="../../images/header-robot-icons.png" alt="icons">
        <img class="get-started__images-robot" src="../../images/header-robot.png" alt="robot">
        <img class="get-started__images-bottom" src="../../images/header-robot-under.png" alt="bottom">
      </div>
    </div>
  </section>
</template>

<script>
import CustomButton from "@/components/UI/CustomButton";

export default {
  name: "GetStarted",
  components: {
    CustomButton
  }
}
</script>

<style lang="scss" scoped>
@import "style";
</style>