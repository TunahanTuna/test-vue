<template>
  <div class="slider">
    <div class="slider-inner">
      <slider-item
        v-for="(slide, index) in slides"
        :key="`item-${index}`"
        :slide="slide"
        :current-slide="currentSlide"
        :index="index"
        :direction="direction"
      />
      <slider-control @prev="prev" @next="next"></slider-control>
    </div>
  </div>
</template>

<script>
import SliderItem from "./SliderItem.vue";
import SliderControl from "./SliderControl.vue";
export default {
  data: () => ({
    slides: [
      "https://ifl.com.tr/images/screen%20shot%202022-06-16%20at%20160022.jpg?crc=143406598",
      "https://ifl.com.tr/images/---%20---.jpg?crc=84542685",
      "https://ifl.com.tr/images/vaccine-4892048.jpg?crc=415578437",
    ],
    currentSlide: 2,
    slideInterval: null,
    direction: "right",
  }),
  methods: {
    setCurrentSlide(index) {
      this.currentSlide = index;
    },
    prev() {
      const index =
        this.currentSlide > 0 ? this.currentSlide - 1 : this.slides.length - 1;
      this.setCurrentSlide(index);
      this.direction = "left";
      this.startSliderInterval();
    },
    _next() {
      const index =
        this.currentSlide < this.slides.length - 1 ? this.currentSlide + 1 : 0;
      this.setCurrentSlide(index);
      this.direction = "right";
    },
    next() {
      this._next();
      this.startSliderInterval();
    },
    startSliderInterval() {
      this.stopSliderInterval();
      this.slideInterval = setInterval(() => {
        this._next();
      }, 6000);
    },
    stopSliderInterval() {
      clearInterval(this.slideInterval);
    },
  },
  mounted() {
    this.startSliderInterval();
  },
  beforeUnmount() {
    this.stopSliderInterval();
  },
  components: {
    SliderItem,
    SliderControl,
  },
};
</script>

<style scoped>
.slider {
  display: flex;
  justify-content: center;
  width: 100%;
  min-width: 900px;
  height: 624px;
}
.slider-inner {
  position: relative;
  width: 100%;
  height: 624px;
  overflow: hidden;
}
</style>
