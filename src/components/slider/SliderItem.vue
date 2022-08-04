<template>
  <transition :name="transitionEffect">
    <div class="slider-item" v-show="currentSlide === index">
      <img class="slider-image" :src="slide" />
    </div>
  </transition>
</template>

<script>
import { computed } from "@vue/runtime-core";
export default {
  props: ["slide", "currentSlide", "index", "direction"],
  computed: {
    transitionEffect() {
      return this.direction === "right" ? "slide-out" : "slide-in";
    },
  },
};
</script>

<style scoped>
.slider-item {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
}
.slider-image {
  height: 624px;
  width: 100%;
  padding-bottom: 1rem;
}

.slide-in-enter-active,
.slide-in-leave-active,
.slide-out-enter-active,
.slide-out-leave-active {
  transition: 0.4s ease-in-out;
}
.slide-in-enter-from {
  transform: translateX(-100%);
}
.slide-in-leave-to {
  transform: translateX(100%);
}
.slide-out-enter-from {
  transform: translateX(100%);
}
.slide-out-leave-to {
  transform: translateX(-100%);
}
</style>
