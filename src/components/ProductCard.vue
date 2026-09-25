<script setup>
import { ref } from 'vue'

const props = defineProps({
  nama: String,
  harga: Number,
  gambar: String,
})

const gambarDipilih = ref(null)

function bukaPreview(src) {
  gambarDipilih.value = src
}

function tutupPreview() {
  gambarDipilih.value = null
}

function tambahKeKeranjang(nama) {
  const suara = new Audio('/audio/nikin-pop-up-something-160353 (2).mp3')
  suara.play()
  alert(`${nama} ditambahkan ke keranjang!`)
}
</script>

<template>
  <article class="product-card">
    <img :src="props.gambar" :alt="props.nama" @click="bukaPreview(props.gambar)" class="product-image" />
    <h3>{{ props.nama }}</h3>
    <p>Rp {{ props.harga.toLocaleString('id-ID') }}</p>
    <button @click="tambahKeKeranjang(props.nama)">Tambah ke Keranjang</button>
  </article>

  <div v-if="gambarDipilih" class="preview-overlay" @click="tutupPreview">
    <img :src="gambarDipilih" class="preview-image" />
  </div>
</template>

<style scoped>
.product-card {
  background: #fff;
  border-radius: 16px;
  box-shadow: 0 10px 25px rgba(15, 23, 42, 0.08);
  padding: 1rem;
  transition: transform 0.2s ease;
}

.product-card:hover {
  transform: translateY(-3px);
}

.product-image {
  width: 100%;
  height: 190px;
  object-fit: cover;
  border-radius: 12px;
  cursor: pointer;
}

.product-card h3 {
  margin-top: 0.75rem;
  font-size: 1.15rem;
  font-weight: 700;
  color: #1f2937;
}

.product-card p {
  margin: 0.35rem 0 0.75rem;
  color: #4b5563;
  font-weight: 600;
}

.product-card button {
  width: 100%;
  border: none;
  border-radius: 10px;
  background: linear-gradient(135deg, #2563eb, #3b82f6);
  color: white;
  font-weight: 600;
  padding: 0.75rem 1rem;
  cursor: pointer;
}

.preview-overlay {
  position: fixed;
  inset: 0;
  background: rgba(0, 0, 0, 0.7);
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 50;
  cursor: zoom-out;
}

.preview-image {
  max-width: 80%;
  max-height: 80%;
  border-radius: 12px;
}
</style>