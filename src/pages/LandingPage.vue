<!-- <template>
 <main>
 <h1>Selamat Datang di Onlineshop Sekolah</h1>
 <p>Belanja gampang, sekolah senang.</p>
 </main>
</template> -->
<!-- 
 -->
<template>
  <div class="landing-page">
    <!-- HERO SECTION -->
    <section class="hero">
      <h1 class="hero-title">Belanja Lebih Cerdas, Hidup Lebih Mudah</h1>
      <p class="hero-subtitle">
        Temukan produk pilihan terbaik dengan harga terjangkau, langsung dari satu platform.
      </p>
      <RouterLink to="/product" class="hero-button">
        Lihat Produk
      </RouterLink>
    </section>

    <!-- FEATURE SECTION -->
    <section class="features">
      <div class="feature-card">
        <div class="feature-icon">🚀</div>
        <h3 class="feature-title">Cepat & Praktis</h3>
        <p class="feature-desc">
          Proses pemesanan cepat tanpa ribet, cukup beberapa klik saja.
        </p>
      </div>

      <div class="feature-card">
        <div class="feature-icon">🔒</div>
        <h3 class="feature-title">Aman & Terpercaya</h3>
        <p class="feature-desc">
          Transaksi terjamin keamanannya dengan sistem pembayaran terverifikasi.
        </p>
      </div>

      <div class="feature-card">
        <div class="feature-icon">💬</div>
        <h3 class="feature-title">Dukungan 24/7</h3>
        <p class="feature-desc">
          Tim support siap membantu kapan pun kamu butuh bantuan.
        </p>
      </div>
    </section>
  </div>
</template>

<script setup>
// Halaman ini murni presentational, belum butuh logic tambahan.
// Import RouterLink otomatis tersedia lewat komponen global Vue Router,
// jadi tidak perlu diimpor manual di sini.
</script>

<style scoped>
.landing-page {
  font-family: "Segoe UI", Arial, sans-serif;
  color: #1f1f2e;
}

/* ===== HERO ===== */
.hero {
  background: linear-gradient(135deg, #000000 0%, #3a04df17 60%, #d30000fd 100%);
  color: #ffffff;
  padding: 100px 24px;
  text-align: center;
  border-radius: 30px;
}

.hero-title {
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 16px;
}

.hero-subtitle {
  font-size: 1.1rem;
  max-width: 560px;
  margin: 0 auto 32px;
  opacity: 0.9;
}

.hero-button {
  display: inline-block;
  background: #ffffff;
  color: #db1821;
  text-decoration: none;
  font-weight: 600;
  padding: 14px 36px;
  border-radius: 999px;
  box-shadow: 0 6px 16px rgba(0, 0, 0, 0.2);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.hero-button:hover {
  transform: translateY(-4px);
  box-shadow: 0 10px 22px rgba(0, 0, 0, 0.28);
}

/* ===== FEATURES ===== */
.features {
  display: flex;
  gap: 24px;
  flex-wrap: wrap;
  justify-content: center;
  padding: 64px 24px;
  background: #f7f8fc;
}

.feature-card {
  background: #ffffff;
  border-radius: 16px;
  box-shadow: 0 4px 14px rgba(0, 0, 0, 0.08);
  padding: 32px 24px;
  width: 280px;
  text-align: center;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.feature-card:hover {
  transform: translateY(-6px);
  box-shadow: 0 10px 24px rgba(0, 0, 0, 0.12);
}

.feature-icon {
  font-size: 2rem;
  margin-bottom: 12px;
}

.feature-title {
  font-size: 1.15rem;
  font-weight: 600;
  margin-bottom: 8px;
}

.feature-desc {
  font-size: 0.95rem;
  color: #555566;
  line-height: 1.5;
}
</style>