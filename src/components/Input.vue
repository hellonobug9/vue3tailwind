<template>
    <label
  for="UserEmail"
  class="relative block overflow-hidden rounded-md border-none bg-gray-100 hover:bg-gray-200 px-3.5 pt-6 pb-2 shadow-sm"
>
  <input
    type="email"
    id="UserEmail"
    placeholder="Email"
    class="peer w-full border-none bg-transparent p-0 placeholder-transparent focus:border-transparent focus:outline-none focus:ring-0"
  />

  <span
    class="absolute left-3 top-[18px] -translate-y-1/2 text-xs text-gray-700 transition-all peer-placeholder-shown:top-1/2 peer-placeholder-shown:text-sm peer-focus:top-[18px] peer-focus:text-xs"
  >
    Email
  </span>
</label>
</template>
<script setup lang="ts">
import { Disclosure, DisclosureButton, DisclosurePanel } from '@headlessui/vue'
import { ChevronDownIcon } from '@heroicons/vue/24/solid'
defineProps<{
  item: any;
}>();

</script>
<style>
    
</style>