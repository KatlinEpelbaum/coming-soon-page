<template>
  <div class="min-h-screen bg-white px-4 py-8 md:px-8 lg:px-16">
    <div class="max-w-7xl mx-auto">
      <!-- Use flex + responsive direction -->
      <div class="flex flex-col lg:flex-row items-center justify-between gap-8 lg:gap-16 py-8 lg:py-10">
        
        <!-- Left text section -->
        <div class="flex-1 max-w-2xl text-left ">
          <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6">
            Stay tuned for something
            <span class="bg-purple-300 px-2">special.</span>
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

        <!-- Right image section -->
        <div class="flex-1 flex justify-center lg:justify-end">
          <img
            src="/hero.webp"
            alt="Hero image"
            class="w-full max-w-md lg:max-w-lg object-cover"
          />
        </div>
      </div>
    </div>
  </div>
</template>
