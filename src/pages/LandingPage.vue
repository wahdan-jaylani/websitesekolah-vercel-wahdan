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
    <!-- HERO -->
    <section class="hero-section">
      <h1>Beli produk sesuai isi dompet mu</h1>
      <p>Platform sederhana untuk membeli CH, memberikan rekomendasi barang yang sesuai budgetmu.</p>
      <RouterLink to="/product" class="btn-primary">Lihat Produk</RouterLink>
    </section>

    <!-- FITUR -->
    <section class="features">
      <FeatureCard
        v-for="feature in features"
        :key="feature.title"
        :icon="feature.icon"
        :title="feature.title"
        :description="feature.desc"
      />
    </section>
  </div>
</template>
<script setup>
import FeatureCard from '@/components/FeatureCard.vue'

const features = [
  {
    icon: '🛒',
    title: 'Belanja Mudah',
    desc: 'Temukan berbagai produk sekolah dengan mudah dan cepat.'
  },
  {
    icon: '🚚',
    title: 'Pengiriman Cepat',
    desc: 'Dapatkan pesananmu dalam waktu singkat dengan layanan pengiriman kami.'
  },
  {
    icon: '💳',
    title: 'Pembayaran Aman',
    desc: 'Nikmati pengalaman belanja yang aman dengan berbagai metode pembayaran.'
  }
]


 <script setup>
import FeatureCard from '@/components/FeatureCard.vue'

const features = [
  {
    id: 1,
    icon: '🛒',
    title: 'Belanja Mudah',
    desc: 'Temukan berbagai produk sekolah dengan mudah dan cepat.'
  },
  {
    id: 2,
    icon: '🚚',
    title: 'Pengiriman Cepat',
    desc: 'Dapatkan pesananmu dalam waktu singkat dengan layanan pengiriman kami.'
  },
  {
    id: 3,
    icon: '💳',
    title: 'Pembayaran Aman',
    desc: 'Nikmati pengalaman belanja yang aman dengan berbagai metode pembayaran.'
  }
]
</script>
<style scoped>
.landing-page {
  font-family: 'Segoe UI', Arial, sans-serif;
  color: #2c2c57;
}

/* ===== HERO ===== */
.hero {
  background: linear-gradient(135deg, #000000 0%, #3a04df17 60%, #d30000fd 100%);
  color: #ffffff;
  padding: 100px 24px;
  text-align: center;
  border-radius: 20px;
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

.btn-primary {
  display: inline-block;
  background: #ffffff;
  color: #e70b3b;
  text-decoration: none;
  font-weight:bold;
  padding: 10px 24px;
  border-radius: 999px;
  box-shadow: 0 7px 17px rgba(0, 0, 0, 0.2);
  transition:transform 0.2s ease,
   
}

.btn-primary:hover {
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
  transition:
    transform 0.2s ease,
    box-shadow 0.2s ease;
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

video {
  margin-top: 40px;
  border-radius: 10px;
  max-width: 100%;
  margin-left: auto;
  margin-right: auto;
  display: block;
}
</style> 
