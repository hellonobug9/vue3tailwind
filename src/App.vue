<template>
  <div class="relative">
    <LastCardDk :cssVars="cssVars" />
  </div>
</template>
<script setup>
import Progress from "./components/Progress.vue";
import MultiImageCard from "./components/MultiImageCard.vue";
import FAQ from "./components/FAQ.vue";
import Input from "./components/Input.vue";
import Gradient from "./components/Gradient.vue";
import AppHeader from "./components/AppHeader.vue";
import AppSubHeader from "./components/SubHeader.vue";
import Footer from "./components/Footer.vue";
import FlippedImage from "./components/FlippedImage.vue";
import Review from "./components/Review.vue";
import NewHeader from "./components/NewHeader.vue";
import NewSubHeader from "./components/NewSubHeader.vue";
import ThreeCard from "./components/ThreeCard.vue";
import LastCardDk from "./components/LastCard-dk.vue";

const cssVars = computed(() => ({
  "--bg-color": "linear-gradient(260.99deg, #FF512F 0%, #DD2476 100%)",
}));
</script>
