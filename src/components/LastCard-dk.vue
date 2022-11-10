<template>
  <div class="h-[100vh] bg-slate-300 p-20">
    <div class="group flex min-h-[444px] flex-col rounded-2xl bg-white p-4">
      <div class="px-8 py-12">
        <div class="">
          <div class="text-xs">Bài viết</div>
          <div class="text-4xl font-bold transition-all duration-300">
            Tâm lý học & Đời sống
          </div>
        </div>
      </div>
      <div class="relative grow overflow-hidden">
        <div class="absolute top-0 left-1/2 -translate-x-1/2 transform">
          <div class="flex space-x-2">
            <div class="">
              <div class="rounded-2xl overflow-hidden h-[448px] w-[284px]">
                <img
                  src="//unsplash.it/200/200"
                  class="h-full w-full object-cover"
                />
              </div>
            </div>
            <div class="space-y-2">
              <div class="rounded-2xl overflow-hidden h-[139px] w-[284px]">
                <img
                  src="//unsplash.it/200/200"
                  class="h-full w-full object-cover"
                />
              </div>
              <div class="rounded-2xl overflow-hidden h-[301px] w-[284px]">
                <img
                  src="//unsplash.it/200/200"
                  class="h-full w-full object-cover"
                />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
defineProps<{}>();
</script>
<style></style>
