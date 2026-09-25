<script setup>
import ProductCard from '../components/ProductCard.vue'
 
const daftarProduk = [
  {
    id: 1,
    nama: 'Matstraw Latte',
    harga: 100000,
    gambar: '/image/download (5).jpg',
  },
  {
    id: 2,
    nama: 'Matstraw Cake',
    harga: 35000,
    gambar: '/image/download (6).jpg',
  },
  {
    id: 3,
    nama: 'Matcha Ice Tea',
    harga: 50000,
    gambar: '/image/IG_%20af_af9.jpg',
  },
]
</script>

<template>
  <main class="product-page">
    <h1>Produk Kami</h1>
    <div class="grid">
      <ProductCard
        v-for="produk in daftarProduk"
        :key="produk.id"
        :nama="produk.nama"
        :harga="produk.harga"
        :gambar="produk.gambar"
      />
    </div>
  </main>
</template>

<style scoped>
.product-page {
  padding: 2rem 0 3rem;
  background: #ffffff;
}

.product-page h1 {
  margin-bottom: 1rem;
  font-size: 2rem;
  font-weight: 700;
  color: rgb(112, 15, 106);
}

.grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(220px, 1fr));
  gap: 1rem;
  align-items: stretch;
  margin: 0 3rem;
  color: rgb(112, 15, 106);
}

@media (max-width: 768px) {
  .grid {
    grid-template-columns: 1fr;
    margin: 0 1rem;
  }
}
</style>