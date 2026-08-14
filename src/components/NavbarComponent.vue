<script setup lang="ts">
import { ref } from 'vue'

const isMobileMenuOpen = ref(false)
</script>

<template>
  <header class="fixed top-3 left-0 w-full z-50 flex justify-center px-4">
    <nav
      aria-label="Navigasi Utama"
      class="bg-white border border-slate-200 backdrop-blur-sm rounded-full w-full max-w-7xl px-6 py-3 md:py-5 flex items-center justify-between"
    >
      <a href="#" class="text-lg md:text-xl font-bold text-slate-900" aria-label="Logo Mahreen"
        >Sehat Sejahtera</a
      >
      <div class="hidden lg:flex items-center space-x-8">
        <a
          href="#home"
          class="text-sm font-medium text-slate-700 hover:text-slate-900 transition-colors"
          >Beranda</a
        >
        <a
          href="#about"
          class="text-sm font-medium text-slate-700 hover:text-slate-900 transition-colors"
          >About</a
        >
        <a
          href="#services"
          class="text-sm font-medium text-slate-700 hover:text-slate-900 transition-colors"
          >Layanan</a
        >
        <a
          href="#testimoni"
          class="text-sm font-medium text-slate-700 hover:text-slate-900 transition-colors"
          >Testimoni</a
        >
        <a
          href="#kontak"
          class="text-sm font-medium text-slate-700 hover:text-slate-900 transition-colors"
          >Kontak</a
        >
      </div>
      <div class="hidden lg:block">
        <a
          href="#kontak"
          class="text-sm font-medium text-slate-50 px-5 py-3 bg-green-700 hover:bg-green-800 transition duration-300 rounded-full"
          >Hubungi Kami</a
        >
      </div>

      <button
        @click="isMobileMenuOpen = !isMobileMenuOpen"
        class="lg:hidden text-slate-900 hover:text-slate-950 focus:outline-none relative w-9 h-9 flex items-center justify-center"
        aria-label="Buka Menu Utama"
      >
        <Transition name="rotate-fade">
          <svg
            v-if="!isMobileMenuOpen"
            xmlns="http://www.w3.org/2000/svg"
            class="h-7 w-7 absolute"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M4 6h16M4 12h16M4 18h16"
            />
          </svg>
          <svg
            v-else
            xmlns="http://www.w3.org/2000/svg"
            class="h-7 w-7 absolute"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M6 18L18 6M6 6l12 12"
            />
          </svg>
        </Transition>
      </button>
    </nav>
    <transition name="slide-down">
      <div
        v-show="isMobileMenuOpen"
        class="absolute top-16 left-4 right-4 bg-white/80 backdrop-blur-sm rounded-2xl shadow-sm p-5 lg:hidden flex flex-col space-y-2"
      >
        <a
          @click="isMobileMenuOpen = false"
          href="#home"
          class="text-base font-medium text-slate-700 hover:text-slate-900 p-3 rounded-lg transition duration-300"
        >
          Beranda
        </a>
        <a
          @click="isMobileMenuOpen = false"
          href="#about"
          class="text-base font-medium text-slate-700 hover:text-slate-900 p-3 rounded-lg transition duration-300"
        >
          About
        </a>
        <a
          @click="isMobileMenuOpen = false"
          href="#services"
          class="text-base font-medium text-slate-700 hover:text-slate-900 p-3 rounded-lg transition duration-300"
        >
          Layanan
        </a>
        <a
          @click="isMobileMenuOpen = false"
          href="#testimoni"
          class="text-base font-medium text-slate-700 hover:text-slate-900 p-3 rounded-lg transition duration-300"
        >
          Testimoni
        </a>
        <a
          @click="isMobileMenuOpen = false"
          href="#kontak"
          class="text-base font-medium text-slate-700 hover:text-slate-900 p-3 rounded-lg transition duration-300"
        >
          Kontak
        </a>
        <div class="pt-5 border-t border-slate-100 flex">
          <a
            @click="isMobileMenuOpen = false"
            href="#kontak"
            class="text-sm font-medium text-slate-50 px-5 py-3 bg-green-700 hover:bg-green-800 transition duration-300 rounded-full"
            >Hubungi Kami</a
          >
        </div>
      </div>
    </transition>
  </header>
</template>

<style scoped>
/* Animasi Transisi Hamburger ke Tanda Silang */
.rotate-fade-enter-active,
.rotate-fade-leave-active {
  transition: all 0.3s ease-in-out;
}
.rotate-fade-enter-from {
  opacity: 0;
  transform: rotate(-90deg) scale(0.5);
}
.rotate-fade-leave-to {
  opacity: 0;
  transform: rotate(90deg) scale(0.5);
}

/* Animasi Dropdown Menu HP (Meluncur dari atas) */
.slide-down-enter-active,
.slide-down-leave-active {
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
}
.slide-down-enter-from,
.slide-down-leave-to {
  opacity: 0;
  transform: translateY(-20px) scaleY(0.95);
}
</style>
