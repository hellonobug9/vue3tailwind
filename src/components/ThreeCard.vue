<template>
  <div class="h-[100vh] bg-slate-300 p-20">
    <div
      class="mx-auto grid max-w-[1040px] grid-cols-2 rounded-2xl bg-white shadow-xl"
    >
      <div class="p-8">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta neque
        sapiente minus labore qui incidunt aperiam. Facilis molestias eius sit
        corrupti nulla similique nam, culpa aperiam. Corporis esse maiores, nisi
        enim, necessitatibus tempore facere tenetur veniam exercitationem
        placeat veritatis! Cum alias veniam totam tempora earum consequuntur,
        impedit repellat quae labore iste libero recusandae debit s corrupti,
        quos est tenetur. Culpa beatae, nobis quia adipisci perferendis
        asperiores eveniet officiis ex nemo
      </div>
      <div class="relative min-h-[524px]">
        <div
          class="absolute inset-0 top-0 left-0 right-0 bottom-0 flex flex-col space-y-4"
        >
          <div class="flex h-full space-x-4">
            <div class="h-full w-[445px] overflow-hidden rounded-br-3xl">
              <div class="h-full w-full bg-red-500"></div>
            </div>
            <div class="h-full w-[396px] overflow-hidden rounded-bl-3xl">
              <div class="h-full w-full bg-yellow-500"></div>
            </div>
          </div>
          <div class="flex h-full space-x-4">
            <div class="h-full w-[365px] overflow-hidden rounded-tr-3xl">
              <div class="h-full w-full bg-green-500"></div>
            </div>
            <div class="h-full w-[476px] overflow-hidden rounded-tl-3xl">
              <div class="h-full w-full bg-blue-500"></div>
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
