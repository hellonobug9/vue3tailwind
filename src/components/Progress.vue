<template>
  <div class="bg-[#E5E5EA] rounded-3xl">
    <div
      class="bg-gradient-to-r from-[#FF8008] to-[#FFC837] font-semibold text-end rounded-3xl p-1"
      :style="`width: ${(complete / total) * 100}%`"
    >
      <div
        class="bg-white rounded-full shadow-2xl flex justify-center items-center w-8 h-8 ml-auto"
      >
        {{ complete }}
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
defineProps<{
  total: number;
  complete: number;
}>();
</script>
