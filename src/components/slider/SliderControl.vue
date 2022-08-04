<template>
  <button class="slider-control left" @click="$emit('prev')">
    {{ prev }}
  </button>
  <button class="slider-control right" @click="$emit('next')">
    {{ next }}
  </button>
</template>

<script>
export default {
  emits: ["next", "prev"],
  data: () => {
    return {
      next: ">",
      prev: "<",
    };
  },
};
</script>

<style scoped>
.slider-control {
  border: none;
  display: inline-block;
  position: absolute;
  height: 50px;
  width: 50px;
  color: #72c172;
  top: calc(50% + 50px);
  background-color: transparent;
  font-size: 24px;
  font-weight: bold;
}
.left {
  left: 20%;
}
.right {
  right: 20%;
}
</style>
