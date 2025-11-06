<template>
  <nav id="home">
    <div class="w-full mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex items-center justify-between h-20">
        <div class="max-w-24 animate-fade-in-down">
          <img 
            src="/logo.webp" 
            alt="Logo" 
            class="transform transition-all duration-500 hover:scale-110 hover:rotate-3"
          />
        </div>

        <div class="hidden md:flex items-center space-x-2 text-lg">
          <a
            
            href="#home" 
            class="relative px-4 py-2 text-gray-900 transition-all duration-300 hover:text-[#FF9B71] hover:-translate-y-1 group animate-fade-in-down animation-delay-100"
          >
            Home
            <span class="absolute left-1/2 -bottom-1 w-0 h-0.5 bg-[#FF9B71] transition-all duration-300 group-hover:w-4/5 group-hover:left-1/2 group-hover:-translate-x-1/2"></span>
          </a>
          <span class="text-orange-400 animate-pulse animation-delay-200">✷</span>
          <a
            
            href="#features" 
            class="relative px-4 py-2 text-gray-900 transition-all duration-300 hover:text-[#FF9B71] hover:-translate-y-1 group animate-fade-in-down animation-delay-300"
          >
            Features
            <span class="absolute left-1/2 -bottom-1 w-0 h-0.5 bg-[#FF9B71] transition-all duration-300 group-hover:w-4/5 group-hover:left-1/2 group-hover:-translate-x-1/2"></span>
          </a>
          <span class="text-orange-400 animate-pulse animation-delay-400">✷</span>
          <a 
            href="#contact-us" 
            class="relative px-4 py-2 text-gray-900 transition-all duration-300 hover:text-[#FF9B71] hover:-translate-y-1 group animate-fade-in-down animation-delay-500"
          >
            Contact Us
            <span class="absolute left-1/2 -bottom-1 w-0 h-0.5 bg-[#FF9B71] transition-all duration-300 group-hover:w-4/5 group-hover:left-1/2 group-hover:-translate-x-1/2"></span>
          </a>
        </div>

        <!-- Mobile menu button -->
        <button
          @click="toggleMenu"
          class="md:hidden p-2 rounded-md text-gray-900 transition-all duration-300 hover:bg-gray-100 hover:scale-110 animate-fade-in-down animation-delay-600"
        >
          <svg
            class="h-6 w-6 transition-transform duration-300"
            :class="{'rotate-90': isMenuOpen}"
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
      class="md:hidden py-4 border-y-4 border-gray-200 animate-slide-in-down"
    >
      <a 
        href="#home" 
        class="block px-4 py-3 text-gray-900 text-center transition-all duration-300 hover:bg-gray-50 hover:text-[#FF9B71] hover:pl-8 animate-fade-in animation-delay-100"
      >
        Home
      </a>
      <a 
        href="#features" 
        class="block px-4 py-3 text-gray-900 text-center transition-all duration-300 hover:bg-gray-50 hover:text-[#FF9B71] hover:pl-8 animate-fade-in animation-delay-200"
      >
        Features
      </a>
      <a 
        href="#contact-us" 
        class="block px-4 py-3 text-gray-900 text-center transition-all duration-300 hover:bg-gray-50 hover:text-[#FF9B71] hover:pl-8 animate-fade-in animation-delay-300"
      >
        Contact Us
      </a>
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

<style scoped>
@keyframes fade-in-down {
  from {
    opacity: 0;
    transform: translateY(-20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes slide-in-down {
  from {
    opacity: 0;
    transform: translateY(-10px);
    max-height: 0;
  }
  to {
    opacity: 1;
    transform: translateY(0);
    max-height: 200px;
  }
}

@keyframes fade-in {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.animate-fade-in-down {
  animation: fade-in-down 0.6s ease-out forwards;
}

.animate-slide-in-down {
  animation: slide-in-down 0.4s ease-out forwards;
}

.animate-fade-in {
  animation: fade-in 0.5s ease-out forwards;
}

.animate-pulse {
  animation: pulse 2s infinite;
}

@keyframes pulse {
  0%, 100% {
    opacity: 1;
  }
  50% {
    opacity: 0.5;
  }
}

.animation-delay-100 {
  animation-delay: 0.1s;
  opacity: 0;
}

.animation-delay-200 {
  animation-delay: 0.2s;
  opacity: 0;
}

.animation-delay-300 {
  animation-delay: 0.3s;
  opacity: 0;
}

.animation-delay-400 {
  animation-delay: 0.4s;
  opacity: 0;
}

.animation-delay-500 {
  animation-delay: 0.5s;
  opacity: 0;
}

.animation-delay-600 {
  animation-delay: 0.6s;
  opacity: 0;
}
</style>