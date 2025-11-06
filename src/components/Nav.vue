<template>
  <nav>
    <div class="w-full mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex items-center justify-between h-20">
        <div class="max-w-24">
          <img src="/logo.webp" alt="Logo" />
        </div>

        <div class="hidden md:flex items-center space-x-2 text-lg">
          <a href="#" class="px-4 py-2 text-gray-900">Home</a>
          <span class="text-orange-400 ">✷</span>
          <a href="#" class="px-4 py-2 text-gray-900">Features</a>
          <span class="text-orange-400">✷</span>
          <a href="#" class="px-4 py-2 text-gray-900">Contact Us</a>
        </div>

        <!-- Mobile menu button -->
        <button
          @click="toggleMenu"
          class="md:hidden p-2 rounded-md text-gray-900"
        >
          <svg
            class="h-6 w-6"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              v-if="!isMenuOpen"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M4 6h16M4 12h16M4 18h16"
            />
            <path
              v-else
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M6 18L18 6M6 6l12 12"
            />
          </svg>
        </button>
      </div>
    </div>

    <!-- Mobile menu -->
    <div
      v-if="isMenuOpen"
      class="md:hidden py-4 border-y-4 border-gray-200"
    >
      <a href="#" class="block px-4 py-3 text-gray-900 text-center">Home</a>
      <a href="#" class="block px-4 py-3 text-gray-900 text-center">Features</a>
      <a href="#" class="block px-4 py-3 text-gray-900 text-center">Contact Us</a>
    </div>
  </nav>
</template>

<script setup>
import { ref } from 'vue'

const isMenuOpen = ref(false)

function toggleMenu() {
  isMenuOpen.value = !isMenuOpen.value
}
</script>
