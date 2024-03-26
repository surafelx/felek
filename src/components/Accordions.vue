<template>
    <div class="accordion">
      <div
        v-for="(item, index) in items"
        :key="index"
        class="border-b border-gray-200"
      >
        <button
          @click="toggleAccordion(index)"
          class="flex justify-between items-center w-full py-2 px-4"
        >
          <span>{{ item.title }}</span>
          <svg
            class="w-4 h-4 transform"
            :class="{ 'rotate-180': activeIndex === index }"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
          >
            <path
              fill="currentColor"
              d="M19 13l-7 7-7-7"
            />
          </svg>
        </button>
        <div
          v-show="activeIndex === index"
          class="px-4 py-2"
        >
          <p>{{ item.content }}</p>
        </div>
      </div>
    </div>
  </template>
  
  <script lang="ts">
  import { defineComponent, ref } from 'vue';
  
  interface AccordionItem {
    title: string;
    content: string;
  }
  
  export default defineComponent({
    name: 'Accordion',
    props: {
      items: {
        type: Array as () => AccordionItem[],
        required: true
      }
    },
    setup(props) {
      const activeIndex = ref(-1);
  
      const toggleAccordion = (index: number) => {
        activeIndex.value = activeIndex.value === index ? -1 : index;
      };
  
      return {
        activeIndex,
        toggleAccordion
      };
    }
  });
  </script>
  
  <style scoped>
  .accordion .rotate-180 {
    transform: rotate(180deg);
  }
  </style>
  