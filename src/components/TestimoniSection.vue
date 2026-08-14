<script setup lang="ts">
// Array data testimoni klien
const testimonials = [
  {
    name: 'Sarah Amalia',
    role: 'Klien Terapi Pijat',
    quote:
      'Layanan terapi di sini sangat luar biasa. Tubuh saya terasa jauh lebih ringan dan nyeri punggung yang menahun hilang setelah sesi pertama!',
    image:
      'https://images.unsplash.com/photo-1438761681033-6461ffad8d80?ixlib=rb-4.0.3&auto=format&fit=crop&w=150&q=80',
    rating: 5,
  },
  {
    name: 'Budi Santoso',
    role: 'Klien Paket Detoks',
    quote:
      'Lingkungannya sangat menenangkan. Terapisnya profesional dan tahu persis apa yang tubuh saya butuhkan. Sangat direkomendasikan.',
    image:
      'https://images.unsplash.com/photo-1500648767791-00dcc994a43e?ixlib=rb-4.0.3&auto=format&fit=crop&w=150&q=80',
    rating: 5,
  },
  {
    name: 'Dina Lestari',
    role: 'Klien Yoga Terapeutik',
    quote:
      'Saya mengambil kelas yoga untuk pemulihan pasca cedera. Instrukturnya sangat sabar dan sekarang fleksibilitas saya sudah kembali normal.',
    image:
      'https://images.unsplash.com/photo-1494790108377-be9c29b29330?ixlib=rb-4.0.3&auto=format&fit=crop&w=150&q=80',
    rating: 5,
  },
]
</script>

<template>
  <section id="testimoni" class="py-24 bg-orange-50" aria-labelledby="testimonial-heading">
    <div class="container mx-auto max-w-7xl px-4">
      <header class="flex flex-col items-center justify-center text-center mb-16">
        <span class="text-slate-700 font-bold uppercase tracking-wider text-sm mb-2 block"
          >Kata Klien</span
        >
        <h2
          id="testimonial-heading"
          class="text-3xl md:text-4xl lg:text-5xl font-bold text-slate-900 mb-4"
        >
          Apa Kata Mereka?
        </h2>
        <p class="text-slate-600 max-w-2xl">
          Ratusan klien telah membuktikan manfaat dari terapi holistik kami. Berikut adalah
          pengalaman jujur mereka.
        </p>
      </header>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <article
          v-for="(testi, index) in testimonials"
          :key="index"
          class="bg-white p-8 rounded-3xl shadow-sm hover:shadow-md transition-shadow relative"
        >
          <div class="flex gap-1 mb-6 text-yellow-400">
            <svg
              v-for="n in testi.rating"
              :key="n"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 24 24"
              fill="currentColor"
              class="w-5 h-5"
            >
              <path
                fill-rule="evenodd"
                d="M10.788 3.21c.448-1.077 1.976-1.077 2.424 0l2.082 5.007 5.404.433c1.164.093 1.636 1.545.749 2.305l-4.117 3.527 1.257 5.273c.271 1.136-.964 2.033-1.96 1.425L12 18.354 7.373 21.18c-.996.608-2.231-.29-1.96-1.425l1.257-5.273-4.117-3.527c-.887-.76-.415-2.212.749-2.305l5.404-.433 2.082-5.006z"
                clip-rule="evenodd"
              />
            </svg>
          </div>

          <p class="text-slate-700 leading-relaxed mb-8 relative z-10 italic">
            "{{ testi.quote }}"
          </p>

          <div class="flex items-center gap-4 mt-auto">
            <img
              :src="testi.image"
              :alt="testi.name"
              class="w-12 h-12 rounded-full object-cover border-2 border-orange-100"
            />
            <div>
              <h4 class="font-bold text-slate-900">{{ testi.name }}</h4>
              <span class="text-xs text-slate-500">{{ testi.role }}</span>
            </div>
          </div>
        </article>
      </div>
    </div>
  </section>
</template>
