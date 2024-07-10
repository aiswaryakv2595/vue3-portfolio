<script setup>
import logo from '@/assets/img/logo.svg'
import { RouterLink,useRoute } from 'vue-router';
const isActiveLink = (routePath) =>{
  const route = useRoute()
  return route.path ===routePath
}
</script>
<template>
    <nav class="sm:px-6 lg:px-6 w-full flex item-center py-1 fixed top-0 z-20 bg-black">
      <div class="w-full flex justify-between items-center max-w-7xl mx-auto">
        <RouterLink class="flex flex-shrink-0 items-center mr-4" to="/">
              <img class="h-10 w-auto" :src="logo" alt="Vue Jobs" />
              <span class="hidden md:block text-white text-2xl font-bold ml-2"
                >Aiswarya K V</span
              >
            </RouterLink>
        <div class="flex h-20 items-center justify-between">
          <div
            class="flex flex-1 items-center justify-center md:items-stretch md:justify-start"
          >
            <!-- Logo -->
         
            <div class="md:ml-auto">
              <div class="flex space-x-2">
                <RouterLink
                  to="/"
                  :class="[isActiveLink('/')?'bg-green-900':'hover:bg-gray-900 hover:text-white','text-white  hover:bg-green-900 hover:text-white rounded-md px-3 py-2']"
                  >
                  Home
                  </RouterLink>
                  <RouterLink
                  to="/about"
                  :class="[isActiveLink('/about')?'bg-green-900':'hover:bg-gray-900 hover:text-white','text-white  hover:bg-green-900 hover:text-white rounded-md px-3 py-2']"
                  >
                  About</RouterLink>
                  <RouterLink
                  to="/contact"
                  :class="[isActiveLink('/contact')?'bg-green-900':'hover:bg-gray-900 hover:text-white','text-white  hover:bg-green-900 hover:text-white rounded-md px-3 py-2']"
                  >
                  Contact Us</RouterLink>
              </div>
            </div>
          </div>
        </div>
      </div>
    </nav>
</template>