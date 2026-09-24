<!-- <template>
 <main>
 <h1>Selamat Datang di Onlineshop Sekolah</h1>
 <p>Belanja gampang, sekolah senang.</p>
 </main>
</template> -->
<!-- 
 -->
<template>
  <div class="font-sans bg-olive-950">
    <!-- HERO SECTION -->
    <section class="bg-linear-to-r from-red-700 via-black-500 to-orange-500
    bg-blue-50 px-2 py-10 text-center text-white rounded-xl justify-center">

      <h1 class="text-2xl font-extrabold ">𝔅𝔢𝔩𝔞𝔫𝔧𝔞𝔩𝔞𝔠 𝔰𝔢𝔰𝔲𝔞𝔦 𝔦𝔰𝔦 𝔡𝔬𝔪𝔭𝔢𝔱𝔪𝔲, 𝔧𝔞𝔫𝔤𝔞𝔫 𝔱𝔦𝔫𝔤𝔤𝔦𝔨𝔞𝔫 𝔢𝔤𝔬𝔪𝔲. </h1>
      <p class="text-xl">
   𝔇𝔞𝔯𝔦 𝔰𝔦𝔩𝔳𝔢𝔯 𝔧𝔢𝔴𝔢𝔩𝔯𝔶, 𝔢𝔶𝔢𝔴𝔢𝔞𝔯, 𝔞𝔭𝔭𝔞𝔯𝔢𝔩, 𝔩𝔢𝔞𝔱𝔠𝔢𝔯 𝔤𝔬𝔬𝔡𝔰, 𝔠𝔦𝔫𝔤𝔤𝔞 𝔠𝔬𝔪𝔢 
   𝔞𝔠𝔠𝔢𝔰𝔰𝔬𝔯𝔦𝔢𝔰—𝔱𝔢𝔪𝔲𝔭𝔞𝔫 𝔰𝔢𝔩𝔲𝔯𝔲𝔠 𝔢𝔨𝔬𝔰𝔦𝔰𝔱𝔢𝔪 ℭ𝔠𝔯𝔬𝔪𝔢 ℌ𝔢𝔞𝔯𝔱𝔰 𝔡𝔦 𝔰𝔞𝔱𝔲 𝔱𝔢𝔪𝔭𝔞𝔱. 
   𝔉𝔢𝔫𝔤𝔨𝔞𝔭, 𝔩𝔞𝔫𝔤𝔨𝔞, 𝔡𝔞𝔫 100% 𝔞𝔲𝔱𝔠𝔢𝔫𝔱𝔦𝔠.
      </p>
      <RouterLink to="/product" class="inlane-block bg-white
          decoration-2 font-semibold p-[<1436>] rounded-full shadow-xl/30 ">
        Lihat Produk
      </RouterLink>
    </section>
  </div>
    <section class="features">
      <div
      v-for="feature in features"
      :key="feature.title"
      class="feature-card"
    >
      <div class="feature-icon">{{ feature.icon }}</div>

      <h3 class="feature-title">
        {{ feature.title }}
      </h3>

      <p class="feature-desc">
        {{ feature.desc }}
      </p>

    </div>
  </section>
    <FeatureSection
  :features="[
    {
      icon: '🚀',
      title: 'Cepat & Praktis',
      desc: 'Proses pemesanan cepat tanpa ribet, cukup beberapa klik saja.'
    },
    {
      icon: '🔒',
      title: 'Aman & Terpercaya',
      desc: 'Transaksi terjamin keamanannya dengan sistem pembayaran terverifikasi.'
    },
    {
      icon: '💬',
      title: 'Dukungan 24/7',
      desc: 'Tim support siap membantu kapan pun kamu butuh bantuan.'
    }
  ]"
/>
    
</template>

<script setup>
import FeatureCard from '@/components/FeatureCard.vue';
</script>

<!-- <style scoped>
.landing-page {
  font-family: "Segoe UI", Arial, sans-serif;
  color: #1f1f2e;
}

/* ===== HERO ===== */
.hero {
  background: linear-gradient(135deg, #000000 0%, hsla(0, 1%, 25%, 0.582) 60%, #ec0101fd 100%);
  color: #ffffff;
  padding: 100px 24px;
  text-align: center;
  border-radius: 30px;
  justify-content: center;
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
  color: black;
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
</style> -->