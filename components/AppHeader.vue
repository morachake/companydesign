<script>
import { Button } from '@/components/ui/button'
import { ref } from 'vue'

export default {
  setup() {
    const isMenuOpen = ref(false)
    const toggleMenu = () => {
      isMenuOpen.value = !isMenuOpen.value
    }
    return {
      isMenuOpen,
      toggleMenu
    }
  }
}
</script>

<template>
  <div class="sticky top-0 flex w-full items-center h-20 bg-white justify-between px-6 sm:px-10 shadow-md z-50">
    <div>
      <h1 class="text-xl font-bold">Logo</h1>
    </div>
    <div class="sm:hidden">
      <button @click="toggleMenu" class="text-gray-700 focus:outline-none">
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path>
        </svg>
      </button>
    </div>
    <ul :class="{'flex': isMenuOpen, 'hidden': !isMenuOpen, 'sm:flex': true, 'flex-col sm:flex-row': true, 'space-y-2 sm:space-y-0 sm:space-x-6': true, 'text-gray-700 font-medium': true, 'absolute sm:static top-20 left-0 right-0 bg-white shadow-md sm:shadow-none z-40 p-4 sm:p-0': true}">
      <li class="hover:text-gray-900 cursor-pointer"><NuxtLink to="/about">About Us</NuxtLink></li>
      <li class="hover:text-gray-900 cursor-pointer"><NuxtLink to="/services">Services</NuxtLink></li>
      <li class="hover:text-gray-900 cursor-pointer"><NuxtLink to="/casestudies">Case Studies</NuxtLink></li>
      <li class="hover:text-gray-900 cursor-pointer"><NuxtLink to="/hireUs">Hire Us</NuxtLink></li>
    </ul>
    <div class="hidden sm:block">
      <Button class="text-white bg-[#161490] px-4 py-2 rounded hover:bg-blue-700">
        Contact Us
      </Button>
    </div>
  </div>
</template>
