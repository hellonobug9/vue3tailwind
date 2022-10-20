<template>
  <div
    class="h-[20rem] top-0 sticky overflow-hidden bg-gray-600 px-6 text-white transition-all z-50"
    :class="{
      'max-h-[3rem]': status === 'hiding',
      'max-h-[10rem]': status === 'searching',
      'max-h-[20rem]': status === 'opening',
    }"
  >
    <div class="flex h-[3rem] w-full justify-between">
      <div class="flex items-center justify-center">
        <div>Menu</div>
      </div>
      <div class="flex items-center justify-center">
        <div>Logo</div>
      </div>
      <div class="flex items-center justify-center">
        <div @click="changeStatus('searching')">
          <XCircleIcon class="h-6 w-6" />
        </div>
      </div>
    </div>

    <div class="">
      <input
        id="search"
        :value="term"
        class="bg-gray-[#F2F2F7] focus:bg-gray-10 block w-full rounded-[0.625rem] border-none p-4 pl-10 text-sm text-gray-900 focus:border-transparent focus:ring-transparent sm:rounded-2xl"
        placeholder="Search for anything"
        type="search"
        @input="onChange"
      />
    </div>
  </div>
</template>

<script lang="ts" setup>
import { ChevronDownIcon, XCircleIcon } from "@heroicons/vue/24/outline";
const status = ref<"hiding" | "searching" | "opening">("hiding");
const changeStatus = (next: "hiding" | "searching" | "opening") => {
  if (status.value === next) {
    status.value = "hiding";
  } else {
    status.value = next;
  }
};
const searching = ref(false);
const opening = ref(false);
const toggleSearching = () => {
  searching.value = !searching.value;
  if (opening.value) {
    opening.value = false;
  }
};

const toggleOpening = () => {
  searching.value = !opening.value;
  opening.value = !opening.value;
};

const term = ref("");
const onChange = (value: any) => {
  console.log(1, value);
  term.value = value.target.value;
};
const clearInput = () => {
  term.value = "";
  toggleSearching();
};
</script>

<style scoped>
/*Vue JS CSS Components*/
.slide-fade-enter-active {
  transition: opacity 0.15s ease;
}

.slide-fade-enter {
  transition: opacity 0.15s ease;
}

.slide-fade-leave-active {
  transition: opacity 0.15s ease;
}

.slide-fade-leave-to, .slide-fade-enter-from
  /* .slide-fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>
