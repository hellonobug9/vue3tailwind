<template>
  <div class="navigation-wrapper keen-slider-container">
    <div ref="container" class="keen-slider over-visible">
      <div class="keen-slider__slide flex items-center space-x-4 overflow-visible">
        <div class="number-slide1 w-1/4 flex-shrink-0">1</div>
        <div class="number-slide2 w-1/4 flex-shrink-0">2</div>
        <div class="number-slide3 w-1/4 flex-shrink-0">3</div>
        <div class="number-slide4 w-1/4 flex-shrink-0">4</div>
      </div>
      <div class="keen-slider__slide flex items-center space-x-4">
        <div class="number-slide5 w-1/4 flex-shrink-0">5</div>
        <div class="number-slide6 w-1/4 flex-shrink-0">6</div>
      </div>
    </div>
    <svg
      @click="slider.prev()"
      :class="{
        arrow: true,
        'arrow--left': true,
        'arrow--disabled': current === 0,
      }"
      xmlns="http://www.w3.org/2000/svg"
      viewBox="0 0 24 24"
    >
      <path
        d="M16.67 0l2.83 2.829-9.339 9.175 9.339 9.167-2.83 2.829-12.17-11.996z"
      ></path>
    </svg>
    <svg
      v-if="slider"
      @click="slider.next()"
      :class="{
        arrow: true,
        'arrow--right': true,
        'arrow--disabled': current === slider.track.details.slides.length - 1,
      }"
      xmlns="http://www.w3.org/2000/svg"
      viewBox="0 0 24 24"
    >
      <path d="M5 3l3.057-3 11.943 12-11.943 12-3.057-3 9-9z"></path>
    </svg>
  </div>
  <div v-if="slider" class="dots">
    <button
      v-for="(_slide, idx) in dotHelper"
      @click="slider.moveToIdx(idx)"
      :class="{ dot: true, active: current === idx }"
      :key="idx"
    ></button>
  </div>
</template>

<script>
import { computed, ref } from "vue";

import { useKeenSlider } from "keen-slider/vue.es";
import "keen-slider/keen-slider.min.css";

export default {
  setup() {
    const current = ref(0);
    const [container, slider] = useKeenSlider({
      mode: "free-snap",
      slides: {
        spacing: 16,
      },
      initial: current.value,
      rtl: false,

      slideChanged: (s) => {
        current.value = s.track.details.rel;
      },
    });

    const dotHelper = computed(() => {
      console.log(
        "hola",
        slider.value
          ? [...Array(slider.value.track.details.slides.length).keys()]
          : []
      );
      return slider.value
        ? [...Array(slider.value.track.details.slides.length).keys()]
        : [];
    });
    console.log(slider);
    return { container, current, dotHelper, slider };
  },
};
</script>

<style>
[class^="number-slide"],
[class*=" number-slide"] {
  background: grey;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 50px;
  color: #fff;
  font-weight: 500;
  height: 200px;
}

.item {
  height: 324px;
}
.number-slide1 {
  background: rgb(64, 175, 255);
  background: linear-gradient(
    128deg,
    rgba(64, 175, 255, 1) 0%,
    rgba(63, 97, 255, 1) 100%
  );
}
.number-slide2 {
  background: rgb(255, 75, 64);
  background: linear-gradient(
    128deg,
    rgba(255, 154, 63, 1) 0%,
    rgba(255, 75, 64, 1) 100%
  );
}
.number-slide3 {
  background: rgb(182, 255, 64);
  background: linear-gradient(
    128deg,
    rgba(182, 255, 64, 1) 0%,
    rgba(63, 255, 71, 1) 100%
  );
  background: linear-gradient(
    128deg,
    rgba(189, 255, 83, 1) 0%,
    rgba(43, 250, 82, 1) 100%
  );
}
.number-slide4 {
  background: rgb(64, 255, 242);
  background: linear-gradient(
    128deg,
    rgba(64, 255, 242, 1) 0%,
    rgba(63, 188, 255, 1) 100%
  );
}
.number-slide5 {
  background: rgb(255, 64, 156);
  background: linear-gradient(
    128deg,
    rgba(255, 64, 156, 1) 0%,
    rgba(255, 63, 63, 1) 100%
  );
}
.number-slide6 {
  background: rgb(64, 76, 255);
  background: linear-gradient(
    128deg,
    rgba(64, 76, 255, 1) 0%,
    rgba(174, 63, 255, 1) 100%
  );
}
.navigation-wrapper {
  position: relative;
}
.dots {
  display: flex;
  padding: 10px 0;
  justify-content: center;
}
.dot {
  border: none;
  width: 10px;
  height: 10px;
  background: #c5c5c5;
  border-radius: 50%;
  margin: 0 5px;
  padding: 5px;
  cursor: pointer;
}
.dot:focus {
  outline: none;
}
.dot.active {
  background: #000;
}
.arrow {
  width: 30px;
  height: 30px;
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  -webkit-transform: translateY(-50%);
  fill: #fff;
  cursor: pointer;
}
.arrow--left {
  left: 5px;
}
.arrow--right {
  left: auto;
  right: 5px;
}
.arrow--disabled {
  fill: rgba(255, 255, 255, 0.5);
}

.keen-slider-container {
 
}
.over-visible {
  overflow: visible !important;
}
</style>
