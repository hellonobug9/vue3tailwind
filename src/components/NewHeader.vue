<template>
  <div class="sticky top-0 z-50 h-[3rem] w-[100vw] text-white transition-all">
    <div
      class="absolute top-0 w-full bg-gray-600 bg-opacity-80 backdrop-blur-sm transition-all ease-in-out"
      :class="[searching ? 'max-h-[10rem]' : 'max-h-[3rem]']"
    >
      <div class="flex h-[3rem] w-full justify-between px-6">
        <div class="flex items-center justify-center" @click="toggleOpening()">
          <div>Menu</div>
        </div>
        <div class="flex items-center justify-center">
          <div>Logo</div>
        </div>
        <div class="flex items-center justify-center">
          <div @click="toggleSearching()">
            <XCircleIcon class="h-6 w-6" />
          </div>
        </div>
      </div>
      <Transition name="search-fade" class="w-full">
        <div
          v-if="searching"
          class="flex w-full items-center justify-center transition-all duration-1000"
        >
          <input
            id="search"
            :value="term"
            class="bg-gray-[#F2F2F7] focus:bg-gray-10 block w-1/2 rounded-[0.625rem] border-none p-4 pl-10 text-sm text-gray-900 focus:border-transparent focus:ring-transparent sm:rounded-2xl"
            placeholder="Search for anything"
            type="search"
            @input="onChange"
          />
        </div>
      </Transition>
      <Transition name="dropdown-fade" class="w-full">
        <div
          v-if="opening"
          class="absolute top-[3rem] z-50 flex min-h-[15rem] w-full flex-col items-center justify-between bg-gray-600"
        >
          <input
            id="search"
            :value="term"
            class="bg-gray-[#F2F2F7] focus:bg-gray-10 block w-1/2 rounded-[0.625rem] border-none p-4 pl-10 text-sm text-gray-900 focus:border-transparent focus:ring-transparent sm:rounded-2xl"
            placeholder="Search for anything"
            type="search"
            @input="onChange"
          />
        </div>
      </Transition>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { ChevronDownIcon, XCircleIcon } from "@heroicons/vue/24/outline";
const term = ref("");
const searching = ref(false);
const opening = ref(false);

const toggleSearching = () => {
  searching.value = !searching.value;
};

const toggleOpening = () => {
  opening.value = !opening.value;
};

// const status = ref<"hiding" | "searching" | "opening">("hiding");
// const changeStatus = (next: "hiding" | "searching" | "opening") => {
//   if (status.value === next) {
//     status.value = "hiding";
//   } else {
//     status.value = next;
//   }
//   console.log("status", status.value);
// };
// const searching = ref(false);
// const opening = ref(false);
// const toggleSearching = () => {
//   searching.value = !searching.value;
//   if (opening.value) {
//     opening.value = false;
//   }
// };

// const toggleOpening = () => {
//   searching.value = !opening.value;
//   opening.value = !opening.value;
// };

// const term = ref("");
const onChange = (value: any) => {
  console.log(1, value);
  term.value = value.target.value;
};
// const clearInput = () => {
//   term.value = "";
//   toggleSearching();
// };
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
