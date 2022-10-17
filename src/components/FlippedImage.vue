<template>
  <div
    class="relative flex h-80 flex-col overflow-hidden rounded-3xl shadow-2xl"
  >
    <div
      v-if="canFlip"
      class="absolute z-10 cursor-pointer transition-all"
      :class="[
        flipping && 'rotate-45',
        'text-black',
        customFlipBtnPosition,
        customFlipBtnSize,
      ]"
      @mouseenter="onMouseDown"
      @mouseleave="onMouseLeave"
      @click="toggleFlipping"
    >
      <svg
        width="40"
        height="40"
        viewBox="0 0 40 40"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
        class="h-8 w-8 sm:h-10 sm:w-10 text-red-500 "
      >
        <path
          d="M17.4248 26.6004L22.8581 21.1671C23.4998 20.5254 23.4998 19.4754 22.8581 18.8337L17.4248 13.4004"
          stroke="currentColor"
          stroke-width="2.4"
          stroke-miterlimit="10"
          stroke-linecap="round"
          stroke-linejoin="round"
        />
        <rect
          x="1.2"
          y="1.2"
          width="37.6"
          height="37.6"
          rx="18.8"
          stroke="currentColor"
          stroke-width="2.4"
        />
      </svg>
      <PlusCircleIconOutline v-if="isOutline" class="h-full w-full" />
      <PlusCircleIcon v-else class="h-full w-full" />
    </div>
    <div
      class="group absolute top-0 isolate flex h-3/4 w-full overflow-hidden bg-black transition-all"
    >
      <!-- the image -->
      <img
        v-if="imageUrl"
        class="absolute inset-0 h-full w-full transform bg-cover bg-center object-cover opacity-80 transition-all duration-500 ease-in-out"
        :class="[
          canDarken && 'group-hover:opacity-50',
          canZoom && 'group-hover:scale-105',
          !flipping ? 'opacity-80' : 'opacity-30',
        ]"
        :src="'https://picsum.photos/600/200'"
        alt="background-image"
      />
    </div>
    <div
      class="absolute bottom-0 w-full bg-white transition-all duration-500 ease-in-out"
      :class="[!flipping ? 'h-1/4' : 'h-full']"
    >
      <div class="h-full w-full">
        <transition
          class="duration-600 transition-opacity"
          enter-active-class="opacity-100"
          enter-from-class="opacity-0"
          leave-from-class="opacity-100"
          leave-active-class="opacity-0"
        >
          <div
            v-if="!flipping"
            class="absolute inset-0 flex h-full w-full items-center px-5"
          >
            <p class="text-xl font-semibold text-black">Effective</p>
          </div>
        </transition>
        <!-- second content -->
      </div>
    </div>
    <div
      class="absolute h-full w-full bg-white transition-all duration-500 ease-in-out"
      :class="[!flipping ? 'top-[100%]' : 'top-0']"
    >
      <transition
        class="transition-opacity duration-300"
        enter-active-class="opacity-100"
        enter-from-class="opacity-0"
        leave-from-class="opacity-100"
        leave-active-class="opacity-0"
      >
        <div
          v-if="flipping"
          class="absolute inset-0 flex h-full w-full items-center px-5"
        >
          <p class="text-lg font-semibold text-black">
            We have adapted techniques from psychology and neuroscience into a
            collection of simple guided sessions.
          </p>
        </div>
      </transition>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { ref } from "vue";
import { PlusCircleIcon } from "@heroicons/vue/24/solid";
import { PlusCircleIcon as PlusCircleIconOutline } from "@heroicons/vue/24/outline";
withDefaults(
  defineProps<{
    imageUrl: string;
    minHeight: string;
    canZoom?: boolean;
    canDarken?: boolean;
    canGradient?: boolean;
    customRounded?: string;
    canRise?: boolean;
    mode?: "black" | "white";
    // handle flip
    canFlip?: boolean;
    customFlipBtnPosition?: string;
    customFlipBtnSize?: string;
  }>(),
  {
    imageUrl: "",
    minHeight: "",
    canZoom: true,
    canDarken: true,
    canFlip: false,
    canGradient: false,
    canRise: false,
    mode: "black",
    customFlipBtnPosition: "bottom-5 right-5 sm:bottom-5 sm:right-5",
    customFlipBtnSize: "w-10 h-10",
  }
);
const flipping = ref(false);
const toggleFlipping = () => {
  flipping.value = !flipping.value;
};
const isOutline = ref(true);
const onMouseDown = () => {
  isOutline.value = false;
};
const onMouseLeave = () => {
  isOutline.value = true;
};
</script>

<style scoped></style>
