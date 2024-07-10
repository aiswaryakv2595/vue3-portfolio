<script setup>
import { defineProps } from 'vue';
import { RouterLink } from 'vue-router';
defineProps({
    title:{
        type:String,
        default:"Become a Vue Dev"
    },
    subtitle:{
        type:String,
        default:"Find the Vue job that fits your skills and needs"
    }
})
</script>
<template>
     <!-- Hero -->
     <section class="bg-green-100 pt-24 my-6 pb-20 mb-4">
      <div
        class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col items-center"
      >
        <div class="text-center">
          <h1
            class="text-4xl font-extrabold sm:text-5xl md:text-6xl"
          >
           {{ title }}
          </h1>
          <p class="my-4 text-xl ">
            {{ subtitle }}
          </p>
        </div>
        <div>

          <a href="https://github.com/aiswaryakv2595">
            
            <i class="pi pi-github"></i>
            github
          </a>
          
          <a href="https://github.com/aiswaryakv2595">
            
            <i class="pi pi-linkedin"></i>
            LinkedIn
          </a>
        </div>
       
      
      </div>
    </section>
</template>