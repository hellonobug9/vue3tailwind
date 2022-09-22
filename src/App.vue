<template>
  <div class="mx-auto max-w-[65rem]">
    <div class="text-3xl text-green-600">Vue3</div>
    <!-- <Progress :total="40" :complete="32"/> -->
    <MultiImageCard />
  </div>
</template>
<script setup>
import Progress from "./components/Progress.vue";
import MultiImageCard from "./components/MultiImageCard.vue";

console.log("Hello no bug");
</script>
