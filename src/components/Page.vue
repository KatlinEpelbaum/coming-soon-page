<template>
  <div class=" bg-white px-8 py-8 md:px-8 lg:px-16 ">
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
            class="bg-gray-800 hover:bg-gray-900 text-white px-8 py-3 rounded-md text-base font-medium transition-all duration-300 hover:scale-105 active:scale-95 hover:-translate-y-1 shadow-lg hover:shadow-xl">
            Contact us
        </button>
        </div>
        <div class="flex-1 flex justify-center lg:justify-end">
          <img src="/hero.webp" alt="Hero image" class="w-full max-w-md lg:max-w-sm object-cover" />
        </div>
      </div>
    </div>
  </div>
  <div class="lg:px-16  px-8 max-w-7xl mx-auto">
    <h1 class="font-bold text-4xl mb-16">What we offer</h1>

    <div
      class="grid grid-cols-1 md:grid-cols-3 *:hover:shadow-lg *:hover:shadow-amber-500/20 *:duration-300 *:transition-shadow *:ease-in *:delay-50 gap-4 mb-4">
      <div class="p-6 flex flex-col border rounded-xl gap-3 bg-white transition animate-fade-up">
        <div class="bg-[#FFDC9C]/41 w-12 h-12 flex items-center justify-center rounded-md">
          <img class="w-6 h-5 " src="/book.png" alt="">
        </div>
        <p class="font-semibold text-lg">Track Your Reads & Watches</p>
        <p class=" text-sm text-pretty">Keep a personal log of all the books you’ve read and movies you’ve watched.
          Never forget what you’ve enjoyed!</p>
      </div>

      <div
        class="p-6 flex flex-col border rounded-xl gap-3 bg-white transition md:col-span-2 animate-delay-100 animate-fade-up">
        <div class="bg-[#FFDC9C]/41 w-12 h-12 flex items-center justify-center rounded-md">
          <img class="w-6 h-5 " src="/gift.png" alt="">
        </div>
        <p class="font-semibold text-lg">Wishlist & Recommendations</p>
        <p class=" text-sm text-pretty">Create a wishlist of books and movies you want to explore, and get personalized
          recommendations based on your tastes.</p>
      </div>
    </div>

    <div
      class="grid grid-cols-1 md:grid-cols-5 gap-4 *:hover:shadow-lg *:hover:shadow-amber-500/20 *:duration-300 *:transition-shadow *:ease-in *:delay-5">
      <div
        class="p-6 flex flex-col border rounded-xl gap-3 bg-white  transition md:col-span-1 animate-delay-150 animate-fade-up">
        <div class="bg-[#FFDC9C]/41 w-12 h-12 flex items-center justify-center rounded-md">
          <img class="w-6 h-5 " src="/star.png" alt="">
        </div>
        <p class="font-semibold text-lg ">Rate & Review</p>
        <p class=" text-sm text-pretty">Give your favorite stories a rating and leave notes for yourself. Share your
          thoughts with friends if you want.</p>
      </div>

      <div
        class="p-6 flex flex-col border rounded-xl gap-3 bg-white  transition md:col-span-2 animate-delay-200 animate-fade-up">
        <div class="bg-[#FFDC9C]/41 w-12 h-12 flex items-center justify-center rounded-md">
          <img class="w-6 h-5 " src="/progress.png" alt="">
        </div>
        <p class="font-semibold text-lg">Progress Tracking</p>
        <p class=" text-sm text-pretty">Track your reading and viewing progress with stats, completion percentages, and
          streaks to stay motivated.</p>
      </div>


      <div
        class="p-6 flex flex-col border rounded-xl gap-3 bg-white transition md:col-span-2 animate-delay-250 animate-fade-up">
        <div class="bg-[#FFDC9C]/41 w-12 h-12 flex items-center justify-center rounded-md">
          <img class="w-6 h-5 " src="/search.png" alt="">
        </div>
        <p class="font-semibold text-lg">Search & Discover</p>
        <p class=" text-sm text-pretty">Easily search for new books or movies, browse trending titles, and discover
          hidden gems you might love.</p>
      </div>
    </div>



  </div>
  <div class="max-w-7xl mx-auto lg:pr-0 lg:pl-16 px-8  py-32 ">
    <div class="lg:flex gap-8 justify-center">
      <div class="mt-35 md:w-1/2">
        <h2 class="text-4xl font-bold mb-6">
          Any questions?
        </h2>
        <p class="text-lg">
          Ask us anything — we’d love to hear your thoughts<br />
          and answer your questions.
        </p>
      </div>

      <div class="bg-[#CAAEFF] rounded-l-xl w-full mt-24 lg:mt-0 py-20 p-5 md:w-1/2">
        <div class="bg-white p-6 rounded-lg border shadow-sm">
          <p class="text-lg mb-4">Contact us</p>

          <div class="block mb-3">
            <p class="text-sm">Email address</p>
            <input v-model="email" type="email" placeholder="example@example.com"
              class="mt-1 p-1 block w-full rounded-sm border border-gray-300 lg:w-3/4" />
          </div>

          <div class="block mb-4">
            <span class="text-sm">Message</span>
            <textarea v-model="message" placeholder="Write your message here"
              class="mt-1 p-1 block w-full rounded-md border border-gray-300 lg:w-3/4"></textarea>
          </div>

          <button @click="sendEmail" :disabled="isSending"
              class="bg-black text-white px-6 mt-4 py-2 rounded-lg hover:bg-gray-800 disabled:opacity-50 transition-all duration-300 hover:scale-105 active:scale-95 hover:-translate-y-1 shadow-lg hover:shadow-xl disabled:hover:scale-100 disabled:hover:translate-y-0">
              {{ isSending ? 'Sending... ✷' : 'Send' }}
          </button>

          <p v-if="statusMessage" class="mt-4 text-sm">{{ statusMessage }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
import emailjs from 'emailjs-com'

//Typewriter effect 
const words = ['special', 'fun', 'exciting', 'amazing', 'awesome']
const displayedText = ref('')
let wordIndex = 0
let charIndex = 0
let isDeleting = false
let timeoutId = null

const typeWriter = () => {
  try {
    const currentWord = words[wordIndex]

    if (isDeleting) {
      displayedText.value = currentWord.substring(0, charIndex - 1)
      charIndex--

      if (charIndex === 0) {
        isDeleting = false
        wordIndex = (wordIndex + 1) % words.length
        timeoutId = setTimeout(typeWriter, 500)
        return
      }
    } else {
      displayedText.value = currentWord.substring(0, charIndex + 1)
      charIndex++

      if (charIndex === currentWord.length) {
        isDeleting = true
        timeoutId = setTimeout(typeWriter, 2000)
        return
      }
    }

    timeoutId = setTimeout(typeWriter, isDeleting ? 50 : 100)
  } catch (error) {
    console.error('Typewriter error:', error)
  }
}

onMounted(() => {
  typeWriter()
})

onUnmounted(() => {
  if (timeoutId) clearTimeout(timeoutId)
})

//EmailJS
const email = ref('')
const message = ref('')
const isSending = ref(false)
const statusMessage = ref('')
const isValidEmail = (emailStr) => {
  const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/
  return emailRegex.test(emailStr)
}

const sendEmail = async () => {
  if (!email.value || !message.value) {
    statusMessage.value = 'Please fill out both fields.'
    return
  }

  if (!isValidEmail(email.value)) {
    statusMessage.value = 'Please enter a valid email address.'
    return
  }

  if (isSending.value) return

  isSending.value = true
  statusMessage.value = ''

  const serviceId = import.meta.env.VITE_EMAILJS_SERVICE_ID
  const templateId = import.meta.env.VITE_EMAILJS_TEMPLATE_ID
  const publicKey = import.meta.env.VITE_EMAILJS_PUBLIC_KEY

  if (!serviceId || !templateId || !publicKey) {
    console.error('Missing EmailJS environment variables')
    statusMessage.value = 'Configuration error. Please try again later.'
    isSending.value = false
    return
  }

  try {
    await emailjs.send(
      serviceId,
      templateId,
      {
        user_email: email.value,
        user_message: message.value
      },
      publicKey
    )

    statusMessage.value = '✅ Message sent successfully!'
    email.value = ''
    message.value = ''
  } catch (err) {
    console.error('EmailJS Error:', err)
    statusMessage.value = '❌ Failed to send message. Please try again later.'
  } finally {
    isSending.value = false
  }
}
</script>
>


<style scoped>
.cursor {
  animation: blink 1s infinite;
  margin-left: 1px;
}

@keyframes blink {

  0%,
  50% {
    opacity: 1;
  }

  51%,
  100% {
    opacity: 0;
  }
}
</style>
