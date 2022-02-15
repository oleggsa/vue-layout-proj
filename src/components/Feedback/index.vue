<template>
  <div class="feedback__wrapper">
    <div class="feedback__content">
      <div class="feedback__content-header">
        <p>Case Studies</p>
        <GradientRectangle></GradientRectangle>
      </div>
      <div class="feedback__content-deqsr">
        <p>Our Instagram marketing services are made for growth.<br>
          Must-have for business, influencers, digital marketing specialists</p>
      </div>
      <div class="feedback__user">
        <div class="feedback__user-photo">
          <img src="../../images/case-photo.png" alt="profile photo">
        </div>
        <div class="feedback__user-info">
          <div class="feedback__user-info-name">Xena_axyenna</div>
          <div class="feedback__user-info-date">Odessa, Ukraine | January 2021</div>
          <div class="feedback__user-info-rate">
            <img src="../../icons/star.png" alt="star" v-for="item of 5">
          </div>
          <div class="feedback__user-info-text">
            You can spend thousands of dollars on ads or<br>
            buying followers to try and build a meaningful<br>
            audience on Instagram before seeing that it’s a<br>
            complete waste
          </div>
        </div>
      </div>
      <CustomButton>GET STARTED</CustomButton>
    </div>
    <div class="feedback__images">
      <div class="feedback__images-phone"><img src="../../images/case-phone.png" alt="phone"></div>
      <div class="feedback__images-bottom"><img src="../../images/case-bottom.png" alt="bottom"></div>
      <div class="feedback__images-robot"><img src="../../images/case-robot.png" alt="robot"></div>
    </div>
  </div>
</template>

<script>
import GradientRectangle from "@/components/UI/GradientRectangle";
import CustomButton from "@/components/UI/CustomButton";

export default {
  name: "index",
  components: {GradientRectangle, CustomButton}
}
</script>

<style lang="scss" scoped>
@import "style";
</style>