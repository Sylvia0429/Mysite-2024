<template>
    <div class="content">
        <Navbar></Navbar>
        <RouterView />
    </div>
</template>

<script setup>
import { RouterView } from 'vue-router'
import Navbar from '@/components/Navbar.vue'
</script>

<style scoped>

</style>
