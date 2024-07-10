<script setup>
import Card from '@/components/Card.vue'
import { RouterLink } from 'vue-router';
import experience from '@/experince.json'
import ExperinceCard from './ExperinceCard.vue';
import { ref } from 'vue';
const experienceData = ref(experience)
console.log('experience',experienceData)
</script>
<template>
     <section class="bg-green-100 py-4">
      <div class="container-xl lg:container m-auto">
        <p className="px-7 sm:text-[18px] text-[14px] text-secondary uppercase tracking-wider">What I have done so far</p>
        <h2 className="px-7 font-black md:text-[60px] sm:text-[50px] xs:text-[40px] text-[30px]">Work Experience</h2>
        <div className="grid grid-cols-1 md:grid-cols-3 gap-6">
          <ExperinceCard v-for="experience in experienceData" :key="experience.title" :experience="experience"/>

        </div>

      </div>
    </section>
</template>
