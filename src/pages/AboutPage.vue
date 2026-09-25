<template>
  <main class="about-page">
    <h1>Tentang Kami</h1>
  </main>

  <div class="container">
    <section class="text">
      <h2>CERITA KAMI</h2>
      <p>Onlineshop ini dikelola langsung oleh siswa SMK Yadika Soreang jurusan PPLG.
      Sebagai proyek pelajar, sekaligus membantu siswa mendapatkan perlengkapan sekolah 
      dengan harga yang terjangkau.
      Selain itu, pengiriman dapat diantar dengan cepat.</p>
    </section>

    <section class="about-page3">
      <img src="/image/idk.webp" alt="Tentang Kami" />
    </section>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  align-items: center;
  gap: 2rem;
  margin-top: 1.5rem;
}

.about-page {
  padding: 2rem;
  text-align: center;
  background: linear-gradient(rgb(238, 148, 250), rgb(243, 184, 242));
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.about-page h1 {
  font-size: 2rem;
  margin-bottom: 0.75rem;
  font-weight: 650;
  color:rgb(240, 242, 244)
}

.text {
  flex: 1;
  display: flex;
  background: #fecafe;
  color: #ffffff;
  border-radius: 18px;
  padding: 1.5rem 1.25rem;
  flex-direction: column;
  align-items: center;
  text-align: center;
  gap: 0.5rem;
  margin-top: 1.1rem;
  box-shadow: 0 0 18px rgba(255, 255, 255, 0.9), 0 0 30px rgba(255, 255, 255, 0.55);
}

.text h2 {
  font-size: 1.5rem;
  margin-bottom: 1.1rem;
  font-weight: 900;
  color: rgb(112, 15, 106);
}

.text p {
  margin: 0;
  line-height: 1.6;
  color: #ffffff;
}

.about-page3 {
  width: 400px;
  height: 250px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 20px;
  overflow: hidden;
  background: transparent;
}

.about-page3 img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
  border-radius: 10px;
}
</style>