<script setup>
import { useRouter } from 'vue-router'

const router = useRouter()

function bukaProduk() {
  router.push('/product')
}
</script>

<template>
 
  <main class="landing-page">
    <h1>Wellcome To SMK Yadika Onlineshop </h1> 
    <button class="btn-grad" @click="bukaProduk">produk kami</button>
  </main>

  <main class="container">
  <main class="landing-page2">
    <h1>🪄</h1>
    <b>Kualitas Terjamin</b>
    <p>Bahan Berkualitas Premium!!</p>
    </main>

  <main class="landing-page2">
    <h1>💰</h1>
    <b>Harga Bersahabat</b>
   <p>Ramah Dikantong Gen z!</p>
  </main> 
 
  <main class="landing-page2">
    <h1>🚚</h1>
    <b>Pengiriman Cepat</b>
    <p>Diantar Langsung!!</p>
    </main>
    </main>

      <main>
    <video controls width="480" loop autoplay>
      <source src="/video/promo.toko.mp4.mp4" type="video/mp4" />
      Browser kamu tidak mendukung pemutaran video.
    </video>
    </main>
</template>

<style scoped>
.container{
  display: grid;
  grid-template-columns: repeat(3, minmax(180px, 1fr));
  gap: 1.5rem;
  justify-content: center;
  margin: 1.5rem auto 10px;
  width: min(100%, 900px);
}

.landing-page{
  padding: 2rem;
  text-align: center;
  background: linear-gradient(rgb(155, 185, 232), rgb(46, 183, 218));
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: auto;
}

.landing-page h1{
  font-size: 2.2rem;
  margin-bottom: 1rem;
  font-weight: 650;
  color: white;
}

.landing-page p{
  font-size: 1.2rem;
  margin-bottom: 2rem;
}
.landing-page2{
  background: linear-gradient(rgb(147, 180, 219), rgb(46, 183, 218));
  text-align: center;
  justify-content: center;
  padding: 20px;
  border-radius: 10px;
  flex-direction: column;
  display: flex;
  flex-wrap: wrap;
  width: 100%;
  min-height: 170px;
  margin-top: 35px;
  box-sizing: border-box;
  box-shadow: 20px 21px 23px rgba(12, 13, 14, 0.18);
}
.landing-page2 b,
.landing-page2 h1{
  font-size: 1.25rem;
  margin-bottom: 1rem;
  color: white;
}
.landing-page2 p{
  font-size: 0,1rem;
  color:rgb(7, 49, 86);
}
.bk{
  background-color:beige;
}

.btn-grad {
  background-image: linear-gradient(to right, #00d2ff 0%, #97cbf4 51%, #00d2ff 100%);
}

.btn-grad {
  margin: 10px;
  padding: 15px 45px;
  text-align: center;
  text-transform: uppercase;
  transition: 0.5s;
  background-size: 200% auto;
  color: white;
  box-shadow: 0 0 20px #eee;
  border-radius: 10px;
  display: block;
  outline: none;
  border: none;
}

.btn-grad:hover {
  background-position: right center;
  color: #fff;
  text-decoration: none;
}
video { 
  margin-top: 6rem;
  margin-left: 23rem;
  justify-content: center;
  border-radius: 10px; 
  display: block; 
}

</style>