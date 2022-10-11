<template>
  <div
    class="sticky top-[52px] z-10 bg-[#636366] bg-opacity-70 text-white drop-shadow-lg backdrop-blur-sm"
  >
    <div class="max-w-4xl mx-auto">
      <!-- DESKTOP -->
      <nav
        class="hidden h-10 w-full  items-center justify-between sm:flex"
      >
        <div>Live class</div>
        <ul class="flex gap-10">
          <li>Overview</li>
          <li>Why us</li>
          <li>Schedule</li>
        </ul>
        <div />
      </nav>

      <!-- MOBILE -->
      <div class="sm:hidden">
        <nav class="flex h-10 w-full items-center justify-between">
          <div>Live class</div>
          <div
            class="flex items-center justify-center gap-1"
            @click="open = !open"
          >
            Overview
            <ChevronDownIcon
              :class="[
                open ? 'back' : 'front',
                'text-gray-60 h-5 w-5 transition-all duration-300 hover:text-gray-400 sm:h-6 sm:w-6',
              ]"
              aria-hidden="true"
            />
          </div>
        </nav>
        <ul
          :class="[
            'absolute w-full overflow-hidden bg-[#636366] bg-opacity-70 drop-shadow-lg backdrop-blur-sm transition-all',
            open ? 'max-h-20 opacity-100' : 'max-h-0 opacity-0',
          ]"
        >
          <li>Overview</li>
          <li>Why us</li>
          <li>Schedule</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { ChevronDownIcon } from "@heroicons/vue/24/outline";
const open = ref(false);
</script>
