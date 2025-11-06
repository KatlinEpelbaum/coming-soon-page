<template>
  <footer>
    <!-- Wave Divider -->
    <div class="w-full overflow-hidden leading-[0] rotate-180">
      <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none" class="relative block w-[calc(100%+1.3px)] h-[79px]">
        <path d="M321.39,56.44c58-10.79,114.16-30.13,172-41.86,82.39-16.72,168.19-17.73,250.45-.39C823.78,31,906.67,72,985.66,92.83c70.05,18.48,146.53,26.09,214.34,3V0H0V27.35A600.21,600.21,0,0,0,321.39,56.44Z" class="fill-[#FFDC9C]"></path>
      </svg>
    </div>
    <!-- Footer Content -->
    <div class="bg-[#FFDC9C] px-8 pt-8 pb-16 md:px-16 md:pt-0 md:pb-16">
      <div class="flex flex-col md:flex-row md:items-center md:justify-between gap-8">
        <!-- Brand Section -->
        <div class="flex flex-col space-y-3 md:w-1/3 animate-fade-in-up">
          <img
            src="/logo.webp"
            alt="Lune Logo"
            class="w-32 transform transition-transform duration-500 hover:scale-110 hover:rotate-3"
          >
          <p class="text-lg font-medium text-[#2D2D2D] animate-slide-in-left animation-delay-200">
            Join our lunatic<br class="hidden md:inline-block"> family <span class="inline-block animate-spin-slow">✷</span>
          </p>
          <p class="text-sm text-gray-600 mt-2 animate-fade-in animation-delay-400">
            © 2025 Lune. All rights reserved.
          </p>
        </div>
        <!-- Navigation Section -->
        <nav class="flex gap-12 flex-wrap md:w-2/3 md:justify-end animate-fade-in-up animation-delay-300">
          <a
            href="#home"
            class="relative text-base font-medium text-[#2D2D2D] transition-all duration-300 hover:text-[#FF9B71] hover:-translate-y-1 group"
          >
            Home
            <span class="absolute left-0 -bottom-1 w-0 h-0.5 bg-[#FF9B71] transition-all duration-300 group-hover:w-full"></span>
          </a>
          <a
            href="#features"
            class="relative text-base font-medium text-[#2D2D2D] transition-all duration-300 hover:text-[#FF9B71] hover:-translate-y-1 group"
          >
            Features
            <span class="absolute left-0 -bottom-1 w-0 h-0.5 bg-[#FF9B71] transition-all duration-300 group-hover:w-full"></span>
          </a>
          <a
            href="#contact"
            class="relative text-base font-medium text-[#2D2D2D] transition-all duration-300 hover:text-[#FF9B71] hover:-translate-y-1 group"
          >
            Contact us
            <span class="absolute left-0 -bottom-1 w-0 h-0.5 bg-[#FF9B71] transition-all duration-300 group-hover:w-full"></span>
          </a>
        </nav>
      </div>
    </div>
  </footer>
</template>
<style scoped>
@keyframes fade-in-up {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
@keyframes slide-in-left {
  from {
    opacity: 0;
    transform: translateX(-30px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
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
@keyframes spin-slow {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}
.animate-fade-in-up {
  animation: fade-in-up 0.8s ease-out forwards;
}
.animate-slide-in-left {
  animation: slide-in-left 0.8s ease-out forwards;
}
.animate-fade-in {
  animation: fade-in 0.8s ease-out forwards;
}
.animate-spin-slow {
  animation: spin-slow 4s linear infinite;
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
</style>