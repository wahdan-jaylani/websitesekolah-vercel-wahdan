<template>
    <div class="feature-card">
        <div class="feature-icon">{{ icon }}</div>
        <h3 class="feature-title">{{ title }}</h3>
        <p class="feature-desc">{{ desc }}</p>
        </div>
        </template>

        <script setup>
         defineProps({
            icon: String,
            title: String,
            desc: String
        })
    </script>