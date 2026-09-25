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
      <img src="/image/download%20(5).jpg" alt="Tentang Kami" />
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
  background: linear-gradient(rgb(155, 185, 232), rgb(46, 183, 218));
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
  flex-direction: column;
  align-items: center;
  text-align: center;
  gap: 0.5rem;
  margin-top: 1.2rem;
}

.text h2 {
  font-size: 1.5rem;
  margin-bottom: 1.2rem;
  font-weight: 600;
  color:rgb(7, 49, 86)
}

.text p {
  margin: 0;
  line-height: 1.6;
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