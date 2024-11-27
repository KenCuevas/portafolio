<template>
    <nav class="bg-gray-800 text-white">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex justify-between h-16 items-center">
          <!-- Logo -->
          <div class="flex items-center">
            <span class="text-xl font-bold">Kenny Cuevas</span>
          </div>
  
          <!-- Desktop Menu -->
          <div class="hidden md:flex space-x-4">
            <a href="#" class="hover:bg-gray-700 px-3 py-2 rounded-md">About</a>
            <a href="#" class="hover:bg-gray-700 px-3 py-2 rounded-md">Projects</a>
            <a href="#" class="hover:bg-gray-700 px-3 py-2 rounded-md">Contact</a>
          </div>
  
          <!-- Mobile Menu Button -->
          <div class="md:hidden">
            <button @click="toggleMenu" class="inline-flex items-center justify-center p-2 rounded-md focus:outline-none">
              <svg
                v-if="!menuOpen"
                xmlns="http://www.w3.org/2000/svg"
                class="h-6 w-6"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7" />
              </svg>
              <svg
                v-else
                xmlns="http://www.w3.org/2000/svg"
                class="h-6 w-6"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
              </svg>
            </button>
          </div>
        </div>
      </div>
  
      <!-- Mobile Menu -->
      <div v-if="menuOpen" class="md:hidden">
        <a href="#" class="block px-3 py-2 hover:bg-gray-700">About</a>
        <a href="#" class="block px-3 py-2 hover:bg-gray-700">Projects</a>
        <a href="#" class="block px-3 py-2 hover:bg-gray-700">Contact</a>
      </div>
    </nav>
  </template>
  
  <script>
  export default {
    data() {
      return {
        menuOpen: false,
      };
    },
    methods: {
      toggleMenu() {
        this.menuOpen = !this.menuOpen;
      },
    },
  };
  </script>
  
  <style scoped>
  </style>
  