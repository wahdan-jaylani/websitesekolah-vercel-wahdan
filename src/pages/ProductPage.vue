 <script setup>
import ProductCard from '../components/ProductCard.vue'
const daftarProduk = [
 { id: 1, nama: ' Chrome Hearts  ', harga: 75000, gambar:
'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRLQkiNJgd_2Sgwy7hTm5ucUCXt8lqBYUHjj552n4L3Tw&s=10' },
 { id: 2, nama: 'Chrome Hearts Diamond Dagger Ring', harga:100000, gambar:
'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS4pIMphfKOzf6HxUgUA_6XhozpZYYNsKOVqZ5BvyUfFQ&s=10' },
 { id: 3, nama: 'Chrome Hearts Gold Ring with Gothic CH Detailing', harga: 540000, gambar:
'https://chromeheartsstoreus.com/wp-content/uploads/2026/05/chrome-hearts-gold-ring-1.webp' },
{ id: 3, nama: 'Chrome Hearts, Black & Grey Silver Cross Patch Jeans', harga: 5100000, gambar:
'https://shengliroadmarket.com/cdn/shop/files/chrome-hearts-black-grey-silver-cross-patch-jeans-7853076.jpg?v=1763710603&width=1080' },

]
</script>
<template>
 <main>
 <h1>𝕸𝖞 𝕻𝖗𝖔𝖉𝖚𝖈𝖙</h1>
 <div class="grid">
 <ProductCard
 v-for="produk in daftarProduk"
 :key="produk.id"
 :nama="produk.nama"
 :harga="produk.harga"
 :gambar="produk.gambar"
 />
 </div>
 </main>
</template>
<style scoped>
.grid {
 display: flex;
 gap: 10px;
 flex-wrap: wrap;
}
</style> 