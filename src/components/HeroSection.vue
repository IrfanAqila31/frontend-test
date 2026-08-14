<script setup lang="ts"></script>

<template>
  <section id="home" class="pt-40 pb-20 bg-orange-50">
    <div class="max-w-7xl mx-auto px-4">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
        <div class="order-2 lg-order-1">
          <span class="text-slate-600 font-bold uppercase tracking-wider text-sm mb-4 block"
            >Pusat Terapi & Relaksasi</span
          >
          <h1 class="text-3xl md:text-5xl font-bold text-slate-900 mb-6 leading-tight">
            Pulihkan Keseimbangan Tubuh & Pikiran Anda
          </h1>
          <p class="text-slate-600 mb-5">
            Layanan terapi kesehatan profesional di Jakarta. Dipercaya lebih dari 2.400 klien sejak
            2015 dengan pendekatan holistic dengan ilmu pengetahuan.
          </p>

          <p class="text-slate-600">
            Metode kami dirancang khusus untuk mengatasi akar penyebab stres, ketegangan otot, dan
            ketidakseimbangan energi, bukan sekadar meredakan gejala.
          </p>
          <nav aria-label="Hero navigation" class="flex flex-wrap justify-center md:justify-start items-center gap-4 mt-10">
            <a
              href="#kontak"
              class="group flex text-sm md:text-base items-center justify-center px-5 md:px-7 py-3 bg-green-700 hover:bg-green-800 text-slate-50 font-medium cursor-pointer rounded-full transition duration-300"
            >
              Buat Janji Sekarang
            </a>
            <a
              href="#services"
              class="group flex text-sm md:text-base items-center justify-center px-5 md:px-7 py-3 bg-white border border-slate-300 hover:bg-green-800 hover:text-slate-50 text-slate-900 font-medium cursor-pointer rounded-full transition duration-300"
            >
              Lihat Layanan
            </a>
          </nav>
        </div>
        <div class="order-1 lg:order-2 rounded-2xl overflow-hidden shadow-2xl">
          <img
            src="https://i.pinimg.com/1200x/44/d5/67/44d567a88a54507e35957a2a06308e98.jpg"
            alt="Terapi Pijat"
            class="w-full h-full object-cover aspect-video lg:aspect-square"
          />
        </div>
      </div>
    </div>
  </section>
</template>
