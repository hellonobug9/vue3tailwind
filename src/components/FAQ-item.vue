<template>
    <div class="bg-gray-50 space-y-12">
      <div class="space-y-2 border-b border-blue-400 pb-5">
        <div class="flex items-center justify-between">
            <div>
             {{item.question}}
            </div>
            <div @click="open = !open">
                <ChevronDownIcon :class="[open ? 'back' : 'front', 'h-6 w-6 transition-all duration-300 text-[#636366] hover:text-black']" aria-hidden="true" />
            </div>
        </div>
        <div :class="['font-xs text-gray-500 transition-all duration-300 overflow-hidden', open ? 'max-h-20':'max-h-0']">
            <span :class="['duration-1000', open ? 'opacity-100' : 'opacity-0']">{{item.answer}}</span>
        </div>
      </div>
    </div>
</template>
<script setup lang="ts">
import { Disclosure, DisclosureButton, DisclosurePanel } from '@headlessui/vue'
import { ChevronDownIcon } from '@heroicons/vue/24/solid'
defineProps<{
  item: any;
}>();
const faqs = [
  {
    id: 1,
    question: "What's the best thing about Switzerland?",
    answer:
      " I don't know, but the flag is a big plus. I don't know, but the flag is a big plus. I don't know, but the flag is a big plus. I don't know, but the flag is a big plus. I don't know, but the flag is a big plus. I don't know, but the flag is a big plus. Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas cupiditate laboriosam fugiat.",
  },
  {
    id: 2,
    question: "What's the best thing about Switzerland?",
    answer:
      "I don't know, but the flag is a big plus. Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas cupiditate laboriosam fugiat.",
  },
  {
      id: 3,
    question: "What's the best thing about Switzerland?",
    answer:
      "I don't know, but the flag is a big plus. Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas cupiditate laboriosam fugiat.",
  },
  {
    id: 4,
    question: "What's the best thing about Switzerland?",
    answer:
      "I don't know, but the flag is a big plus. Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas cupiditate laboriosam fugiat.",
  },
  {
    id: 5,
    question: "What's the best thing about Switzerland?",
    answer:
      "I don't know, but the flag is a big plus. Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas cupiditate laboriosam fugiat.",
  },
  // More questions...
];
const open = ref(false);
</script>
<style>

    .back {
        transform: rotateX(-180deg);
    }

    .front {
        transform: rotateX(0deg);
    }


    .display {
        max-height: 500px;
    }

    .text-display {
        opacity: 100;
    }

</style>