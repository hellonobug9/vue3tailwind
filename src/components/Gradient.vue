<template>
  <div class="gradient h-full w-full">
    <slot></slot>
  </div>
</template>
<script setup lang="ts">
import { Disclosure, DisclosureButton, DisclosurePanel } from "@headlessui/vue";
import { ChevronDownIcon } from "@heroicons/vue/24/solid";
defineProps<{
  item: any;
}>();
</script>
<style>
.gradient {
  position: relative;
  min-height: 200px;
  background: black;
  z-index: 1;
}

.gradient::before {
  position: absolute;
  content: "";
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  background-image: linear-gradient(to bottom right, black, gray);
  z-index: -1;
  transition: opacity 0.3s linear;
  opacity: 0;
}
.gradient:hover::before {
  opacity: 0.5;
}
</style>
