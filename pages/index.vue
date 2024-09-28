<script>
import {
  Popover,
  PopoverContent,
  PopoverTrigger,
} from '@/components/ui/popover'
import { Button } from '@/components/ui/button'
import ContactForm from '@/components/ContactForm'
</script>

<template>
  <image 
    src="/assets/images/bg.png"
    alt="Background image"
    class ="w-full h-auto"
  />
  <div class="h-screen flex flex-col md:flex-row items-center justify-around m-4 md:m-11 lg:px-20">
    <!-- Text Content -->
    <div class="flex flex-col justify-center text-center md:text-left">
      <h2 class="text-4xl sm:text-5xl font-light leading-tight">
        Great
        <span class="text-purple-500 font-semibold">Product</span>
        is
        <div>
          <span class="font-bold text-black">built by great</span>
          <span class="text-purple-500 font-bold">teams</span>
        </div>
      </h2>
      <h1 class="text-gray-500 mt-4 text-lg sm:text-xl max-w-md mx-auto md:mx-0">
        We help build and manage a team of world-class developers to bring your vision to life
      </h1>
      <div class="mt-8">
        <Popover>
          <PopoverTrigger>
            <Button class="bg-blue-600 text-white px-6 py-3 rounded-lg hover:bg-blue-700 transition duration-300">
              Let's get started!
            </Button>            
          </PopoverTrigger>
          <PopoverContent>
            <ContactForm />
          </PopoverContent>
        </Popover>
      </div>
    </div>

    <!-- Image Content -->
    <div class="w-full max-w-xl mt-10 md:mt-0">
      <img src="/assets/images/hero.png" alt="Hero image" class="w-full h-auto" />
    </div>
  </div>
</template>
