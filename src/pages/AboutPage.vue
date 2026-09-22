<!-- <template>
 <main>
 <h1>Tentang Kami</h1>
 <p>Onlineshop ini dikelola oleh siswa SMK Yadika Soreang jurusan
PPLG.</p>
 </main>
</template> -->
<script setup>
import TeamCard from '../components/TeamCard.vue'

const daftarTim = [
  { id: 1, nama: 'Jaymieuu', jabatan: 'Founder & Owner' },
  { id: 2, nama: 'Rubby Jhosep', jabatan: 'Kepala Produksi' },
  { id: 3, nama: 'Janee', jabatan: 'Customer Care' }
]
</script>

<template>
  <div class="about-page">
    <!-- Banner Tentang Kami -->
    <section class="banner">
      <h1>𝕿𝖊𝖓𝖙𝖆𝖓𝖌 𝕶𝖆𝖒𝖎</h1>
    </section>

    <!-- Bagian Cerita Kami -->
    <section class="cerita-kami container">
      <div class="cerita-teks">
        <h2>𝕮𝖊𝖗𝖎𝖙𝖆 𝕶𝖆𝖒𝖎</h2>
        <p>
     Berawal dari komunitas pecinta produk Chrome Hearts, kami hadir 
     memberikan layanan jasa titip (jastip) yang terpercaya. Berbekal 
     semangat untuk berbagi produk berkualitas dengan harga yang kompetitif,
     usaha yang bermula dari skala rumahan ini kini telah tumbuh menjadi toko pilihan 
     pelanggan setia. Setiap produk dipilah dan dipilih secara teliti untuk 
     memastikan Anda selalu mendapatkan yang terbaik.
        </p>
      </div>
      <div class="cerita-gambar">
        <img src="https://i.pinimg.com/1200x/65/ca/2f/65ca2fa1fded032dedaebd07db8e97c3.jpg" alt="Cerita kami" />
      </div>
    </section>

    <!-- Bagian Tim Kami -->
    <section class="tim-kami container">
      <h2>𝕿𝖎𝖒 𝕶𝖆𝖒𝖎</h2>
      <div class="grid-tim">
        <TeamCard
          v-for="anggota in daftarTim"
          :key="anggota.id"
          :nama="anggota.nama"
          :jabatan="anggota.jabatan"
        />
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
  background-color: #c90202; /* SESUAIKAN dengan warna Landing Page kalian */
  color: #fff;
  text-align: center;
  padding: 4rem 1rem;
  border-radius: 20px;
  box-shadow: 0 6px 13px rgba(0, 0, 0, 0.1);
}

.banner h1 {
  margin: 0;
  font-size: 2.2rem;
}

/* Layout 2 kolom Cerita Kami */
.cerita-kami {
  display: flex;
  align-items: center;
  gap: 2rem;
  flex-wrap: wrap; /* biar rapi kalau layar kecil */
}

.cerita-teks {
  flex: 1; /* kedua kolom berbagi lebar merata */
  min-width: 280px;
}

.cerita-gambar {
  flex: 1;
  min-width: 280px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  border-radius: 8px;
}

.cerita-gambar img {
  width: 100%;
  border-radius: 8px;
  display: block;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

/* Grid untuk kartu tim */
.grid-tim {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 1.5rem;
  margin-top: 1.5rem;
  box-shadow: 0 5px 12px rgba(0, 0, 0, 0.1);
  padding: 1.5rem;
}
</style>
