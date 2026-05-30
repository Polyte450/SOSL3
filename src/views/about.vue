<script setup>
import { ref, onMounted } from 'vue'

import img1 from '/src/assets/KCC.jfif'
import img2 from '/src/assets/Rwanda lake.jfif'
import img3 from '/src/assets/mountain.jfif'

const images = [img1, img2, img3]
const index = ref(0)

onMounted(() => {
  setInterval(() => {
    index.value = (index.value + 1) % images.length
  }, 2000)
})
</script>

<template>
<section class="relative">
  <img :src="images[index]" class="w-full h-screen object-cover" alt="Rwanda">

  <div class="absolute inset-0 bg-black/50 flex flex-col items-center justify-start pt-15">

    <h1 class="text-white text-5xl font-bold text-center">ABOUT RWANDA TOURISM</h1><br><br>

    <p class="text-2xl text-white text-center">Discover Rwanda’s beauty, culture and adventure</p><br><br>

    <!-- ROW 1 -->
    <div class="flex gap-6">
      <div class="bg-white/10 backdrop-blur-xl border border-white/20 p-5 rounded-2xl w-64 text-white text-sm text-center">
        Rwanda is known as the Land of a Thousand Hills with peaceful communities and rich culture.
      </div>

      <div class="bg-white/10 backdrop-blur-xl border border-white/20 p-5 rounded-2xl w-64 text-white text-sm text-center">
        Kigali is one of the cleanest cities in Africa with modern infrastructure and tourism attractions.
      </div>
    </div><br>

    <!-- ROW 2 -->
    <div class="flex gap-6">
      <div class="bg-white/10 backdrop-blur-xl border border-white/20 p-5 rounded-2xl w-64 text-white text-sm text-center">
        Wildlife includes gorillas, lions, elephants, giraffes and many rare species in national parks.
      </div>

      <div class="bg-white/10 backdrop-blur-xl border border-white/20 p-5 rounded-2xl w-64 text-white text-sm text-center">
        Rwanda has beautiful nature like mountains, lakes, forests and volcanoes across the country.
      </div>
    </div><br>

    <!-- CENTER BOX -->
    <div class="bg-white/10 backdrop-blur-xl border border-white/20 p-6 rounded-2xl w-80 text-white text-sm text-center">
      Top activities include gorilla trekking, safaris, hiking, boat rides on Lake Kivu and cultural tours.
    </div><br>

    <!-- BUTTON -->
    <button class="bg-green-700 px-6 py-3 rounded-lg text-white">
      FIND PLACES
    </button>

  </div>
</section>
</template>