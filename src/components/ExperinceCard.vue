<script setup>
import { defineProps } from 'vue';
const props = defineProps({
    experience: Object
});
</script>

<template>
  <div class="bg-white rounded-xl shadow-md relative">
    <div class="p-4">
      <div class="mb-6">
        <div class="text-gray-600 text-[24px] font-bold">{{ experience.title }}</div>
        <h3 class="text-[16px] font-semibold">{{ experience.company_name }}</h3>
        <h6 class="text-[14px] font-medium">{{ experience.date }}</h6>
        <ul class="mt-5 list-disc ml-5 space-y-2">
          <li v-for="(point, index) in experience.points" :key="index">{{ point }}</li>
        </ul>
      </div>
    </div>
  </div>
</template>
