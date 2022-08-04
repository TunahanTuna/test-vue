<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import Footer from "./components/footer/Footer.vue";
import Slider from "./components/slider/Slider.vue";
import Members from "./components/members/members.vue";
import Card from "./components/card/Cards.vue";
import About from "./components/about/About.vue";
</script>

<template>
  <div class="test">
    <Slider />
    <About />
    <Card />
    <Members />
    <Footer />
  </div>
</template>

<style>
* {
  padding: 0;
  margin: 0;
}
</style>
