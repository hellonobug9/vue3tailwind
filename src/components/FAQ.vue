<template>
    <div class="bg-gray-50 space-y-12">
        <FAQItem v-for="item in faqs" :key="item.id" :item="item" />
    </div>
</template>
<script setup>
import { Disclosure, DisclosureButton, DisclosurePanel } from '@headlessui/vue'
import { ChevronDownIcon } from '@heroicons/vue/24/outline'
import FAQItem from './FAQ-item.vue';
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
]

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