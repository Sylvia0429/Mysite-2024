<template>
    <div class="content">
        <Navbar></Navbar>
        <RouterView />
        <Footer></Footer>
        <button @click="goTop"
            class="fixed bottom-5 right-10 z-50 bg-white border border-[#827568] rounded-[100px] p-2 hover:bg-[#EAE8E7]">
            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M4.35 18.35L12 10.7167L19.65 18.35L22 16L12 6L2 16L4.35 18.35Z" fill="#504539" />
            </svg>
        </button>
    </div>
</template>

<script setup>
import { watch } from 'vue'
import { RouterView, useRoute } from 'vue-router'
import Navbar from '@/components/Navbar.vue'
import Footer from './components/Footer.vue';


const route = useRoute()

const goTop = () => {
    window.scrollTo({
        top: 0, // 頁面頂部
        behavior: 'smooth' // 平滑滾動效果
    });
}

watch(() => route.path, () => {
    window.scrollTo({
        top: 0, // 頁面頂部
        behavior: 'smooth' // 平滑滾動效果
    });
})

</script>

<style scoped></style>
