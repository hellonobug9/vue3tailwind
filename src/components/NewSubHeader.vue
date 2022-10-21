<template>
  <div
    class="sticky top-[3rem] h-[3rem] w-[100vw] bg-red-800 text-white transition-all"
  ></div>
</template>

<script lang="ts" setup>
import { ChevronDownIcon, XCircleIcon } from "@heroicons/vue/24/outline";

const opening = ref(false);

const toggleOpening = () => {
  opening.value = !opening.value;
};
</script>

<style scoped>
/*Vue JS CSS Components*/
.dropdown-fade-enter-active {
  transition: opacity 0.7s ease;
}

.dropdown-fade-enter {
  transition: opacity 0.7s ease;
}

.dropdown-fade-leave-active {
  transition: opacity 0.7s ease;
}

.dropdown-fade-leave-to, .dropdown-fade-enter-from
    /* .dropdown-fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}

.search-fade-enter-active {
  transition: opacity 0.7s ease;
}

.search-fade-enter {
  transition: opacity 0.7s ease;
}

.search-fade-leave-active {
  transition: opacity 0.1s ease;
}

.search-fade-leave-to, .search-fade-enter-from
    /* .search-fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>
