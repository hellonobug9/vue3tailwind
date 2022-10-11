<template>
  <div
    class="sticky top-0 z-20 h-[52px] bg-[#F9F9FB] bg-opacity-70 text-black drop-shadow-lg backdrop-blur-sm"
  >
    <div
      class="absolute inset-0 hidden h-full w-full bg-gradient-to-t from-gray-100 via-gray-200/20 to-gray-100/10 sm:block"
    ></div>

    <div class="relative mx-auto h-full w-full max-w-4xl">
      <nav class="relative flex h-full w-full items-center justify-between">
        <!-- LOGO -->
        <div class="sm:order-0 order-1">Logo</div>
        
        <!-- MENU -->
        <div class="order-0 sm:order-1">
          <div class="h-6 w-6 sm:hidden" @click="toggleOpening">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              strokeWidth="{1.5}"
              stroke="currentColor"
              className="w-full h-full object-cover"
            >
              <path
                strokeLinecap="round"
                strokeLinejoin="round"
                d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
              />
            </svg>
          </div>
          <ul class="hidden gap-10 sm:flex">
            <li>Overview</li>
            <li>Why us</li>
            <li>Schedule</li>
          </ul>
        </div>

        <!-- SEARCH ICON -->
        <div
          @click="toggleSearching"
          class="order-2 flex flex-shrink-0 items-center justify-end sm:w-[344px]"
          :class="[opening && 'pointer-events-none opacity-0 sm:opacity-100']"
        >
          <svg
            v-if="!searching"
            aria-hidden="true"
            class="h-5 w-5 text-black"
            fill="none"
            stroke="currentColor"
            viewBox="0 0 24 24"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
            ></path>
          </svg>
          <svg
            v-if="searching"
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            strokeWidth="{1.5}"
            stroke="currentColor"
            class="h-5 w-5 text-black sm:hidden"
          >
            <path
              strokeLinecap="round"
              strokeLinejoin="round"
              d="M6 18L18 6M6 6l12 12"
            />
          </svg>
        </div>

        <!-- DROPDOWN -->
        <Transition name="slide-fade">
          <div
            class="absolute top-[52px] w-full bg-[#F9F9FB] sm:right-0 sm:top-0 sm:w-[344px] sm:bg-transparent"
            v-if="searching"
          >
            <div class="mx-auto">
              <div class="relative">
                <div
                  class="pointer-events-none absolute inset-y-0 left-0 flex items-center pl-3"
                >
                  <svg
                    aria-hidden="true"
                    class="h-5 w-5 text-gray-500"
                    fill="none"
                    stroke="currentColor"
                    viewBox="0 0 24 24"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      stroke-width="2"
                    ></path>
                  </svg>
                </div>
                <input
                  id="search"
                  :value="term"
                  class="bg-gray-[#F2F2F7] focus:bg-gray-10 block w-full rounded-[0.625rem] border-none p-4 pl-10 text-sm text-gray-900 focus:border-transparent focus:ring-transparent sm:rounded-2xl"
                  placeholder="Search for anything"
                  type="search"
                  @change="onChange"
                />
                <button
                  class="absolute right-2.5 bottom-2.5 h-8 w-8 rounded-lg px-1 py-2 text-sm font-medium"
                  @click="clearInput"
                >
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    strokeWidth="{1.5}"
                    stroke="currentColor"
                    className="w-full  h-full object-cover"
                  >
                    <path
                      strokeLinecap="round"
                      strokeLinejoin="round"
                      d="M9.75 9.75l4.5 4.5m0-4.5l-4.5 4.5M21 12a9 9 0 11-18 0 9 9 0 0118 0z"
                    />
                  </svg>
                </button>
              </div>
              <ul v-if="opening" class="w-full sm:hidden">
                <li>Overview</li>
                <li>Why us</li>
                <li>Schedule</li>
              </ul>
            </div>
            <div
              class="absolute top-20 right-0 hidden w-full rounded-3xl bg-white py-6 px-8 shadow-xl sm:block"
            >
              <p>Suggestions</p>
              <ul>
                <li>Trauma</li>
              </ul>
            </div>
          </div>
        </Transition>
      </nav>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { ChevronDownIcon, XCircleIcon } from "@heroicons/vue/24/outline";
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
