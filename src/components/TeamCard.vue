<script setup>
import { ref } from 'vue'

defineProps({
  nama: {
    type: String,
    required: true
  },
  jabatan: {
    type: String,
    required: true
  },
  foto: {
    type: String,
    default: ''
  },
  deskripsi: {
    type: String,
    default: 'Anggota tim yang berdedikasi untuk memberikan pelayanan terbaik.'
  }
})

// state lokal untuk tiap kartu, menyimpan apakah sedang "terbalik"
const terbalik = ref(false)

function toggleKartu() {
  terbalik.value = !terbalik.value
}
</script>

<template>
  <div class="flip-container" @click="toggleKartu">
    <div class="flip-inner" :class="{ 'is-flipped': terbalik }">
      
      <!-- SISI DEPAN -->
      <div class="flip-front">
        <div class="avatar">
          <img v-if="foto" :src="foto" :alt="nama" class="avatar-img" />
          <span v-else class="avatar-inisial">{{ nama.charAt(0) }}</span>
        </div>
        <h3 class="nama">{{ nama }}</h3>
        <p class="jabatan">{{ jabatan }}</p>
        <span class="hint">Klik untuk lihat detail</span>
      </div>

      <!-- SISI BELAKANG -->
      <div class="flip-back">
        <h3 class="nama-back">{{ nama }}</h3>
        <p class="deskripsi">{{ deskripsi }}</p>
        <span class="hint">Klik untuk kembali</span>
      </div>

    </div>
  </div>
</template>

<style scoped>
.flip-container {
  background-color: transparent;
  width: 100%;
  height: 220px;
  perspective: 1000px; /* memberi efek kedalaman 3D */
  cursor: pointer;
}

.flip-inner {
  position: relative;
  width: 100%;
  height: 100%;
  text-align: center;
  transition: transform 0.6s;
  transform-style: preserve-3d;
}

/* saat kartu diklik, putar 180 derajat */
.flip-inner.is-flipped {
  transform: rotateY(180deg);
}

.flip-front,
.flip-back {
  position: absolute;
  width: 100%;
  height: 100%;
  backface-visibility: hidden; /* sisi belakang tidak terlihat saat depan tampil */
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
  padding: 1.5rem;
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.flip-front {
  background-color: #fff;
}

.flip-back {
  background-color: #474747; /* samakan dengan warna brand */
  color: #fff;
  transform: rotateY(180deg); /* sisi belakang dibalik dari awal */
}

.avatar {
  width: 70px;
  height: 70px;
  border-radius: 50%;
  margin-bottom: 0.75rem;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color:#252525 ;
}

.avatar-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.avatar-inisial {
  font-size: 1.6rem;
  font-weight: bold;
  color: #fff;
}

.nama, .nama-back {
  margin: 0.25rem 0;
  font-size: 1.1rem;
}

.jabatan {
  margin: 0;
  color: #666;
  font-size: 0.9rem;
}

.deskripsi {
  font-size: 0.9rem;
  margin: 0.5rem 0;
}

.hint {
  margin-top: 0.75rem;
  font-size: 0.75rem;
  opacity: 0.7;
}
</style>