<template>
    <main class="contact-page">
      <h1>Hubungi Kami</h1>
    </main>

    <main class="container">
    <main class="text">
      <h1> Info Kontak</h1>
      <h3>📍Alamat</h3>
      <p> jl. smk yadika soreang</p>
      <h3>📞Telepon</h3>
      <p>081234567810</p>
      <h3>📧Email</h3>
      <p>info@webyadika.com</p>
    </main>

    <main class="formulir">
      <h1>Kirim Pesan</h1>
      <p>Nama</p>
      <input type="text" placeholder="Nama Kamu" />
      <p>Email</p>
      <input type="email" placeholder="Email" />
      <p>Pesan</p>
      <textarea placeholder="Pesan"></textarea>
      <button class="btn-grad">Kirim</button>
    </main>
    </main>
  
  </template>
  <style scoped>
  .container {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    align-items: start;
    justify-content: center;
    gap: 1rem;
    width: 95%;
  } 

  .text h1 {
    font-size: 2rem;
    margin-top: 2rem;
    margin-left: 2.3rem;
    font-weight: 650;
    color:rgb(7, 49, 86);
  }

  .text h3,
  .text p {
    font-size: 1.2rem;
    margin-left: 2.3rem;
    font-weight: 600;
    color:rgb(7, 49, 86);
  }

  .contact-page {
  padding: 2rem;
  text-align: center;
  background: linear-gradient(rgb(155, 185, 232), rgb(46, 183, 218));
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
  }

  .contact-page h1 {
    font-size: 2rem;
    margin-bottom: 0.75rem;
    font-weight: 650;
    color:rgb(240, 242, 244)
  }

  .formulir {
    display: flex;
    flex: 1;
    flex-direction: column;
    gap: 0.35rem;
    width: min(100%, 420px);
    margin: 3rem 0rem 2rem;
    padding: 1rem;
    border: 1px solid rgba(135, 157, 245, 0.45);
    border-radius: 16px;
    background: linear-gradient(rgb(180, 210, 247), rgb(157, 229, 247));
    box-shadow: 0 9px 21px rgba(6, 13, 18, 0.18);
    box-sizing: border-box;
  }

  .formulir h1 {
    margin: 0 0 0.5rem;
    text-align: center;
    font-size: 1.5rem;
    font-weight: 600;
    color:rgb(253, 254, 255);
  }

  .formulir p {
    margin: 0.35rem 0 0;
    color:rgb(7, 49, 86);
  }

  .formulir input,
  .formulir textarea {
    width: 97%;
    padding: 0.3rem;
    border: 1px solid rgba(6, 10, 21, 0.45);
    border-radius: 5px;
  }

  .btn-grad {
  background-image: linear-gradient(to right, #00d2ff 0%, #97cbf4 51%, #00d2ff 100%);
}

.btn-grad {
  margin: 10px;
  padding: 15px 15px;
  text-align: center;
  text-transform: uppercase;
  transition: 0.5s;
  background-size: 150% auto;
  color: rgb(32, 16, 122);
  box-shadow: 0 0 20px #2b1270;
  border-radius: 999px;
  display: block;
  outline: none;
  border: none;
}

.btn-grad:hover {
  background-position: right center;
  color: #fff;
  text-decoration: none;
}
</style>
  