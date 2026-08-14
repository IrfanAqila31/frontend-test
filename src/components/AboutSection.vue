<script setup lang="ts">
// Data untuk kotak statistik (Bisa dengan mudah diedit di masa depan)
const statistics = [
  { value: '12', label: 'Terapis Ahli' },
  { value: '7+', label: 'Tahun Pengalaman' },
  { value: '6', label: 'Lokasi Cabang' },
]
</script>

<template>
  <section id="about" aria-label="about-heading" class="pt-10 lg:pt-30 pb-20 overflow-hidden bg-orange-50">
    <div class="max-w-7xl mx-auto px-4">
      <div class="grid grid-cols-1 md:grid-cols-2 gap-16 lg:gap-20 items-center">
        <!-- Kiri -->
        <figure class="relative group m-0 lg:ml-10 mb-8 lg:mt-0">
          <img
            src="https://i.pinimg.com/1200x/c3/ab/c9/c3abc9b12081d57bac30d478be1d3478.jpg"
            alt="Gedung perusahaan modern"
            class="relative rounded-2xl object-cover w-full h-110"
          />
          <figcaption
            class="absolute -bottom-10 left-5 lg:-left-10 bg-slate-50 p-5 rounded-xl shadow-[0_15px_40px_-10px_rgba(0,0,0,0.15)] max-w-60 animate-bounce-slow [animation-delay:-2.5s]"
          >
            <strong class="block text-2xl font-extrabold text-slate-900 mb-1">2.400+</strong>
            <span class="block text-sm font-bold text-slate-800 mb-2">Klien Terbantu</span>
            <span class="block text-xs text-slate-600">
              Telah mempercayakan pemulihan kesehatannya kepada kami sejak 2015.</span
            >
          </figcaption>
        </figure>
        <!-- Kanan -->
        <article class="flex flex-col">
          <header>
            <span class="text-slate-600 font-bold uppercase text-xs md:text-sm mb-3 block"
              >Tentang Kami</span
            >
            <h1 class="text-3xl md:text-4xl lg:text-5xl font-bold text-slate-900 mb-5">
              Pendekatan Holistic <br class="hidden lg:block" />Untuk Keseimbangan Tubuh & Pikiran
            </h1>
          </header>
          <p class="text-base text-slate-600 mb-8 leading-relaxed max-w-lg">
            Sehat Sejahtera didirikan pada 2015 dengan visi menghadirkan layanan kesehatan holistik
            berkualitas tinggi yang terjangkau bagi masyarakat Jakarta. Kami percaya bahwa kesehatan
            sejati mencakup keseimbangan fisik, mental, dan emosional. <br /><br />
            Tim kami terdiri dari 12 terapis dan praktisi kesehatas bersertifikat dengan rata-rata
            pengalaman 7 tahun. Setiap program terapi kami berbasis penelitian ilmiah dan
            disesuaikan dengan kebutuhan individual klien.
          </p>
          <div class="grid grid-cols-2 md:grid-cols-3 gap-4 mt-4">
            <div
              v-for="(stat, index) in statistics"
              :key="index"
              :class="[
                'p-4 border border-slate-200 rounded-2xl text-center bg-white hover:shadow-md transition-shadow',
                index === 2 ? 'col-span-2 md:col-span-1' : '',
              ]"
            >
              <strong class="block text-xl font-extrabold text-green-700 mb-1">
                {{ stat.value }}
              </strong>
              <span class="text-xs md:text-sm text-slate-600 font-normal">
                {{ stat.label }}
              </span>
            </div>
          </div>
        </article>
      </div>
    </div>
  </section>
</template>

<style scoped>
.animate-bounce-slow {
  will-change: transform;
  animation: float 3s ease-in-out infinite;
}

@keyframes float {
  0%,
  100% {
    transform: translate3d(0, 0, 0);
  }
  50% {
    transform: translate3d(0, -15px, 0);
  }
}
</style>
