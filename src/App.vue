<template>
    <div class="content">
        <Navbar></Navbar>
        <RouterView />
        <Footer></Footer>
        <img @click="goTop" class="fixed bottom-5 right-10 z-50 bg-white" src="./assets/image/goTop.svg">
    </div>
</template>

<script setup>
import { RouterView } from 'vue-router'
import Navbar from '@/components/Navbar.vue'
import Footer from './components/Footer.vue';

const goTop = () => {
    window.scrollTo({
        top: 0, // 頁面頂部
        behavior: 'smooth' // 平滑滾動效果
    });
}

</script>

<style scoped></style>
