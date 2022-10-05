<template>
  <div class="mx-auto max-w-[65rem] space-y-12 p-10">
    <div class="text-3xl text-green-600">Vue3</div>
    <Input/>
    <Gradient class="h-[20rem] w-[10rem]">
      <div class="text-white">Hello no bug</div>
    </Gradient>
    <!-- <FAQ/> -->
    <!-- <Progress :total="40" :complete="32"/> -->
    <!-- <MultiImageCard /> -->
  </div>
</template>
<script setup>
import Progress from "./components/Progress.vue";
import MultiImageCard from "./components/MultiImageCard.vue";
import FAQ from "./components/FAQ.vue";
import Input from "./components/Input.vue";
import Gradient from "./components/Gradient.vue";

console.log("Hello no bug");
</script>
