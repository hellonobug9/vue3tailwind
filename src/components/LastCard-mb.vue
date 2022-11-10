<template>
    <div class="h-[100vh] bg-slate-300 p-20">
      <div
        class="group mx-auto grid min-h-[464px] max-w-[1040px] grid-cols-2 gap-4 rounded-2xl bg-white p-4 shadow-xl"
      >
        <div class="px-8 py-12">
          <div class="">
            <div class="text-xs">Bài viết</div>
            <div
              class="text-4xl font-bold transition-all duration-300 "
            >
              Tâm lý học & Đời sống
            </div>
            <div class="relative mt-6">
              Lý giải về các tình huống trong đời sống xã hội theo góc nhìn tâm lý
              học. Hàng nghìn bài báo khoa học trong và ngoài nước về chủ đề tâm
              lý. Nâng cao hiểu biết, từ đó nâng cao sức khỏe tinh thần và chất
              lượng cuộc sống.
              <div
                class="absolute bottom-0 left-0 right-0 z-10 h-full bg-white transition-all duration-300 group-hover:h-0"
              ></div>
            </div>
          </div>
        </div>
        <div class="relative overflow-hidden">
          <div
            class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 transform"
          >
            <div class="flex flex-col space-y-4">
              <div class="flex space-x-4">
                <div
                  class="h-[254px] w-[445px] cursor-pointer overflow-hidden rounded-3xl"
                >
                  <img
                    src="//unsplash.it/200/200"
                    class="h-full w-full object-cover"
                  />
                </div>
                <div
                  class="h-[254px] w-[396px] cursor-pointer overflow-hidden rounded-3xl"
                >
                  <img
                    src="//unsplash.it/200/200"
                    class="h-full w-full object-cover"
                  />
                </div>
              </div>
              <div class="flex space-x-4">
                <div
                  class="h-[254px] w-[365px] cursor-pointer overflow-hidden rounded-3xl"
                >
                  <img
                    src="//unsplash.it/200/200"
                    class="h-full w-full object-cover"
                  />
                </div>
                <div
                  class="h-[254px] w-[476px] cursor-pointer overflow-hidden rounded-3xl"
                >
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
  