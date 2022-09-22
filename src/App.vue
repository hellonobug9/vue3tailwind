<template>
  <div class='p-16'>
   <div class="text-green-600 text-3xl">Vue3</div>
   <Progress :total="40" :complete="32"/>
  </div>
</template>
<script setup>
    import Progress from "./components/Progress.vue"
    console.log('Hello no bug');
</script>