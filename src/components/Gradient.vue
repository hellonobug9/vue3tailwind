<template>
    <div class="gradient-bg w-full h-full">
        <slot></slot>
    </div>
</template>
<script setup lang="ts">
import { Disclosure, DisclosureButton, DisclosurePanel } from '@headlessui/vue'
import { ChevronDownIcon } from '@heroicons/vue/24/solid'
defineProps<{
  item: any;
}>();
</script>
<style>
.gradient-bg {
        display: flex;
        align-items: center;
        justify-content: center;
        margin: 0 0 1rem 0;
      }
      .gradient-bg {
        position: relative;
        z-index: 1; /* matters! */
        background: black;
      }
      .gradient-bg::before {
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: linear-gradient(105.94deg, #000000 0%, #48484A 126.45%);
        opacity: 0;
        transition: opacity 0.4s;
        z-index: -1;
      }
      .gradient-bg:hover::before {
        opacity: 1;
      }
</style>