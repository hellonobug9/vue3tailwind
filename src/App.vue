<template>
  <div class="bg-[#F5F5F5] py-20">
    <div class="mx-auto mt-20 grid max-w-4xl grid-cols-3 gap-4">
      <FlippedImage
        :mode="'white'"
        :image-url="'https://picsum.photos/600/200'"
        :can-flip="true"
        :min-height="'min-h-[400px]'"
      />
      <FlippedImage
        :mode="'white'"
        :image-url="'https://picsum.photos/600/200'"
        :can-flip="true"
        :min-height="'min-h-[400px]'"
      />
      <FlippedImage
        :mode="'white'"
        :image-url="'https://picsum.photos/600/200'"
        :can-flip="true"
        :min-height="'min-h-[400px]'"
      />
    </div>
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
</script>
