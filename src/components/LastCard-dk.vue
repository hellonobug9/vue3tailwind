<template>
  <button :style="cssVars">hello</button>
</template>
<script setup lang="ts">
defineProps<{
  cssVars: any
}>();

</script>
<style>
button {
  position: relative;
  -webkit-appearance: none;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background: transparent;
  font-size: 16px;
  text-transform: uppercase;
  color: #fff;
  font-weight: 500;
  padding: 10px 15px;
  margin: 5px;
  border-radius: 5px;
  border: none;
  min-width: 150px;
}
button::before {
  content: "";
  background-image: var(--bg-color);
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  z-index: -1;
  border-radius: 5px;
}
button::after {
  content: "";
  opacity: 0;
  background-image: var(--bg-color);
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  z-index: -1;
  transition: opacity 500ms ease;
  border-radius: 5px;
}
</style>
