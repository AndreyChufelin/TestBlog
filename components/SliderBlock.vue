<script setup>
const props = defineProps({
  data: Array,
});

const currentIndex = ref(0);
const animation = ref("slide");

function prev() {
  animation.value = "slide-prev";
  currentIndex.value--;
}
function next() {
  animation.value = "slide";
  currentIndex.value++;
}
</script>

<template lang="pug">
section(class="slider container")
  button(class="slider__button" @click="prev")
    svg(width="12" height="21" viewBox="0 0 12 21" fill="none" xmlns="http://www.w3.org/2000/svg")
      path(d="M10.4351 19L2.65688 11.2218C2.26636 10.8313 2.26636 10.1981 2.65688 9.80761L10.4351 2.02944" stroke="#D9D9D9" stroke-width="3" stroke-linecap="round")
  TransitionGroup(:name="animation" tag="div" class="slides")
    div(v-for="i in [currentIndex]" :key="i")
      img( :src="data[Math.abs(i) % data.length]")
  button(class="slider__button" @click="next") 
    svg(width="12" height="21" viewBox="0 0 12 21" fill="none" xmlns="http://www.w3.org/2000/svg")
      path(d="M1.56494 2L9.34312 9.77817C9.73364 10.1687 9.73364 10.8019 9.34312 11.1924L1.56494 18.9706" stroke="#D9D9D9" stroke-width="3" stroke-linecap="round")
</template>

<style scoped lang="scss">
.slider {
  display: flex;
  justify-content: space-between;
  align-items: center;

  &__button {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 60px;
    height: 60px;
    background-color: #1b1b1b;
  }
}

.slide-enter-active {
  transition: all 1s;
}
.slide-leave-active {
  transition: all 0.8s;
}

.slide-enter-from {
  transform: translate(100%, 0);
}
.slide-leave-to {
  transform: translate(-100%, 0);
}

.slide-prev-enter-active {
  transition: all 1s;
}
.slide-prev-leave-active {
  transition: all 0.8s;
}

.slide-prev-enter-from {
  transform: translate(-100%, 0);
}
.slide-prev-leave-to {
  transform: translate(100%, 0);
}
.slides {
  --slide-height: 550px;
  overflow: hidden;
  position: relative;
  height: 200px;
  width: 70%;
  height: var(--slide-height);
  margin: 0 5px;

  @media (max-width: 768px) {
    --slide-height: 320px;
  }
  @media (max-width: 576px) {
    --slide-height: 200px;
  }
}
.slides img {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  width: 100%;
  height: var(--slide-height);
  object-fit: cover;
}
</style>
