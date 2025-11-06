<template>
  <div class="min-h-screen bg-white px-4 py-8 md:px-8 lg:px-16 ">
    <div class="max-w-7xl mx-auto">
      <div class="flex flex-col lg:flex-row items-center justify-between gap-8 lg:gap-16 py-8 lg:py-10">
        
        <div class="flex-1 max-w-2xl text-left ">
          <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6">
            Stay tuned for something
            <span class="bg-purple-300 px-2 inline-block">
              <span class="typewriter">{{ displayedText }}</span>
              <span class="cursor font-thin">|</span>
            </span>
          </h1>

          <p class="text-lg md:text-xl text-gray-700 mb-8 leading-relaxed">
            Discover, explore, and enjoy your favourite books, movies, and shows — all in one place.
          </p>

          <button
            class="bg-gray-800 hover:bg-gray-900 text-white px-8 py-3 rounded-md text-base font-medium transition-colors duration-200"
          >
            Contact us
          </button>
        </div>
        <div class="flex-1 flex justify-center lg:justify-end">
          <img
            src="/hero.webp"
            alt="Hero image"
            class="w-full max-w-md lg:max-w-sm object-cover"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const words = ['special', 'fun', 'exciting', 'amazing', 'awesome'];
const displayedText = ref('');
let wordIndex = 0;
let charIndex = 0;
let isDeleting = false;
let timeoutId = null;

const typeWriter = () => {
  const currentWord = words[wordIndex];
  
  if (isDeleting) {
    displayedText.value = currentWord.substring(0, charIndex - 1);
    charIndex--;
    
    if (charIndex === 0) {
      isDeleting = false;
      wordIndex = (wordIndex + 1) % words.length;
      timeoutId = setTimeout(typeWriter, 500);
      return;
    }
  } else {
    displayedText.value = currentWord.substring(0, charIndex + 1);
    charIndex++;
    
    if (charIndex === currentWord.length) {
      isDeleting = true;
      timeoutId = setTimeout(typeWriter, 2000);
      return;
    }
  }
  
  timeoutId = setTimeout(typeWriter, isDeleting ? 50 : 100);
};

onMounted(() => {
  typeWriter();
});

onUnmounted(() => {
  if (timeoutId) {
    clearTimeout(timeoutId);
  }
});
</script>

<style scoped>
.cursor {
  animation: blink 1s infinite;
  margin-left: 1px;
}

@keyframes blink {
  0%, 50% {
    opacity: 1;
  }
  51%, 100% {
    opacity: 0;
  }
}
</style>
