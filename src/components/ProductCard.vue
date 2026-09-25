<script setup>
import { ref } from 'vue'

const props = defineProps({
  nama: String,
  harga: Number,
  gambar: String,
})

const gambarDipilih = ref(null)
const suaraKlik = new Audio('/audio/notifikasi.mp3.mp3')

function putarSuara() {
  suaraKlik.currentTime = 0
  suaraKlik.play().catch(() => {})
}

function bukaPreview(src) {
  gambarDipilih.value = src
}

function tutupPreview() {
  gambarDipilih.value = null
}

function tambahKeKeranjang(nama) {
  putarSuara()
  alert(`${nama} ditambahkan ke keranjang!`)
}
</script>

<template>
  <article class="product-card">
    <img :src="props.gambar" :alt="props.nama" @click="bukaPreview(props.gambar)" class="product-image" />
    <h3>{{ props.nama }}</h3>
    <p>Rp {{ props.harga.toLocaleString('id-ID') }}</p>

    <div class="button-group">
      <button class="btn-primary" @click="tambahKeKeranjang(props.nama)">Tambah ke Keranjang</button>
    </div>
  </article>

  <div v-if="gambarDipilih" class="preview-overlay" @click="tutupPreview">
    <img :src="gambarDipilih" class="preview-image" />
  </div>
</template>

<style scoped>
.product-card {
  background: #ffffff;
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
  color: rgb(112, 15, 106);
}

.product-card p {
  margin: 0.35rem 0 0.75rem;
  color: rgb(112, 15, 106);
  font-weight: 600;
}

.button-group {
  display: flex;
  flex-direction: column;
  gap: 0.65rem;
}

.product-card button {
  width: 100%;
  border: none;
  border-radius: 10px;
  font-weight: 600;
  padding: 0.75rem 1rem;
  cursor: pointer;
}

.btn-primary {
  background: linear-gradient(135deg, #fecafe, #d8b4fe);
  color: #ffffff;
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
  max-width: 70%;
  max-height: 80%;
  border-radius: 12px;
}
</style>