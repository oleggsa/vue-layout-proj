<template>
  <div class="wrapper">
    <Header/>
    <GetStarted/>
    <Check/>
    <Why/>
    <Prices/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import GetStarted from "@/components/GetStarted";
import Check from "@/components/Check";
import Why from "@/components/Why";
import Prices from "@/components/Prices";

export default {
  name: 'App',
  components: {
    Why,
    Header,
    GetStarted,
    Check,
    Prices
  }
}
</script>

<style>

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
