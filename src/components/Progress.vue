<template>
  <div class="rounded-3xl bg-[#E5E5EA]">
    <div
      class="rounded-3xl bg-gradient-to-r from-[#FF8008] to-[#FFC837] p-1 text-end font-semibold"
      :style="`width: ${(complete / total) * 100}%`"
    >
      <div
        class="ml-auto flex h-8 w-8 items-center justify-center rounded-full bg-white shadow-2xl"
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
