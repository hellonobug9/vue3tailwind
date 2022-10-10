<template>
  <div
    class="sticky top-0 bg-[#636366] bg-opacity-70 drop-shadow-lg backdrop-blur-sm text-white"
  >
    <!-- DESKTOP -->
    <nav class=" hidden sm:flex h-10 w-full justify-between items-center ">
      <div>Live class</div>
      <ul class="flex gap-10">
        <li>Overview</li>
        <li>Why us</li>
        <li>Schedule</li>
      </ul>
      <div/>
    </nav>
    
    <!-- MOBILE -->
    <div class="sm:hidden">
    <nav class="flex h-10 w-full justify-between items-center ">
      <div>Live class</div>
      <div class="flex justify-center items-center gap-1" @click="open = !open">Overview <ChevronDownIcon
        :class="[
            open ? 'back' : 'front',
            'h-5 w-5 text-gray-60 transition-all duration-300 hover:text-gray-400 sm:h-6 sm:w-6',
        ]"
        aria-hidden="true"
    /></div>
    </nav>
    <ul :class="['absolute w-full transition-all bg-[#636366] bg-opacity-70 drop-shadow-lg backdrop-blur-sm overflow-hidden', open ? 'max-h-20 opacity-100':'max-h-0 opacity-0']">
      <li>Overview</li>
      <li>Why us</li>
      <li>Schedule</li>
    </ul>
  </div>
  </div>
</template>

<script lang="ts" setup>
import { ChevronDownIcon } from '@heroicons/vue/24/outline';
const open = ref(false);

</script>
