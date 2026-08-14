<script setup lang="ts">
import { ref } from 'vue'

const form = ref({
  name: '',
  phone: '',
  service: '',
  date: '',
})

const submitForm = () => {
  alert(
    `Terima kasih ${form.value.name}!\n\n` +
      `Permintaan jadwal Anda untuk layanan ${form.value.service} pada ${form.value.date} telah kami terima.\n` +
      `Tim kami akan segera menghubungi Anda melalui nomor WhatsApp ${form.value.phone}.`,
  )

  form.value = {
    name: '',
    phone: '',
    service: '',
    date: '',
  }
}
</script>

<template>
  <section id="kontak" class="py-24 bg-white" aria-labelledby="appointment-heading">
    <div class="container mx-auto max-w-3xl px-4">
      <header class="flex flex-col items-center justify-center text-center mb-16">
        <span
          class="text-slate-700 font-bold uppercase tracking-wider text-xs md:text-sm mb-2 block"
        >
          Reservasi
        </span>
        <h2
          id="appointment-heading"
          class="text-3xl md:text-4xl lg:text-5xl font-bold text-slate-900 mb-4"
        >
          Mulai Perjalanan Kesehatan Anda
        </h2>
        <p class="text-slate-600 max-w-xl font-light">
          Isi formulir singkat di bawah ini dan tim kami akan segera mengonfirmasi jadwal Anda.
        </p>
      </header>

      <form
        @submit.prevent="submitForm"
        class="bg-white p-6 md:p-10 rounded-3xl border border-slate-200 shadow-sm hover:shadow-md transition-shadow"
      >
        <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-8">
          <!-- Input Nama -->
          <div>
            <label for="name" class="block text-sm font-semibold text-slate-700 mb-2"
              >Nama Lengkap</label
            >
            <input
              type="text"
              id="name"
              v-model="form.name"
              placeholder="Masukkan nama Anda"
              class="w-full px-4 py-3 rounded-xl border border-slate-200 focus:outline-none focus:ring-2 focus:ring-green-600 transition-all text-slate-700"
              required
            />
          </div>

          <!-- Input WA -->
          <div>
            <label for="phone" class="block text-sm font-semibold text-slate-700 mb-2"
              >No. WhatsApp</label
            >
            <input
              type="tel"
              id="phone"
              v-model="form.phone"
              placeholder="Contoh: 08123456789"
              class="w-full px-4 py-3 rounded-xl border border-slate-200 focus:outline-none focus:ring-2 focus:ring-green-600 transition-all text-slate-700"
              required
            />
          </div>

          <!-- Input Pilihan Layanan -->
          <div>
            <label for="service" class="block text-sm font-semibold text-slate-700 mb-2"
              >Pilih Layanan</label
            >
            <select
              id="service"
              v-model="form.service"
              class="w-full px-4 py-3 rounded-xl border border-slate-200 focus:outline-none focus:ring-2 focus:ring-green-600 transition-all text-slate-700 bg-white"
              required
            >
              <option value="" disabled>Pilih salah satu...</option>
              <option value="Terapi Pijat Holistik">Terapi Pijat Holistik</option>
              <option value="Aromaterapi & Spa">Aromaterapi & Spa</option>
              <option value="Terapi Batu Panas">Terapi Batu Panas</option>
              <option value="Yoga Terapeutik">Yoga Terapeutik</option>
              <option value="Paket Detoks Premium">Paket Detoks Premium</option>
            </select>
          </div>

          <!-- Input Tanggal Kunjungan -->
          <div>
            <label for="date" class="block text-sm font-semibold text-slate-700 mb-2"
              >Rencana Tanggal</label
            >
            <input
              type="date"
              id="date"
              v-model="form.date"
              class="w-full px-4 py-3 rounded-xl border border-slate-200 focus:outline-none focus:ring-2 focus:ring-green-600 transition-all text-slate-700"
              required
            />
          </div>
        </div>

        <!-- Tombol Submit -->
        <button
          type="submit"
          class="w-full bg-green-700 hover:bg-green-800 text-white font-bold text-md py-4 rounded-xl shadow-sm transition-all duration-300"
        >
          Konfirmasi Janji Temu
        </button>
        
      </form>
    </div>
  </section>
</template>
