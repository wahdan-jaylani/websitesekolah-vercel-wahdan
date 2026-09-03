<script setup>
// Form ini cukup tampilan saja, belum perlu logic submit
</script>

<template>
  <div class="contact-page">
    <!-- Banner -->
    <section class="banner">
      <h1>𝕳𝖚𝖇𝖚𝖓𝖌𝖎 𝕶𝖆𝖒𝖎</h1>
    </section>

    <section class="contact-content container">
      <!-- Kolom Info Kontak -->
      <div class="info-kontak">
        <h2>Info Kontak</h2>
        <p class="deskripsi">
          Ada pertanyaan seputar produk atau pesanan? Hubungi kami lewat
          kontak di bawah ini.
        </p>

        <div class="item-kontak">
          <span class="ikon">📍</span>
          <div>
            <strong>Alamat</strong>
            <p>Jl. Merdeka No. 45, Bandung, Jawa Barat</p>
          </div>
        </div>

        <div class="item-kontak">
          <span class="ikon">📞</span>
          <div>
            <strong>Telepon</strong>
            <p>+62 812 3456 7890</p>
          </div>
        </div>

        <div class="item-kontak">
          <span class="ikon">✉️</span>
          <div>
            <strong>Email</strong>
            <p>halo@tokokami.id</p>
          </div>
        </div>

        <div class="item-kontak">
          <span class="ikon">🕒</span>
          <div>
            <strong>Jam Operasional</strong>
            <p>Senin - Sabtu, 09.00 - 20.00 WIB</p>
          </div>
        </div>
      </div>

      <!-- Kolom Formulir -->
      <div class="form-card">
        <h2>Kirim Pesan</h2>
        <form class="form-kontak">
          <label for="nama">Nama</label>
          <input type="text" id="nama" placeholder="Masukkan nama kamu" />

          <label for="email">Email</label>
          <input type="email" id="email" placeholder="nama@email.com" />

          <label for="pesan">Pesan</label>
          <textarea id="pesan" rows="5" placeholder="Tulis pesan kamu di sini..."></textarea>

          <button type="button">Kirim ✈️</button>
        </form>
      </div>
    </section>
  </div>
</template>

<style scoped>
.container {
  max-width: 1000px;
  margin: 0 auto;
  padding: 3rem 1.5rem;
}

.banner {
  background-color: #e70b3b;
  color: #fff;
  text-align: center;
  padding: 4rem 1rem;
  border-radius: 20px;
}

.banner h1 {
  margin: 0;
  font-size: 2.2rem;
}

/* Layout 2 kolom sejajar */
.contact-content {
  display: flex;
  gap: 2.5rem;
  flex-wrap: wrap;
}

.info-kontak {
  flex: 1;
  min-width: 280px;
}

.deskripsi {
  color: #666;
  margin-bottom: 1.5rem;
}

.item-kontak {
  display: flex;
  align-items: flex-start;
  gap: 0.75rem;
  margin-bottom: 1.25rem;
}

.item-kontak .ikon {
  font-size: 1.4rem;
}

.item-kontak strong {
  display: block;
  margin-bottom: 0.15rem;
}

.item-kontak p {
  margin: 0;
  color: #555;
  font-size: 0.9rem;
}

/* Kartu Formulir */
.form-card {
  flex: 1;
  min-width: 280px;
  background-color: #fff;
  padding: 2rem;
  border-radius: 16px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.08);
}

.form-kontak {
  display: flex;
  flex-direction: column;
}

.form-kontak label {
  font-size: 0.85rem;
  font-weight: 600;
  margin-bottom: 0.35rem;
  margin-top: 1rem;
}

.form-kontak input,
.form-kontak textarea {
  padding: 0.75rem 1rem;
  border-radius: 10px;
  border: 1px solid #ddd;
  font-family: inherit;
  font-size: 0.95rem;
  outline: none;
  resize: vertical;
  transition: border-color 0.2s;
}

.form-kontak input:focus,
.form-kontak textarea:focus {
  border-color:  #e70b3b;
}

.form-kontak button {
  margin-top: 1.5rem;
  background:  #474747;
  color: #fff;
  border: none;
  padding: 0.8rem 1.5rem;
  border-radius: 999px; /* bentuk pil, senada tombol Landing Page */
  font-size: 1rem;
  font-weight: 600;
  cursor: pointer;
  align-self: flex-start;
  transition: background 0.2s, transform 0.15s;
}

.form-kontak button:hover {
  background: #e70b3b;
  transform: translateY(-1px);
}
</style> -->