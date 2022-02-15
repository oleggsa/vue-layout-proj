<template>
  <div class="wrapper">
    <Header :isSticky="true"/>
    <GetStarted/>
    <Check/>
    <Why/>
    <Prices/>
    <Feedback/>
    <Footer/>
    <Copyright/>
  </div>
</template>

<script>
import Header from './components/Header'
import GetStarted from "@/components/GetStarted";
import Check from "@/components/Check";
import Why from "@/components/Why";
import Prices from "@/components/Prices";
import Feedback from "@/components/Feedback";
import Footer from "@/components/Footer";
import Copyright from "@/components/Copyright";

export default {
  name: 'App',
  components: {
    Why,
    Header,
    GetStarted,
    Check,
    Prices,
    Feedback,
    Footer,
    Copyright
  }
}
</script>

<style>
@import "./assets/common/bootstrap-grid.min.css";
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Montserrat, sans-serif;
}
.wrapper {
  width: 1440px;
  margin: 0 auto;
}

a {
  text-decoration: none;
  color: black;
}
</style>
