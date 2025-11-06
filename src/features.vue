<script setup>

</script>

<template>
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

<style scoped>

</style>