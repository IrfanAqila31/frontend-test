<script setup lang="ts">
// 1. Import komponen kartu yang baru dibuat
import ServicesCard from './ServicesCard.vue'

// 2. Data array layanan
const services = [
  {
    title: 'Terapi Pijat Holistik',
    duration: '60 Menit',
    price: 'Rp 250.000',
    desc: 'Kombinasi teknik pijat tradisional dan modern untuk meredakan ketegangan otot dan stres.',
    image: 'https://i.pinimg.com/736x/e4/66/40/e466405b85c7bc79b7a023472a000248.jpg',
  },
  {
    title: 'Aromaterapi & Spa',
    duration: '90 Menit',
    price: 'Rp 350.000',
    desc: 'Perawatan relaksasi menggunakan essential oil murni untuk menenangkan pikiran dan meremajakan kulit.',
    image: 'https://i.pinimg.com/1200x/01/a7/4c/01a74cbd2c55195b0e7ea4a9f033bf02.jpg',
  },
  {
    title: 'Akupunktur Terapan',
    duration: '45 Menit',
    price: 'Rp 300.000',
    desc: 'Terapi tusuk jarum profesional untuk melancarkan sirkulasi energi (Qi) dalam tubuh secara alami.',
    image: 'https://i.pinimg.com/1200x/a6/1b/02/a61b029dd0a87e01ae72c7f62d65552a.jpg',
  },
  {
    title: 'Terapi Batu Panas',
    duration: '90 Menit',
    price: 'Rp 400.000',
    desc: 'Penggunaan batu basal hangat untuk merilekskan otot yang tegang, melancarkan sirkulasi darah, dan meredakan stres.',
    image: 'https://i.pinimg.com/1200x/74/b7/77/74b7777636415d10fc5e71177646a696.jpg',
  },
  {
    title: 'Yoga Terapeutik',
    duration: '60 Menit',
    price: 'Rp 180.000',
    desc: 'Terapi yoga yang dirancang khusus untuk mengatasi masalah kesehatan fisik dan mental dengan pendekatan holistik.',
    image: 'https://i.pinimg.com/1200x/e2/a1/f2/e2a1f2118ca08b995d079d5f5bb0434d.jpg',
  },
  {
    title: 'Paket Detoks Premium',
    duration: '180 menit',
    price: 'Rp 750.000',
    desc: 'Program perawatan menyeluruh untuk membersihkan racun dalam tubuh, melancarkan sirkulasi limfatik, dan mengembalikan energi alami Anda.',
    image: 'https://i.pinimg.com/736x/2b/dc/74/2bdc74aef45d864a2890f189cd7417f7.jpg',
  },
]
</script>

<template>
  <section id="services" class="py-20 bg-white" aria-labelledby="services-heading">
    <div class="container mx-auto max-w-7xl px-4">
      <header class="flex flex-col items-center justify-center text-center mb-25">
        <span class="text-slate-700 font-bold uppercase text-xs md:text-sm mb-2 block"
          >Layanan Kami</span
        >
        <h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-slate-900 mb-3">
          Program Terapi & Wellness
        </h2>
        <p class="text-slate-900 font-light">
          Pilih program perawatan yang dirancang khusus untuk memulihkan keseimbangan fisik dan
          mental Anda.
        </p>
      </header>

      <!-- Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <ServicesCard v-for="(service, index) in services" :key="index" v-bind="service" />
      </div>
    </div>
  </section>
</template>
