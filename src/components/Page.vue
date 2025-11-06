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
  <div class="px-10 py-16">
  <h1 class="font-bold text-3xl mb-10">What we offer</h1>

  <div class="grid grid-cols-1 md:grid-cols-3 gap-4 mb-4">
    <div class="p-6 flex flex-col border rounded-xl gap-3 bg-white transition">
      <div class="bg-[#FFDC9C]/41 w-12 h-12 flex items-center justify-center rounded-md">
        <img class="w-6 h-5 " src="/book.png" alt="">
      </div>
      <p class="font-semibold text-lg">Track Your Reads & Watches</p>
      <p class=" text-sm">Keep a personal log of all the books you’ve read and movies you’ve watched. Never forget what you’ve enjoyed!</p>
    </div>

    <div class="p-6 flex flex-col border rounded-xl gap-3 bg-white transition md:col-span-2">
      <div class="bg-[#FFDC9C]/41 w-12 h-12 flex items-center justify-center rounded-md">
        <img class="w-6 h-5 " src="/gift.png" alt="">
      </div>
      <p class="font-semibold text-lg">Wishlist & Recommendations</p>
      <p class=" text-sm">Create a wishlist of books and movies you want to explore, and get personalized recommendations based on your tastes.</p>
    </div>
  </div>

  <div class="grid grid-cols-1 md:grid-cols-5 gap-4">
    <div class="p-6 flex flex-col border rounded-xl gap-3 bg-white  transition md:col-span-1">
      <div class="bg-[#FFDC9C]/41 w-12 h-12 flex items-center justify-center rounded-md">
        <img class="w-6 h-5 " src="/star.png" alt="">
      </div>
      <p class="font-semibold text-lg ">Rate & Review</p>
      <p class=" text-sm">Give your favorite stories a rating and leave notes for yourself. Share your thoughts with friends if you want.</p>
    </div>

    <div class="p-6 flex flex-col border rounded-xl gap-3 bg-white  transition md:col-span-2">
      <div class="bg-[#FFDC9C]/41 w-12 h-12 flex items-center justify-center rounded-md">
        <img class="w-6 h-5 " src="/progress.png" alt="">
      </div>
      <p class="font-semibold text-lg">Progress Tracking</p>
      <p class=" text-sm">Track your reading and viewing progress with stats, completion percentages, and streaks to stay motivated.</p>
    </div>

    
    <div class="p-6 flex flex-col border rounded-xl gap-3 bg-white transition md:col-span-2">
      <div class="bg-[#FFDC9C]/41 w-12 h-12 flex items-center justify-center rounded-md">
        <img class="w-6 h-5 " src="/search.png" alt="">
      </div>
      <p class="font-semibold text-lg">Search & Discover</p>
      <p class=" text-sm">Easily search for new books or movies, browse trending titles, and discover hidden gems you might love.</p>
    </div>
  </div>

<!-- Email -->

  <div class="px-10 py-16 ">
    <div class="max-w-6xl grid grid-cols-1 md:grid-cols-2 gap-8 items-start">
      
      <div class="mt-35">
        <h2 class="text-3xl font-bold mb-4">Any questions?</h2>
        <p class="text-lg">Ask us anything — we’d love to hear your thoughts and answer your questions.</p>
      </div>
      <div class="bg-[#CAAEFF] py-20 p-5">
        <div class="bg-white p-6 rounded-lg border shadow-sm ">
          <p class="text-lg mb-4">Contact us</p>

          <div class="block mb-3">
            <p class="text-sm ">Email address</p>
            <input placeholder="example@example.com" class="mt-1 block w-full rounded-md border border-gray-300  "/>
          </div>

          <div class="block mb-4">
            <span class="text-sm">Message</span>
            <textarea placeholder="Write your message here" class="mt-1 block w-full rounded-md border border-gray-300 "></textarea>
          </div>

          <button class="bg-black text-white px-6 py-2 rounded-lg ">Send</button>
        </div>
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
