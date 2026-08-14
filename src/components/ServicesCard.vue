<script setup lang="ts">
// Mendefinisikan Props yang akan diterima oleh komponen kartu ini
defineProps<{
  image: string
  duration: string
  price: string
  title: string
  desc: string
}>()
</script>

<template>
  <article class="group bg-white border border-slate-200 rounded-2xl overflow-hidden shadow-sm hover:shadow-md transition-all duration-300 flex flex-col">
    <figure class="relative h-56 overflow-hidden">
      <img 
        :src="image" 
        :alt="title" 
        class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500"
      />
    </figure>
    
    <div class="p-6 flex flex-col grow">
      <div class="flex items-center justify-between mb-4">
        <span class="text-green-700 bg-green-50 px-3 py-1 rounded-full text-xs font-bold tracking-wide">
          {{ duration }}
        </span>
        <span class="text-slate-900 font-bold text-lg">{{ price }}</span>
      </div>
      
      <h3 class="text-xl font-bold text-slate-900 mb-2">{{ title }}</h3>
      <p class="text-slate-600 mb-6 text-sm leading-relaxed grow">
        {{ desc }}
      </p>
      
    
      <a href="#kontak" class="inline-flex items-center text-green-700 font-bold text-sm group-hover:text-green-800 transition-colors">
        Pesan Sekarang 
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-4 h-4 ml-2 transform group-hover:translate-x-1 transition-transform">
          <path stroke-linecap="round" stroke-linejoin="round" d="M13.5 4.5 21 12m0 0-7.5 7.5M21 12H3" />
        </svg>
      </a>
    </div>
  </article>
</template>
