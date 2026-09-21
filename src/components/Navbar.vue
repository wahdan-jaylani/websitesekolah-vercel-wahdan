<template>
 <nav>
 <h2>𝕵𝖆𝖞𝖒𝖎𝖊𝖚𝖚𝖕- 𝕺𝖓𝖑𝖎𝖓𝖊𝖘𝖍𝖔𝖕</h2>
 <RouterLink to="/">𝕷𝖆𝖓𝖉𝖎𝖓𝖌</RouterLink> |
 <RouterLink to="/product">𝖅𝖗𝖔𝖉𝖚𝖈𝖙</RouterLink> |
 <RouterLink to="/about">𝕬𝖇𝖔𝖚𝖙</RouterLink> |
 <RouterLink to="/contact">𝕮𝖔𝖓𝖙𝖆𝖈𝖙</RouterLink>
 
 </nav>
 <hr /> 
</template>
<script setup>
 // JavaScript-nya di sini
</script>
<style scoped>
 .navbar {
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: nowrap;
    padding: 10px 20px;
    color: #dc2626;
    background-color: transparent;
    font-weight: bold;
} 
.navbar a.router-link-active,
.navbar a.router-link-exact-active {
background-color: transparent;
color:#dc2626;
font-weight: bold;
}
</style>
