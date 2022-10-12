<template>
  <div>
    <div
      class="flex cursor-pointer items-start justify-between"
      @click="open = !open"
    >
      <div
        class="text-mobileHeadline-6 sm:text-desktopHeadline-9 font-semibold"
      >
        {{ item.label }}
      </div>
      <div>
        <ChevronDownIcon
          :class="[
            open ? 'back' : 'front',
            'h-5 w-5 text-black transition-all duration-300 hover:text-black sm:h-6 sm:w-6',
          ]"
          aria-hidden="true"
        />
      </div>
    </div>
    <transition name="slide">
      <ul class="list" v-if="open">
        <li v-for="nav in item.items" :key="nav.id">
          {{ nav.label }}
        </li>
      </ul>
    </transition>
  </div>
</template>
<script setup lang="ts">
import { ref } from "vue";
import { ChevronDownIcon } from "@heroicons/vue/24/outline";
defineProps<{
  item: any;
}>();
const open = ref(false);
</script>
<style scoped="true">
.back {
  transform: rotateX(-180deg);
}

.front {
  transform: rotateX(0deg);
}

.list {
  width: 204px;
  margin: 0;
  padding: 0;
  list-style-type: none;
  transform-origin: top;
  transition: transform 0.4s ease-in-out;
  overflow: hidden;
}
li {
  padding: 10px;
  background: white;
  border-bottom: solid thin #eee;
  border-left: solid medium #cbc;
}
.slide-enter,
.slide-leave-to {
  transform: scaleY(0);
}
</style>
