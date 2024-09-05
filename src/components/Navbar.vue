<template>
  <div class="sticky-sentinel" ref="sentinel"></div> <!-- 透明占位元素 -->
  <div ref="navbar" class="navbar bg-base-100 px-8 py-6 sticky top-10 z-50" :class="{ 'rounded-[100px] shadow-md': isSticky }">
    <div class="flex-1">
      <div class="btn btn-ghost btn-circle avatar border-none">
        <div class="w-12 rounded-full">
          <img src="../assets/image/avatar.jpg" alt="頭像" />
        </div>
      </div>
    </div>
    <div class="flex-none font-bold gap-2">
      <button @click="goHome"
        class="btn min-h-10 w-24 h-10 rounded-[100px] bg-white text-[#825514]  border-none shadow-none hover:bg-[#825514] hover:bg-opacity-[12%]"
        :class="{ '!bg-[#825514] !text-white': $route.path === '/' }">設計案例</button>
      <!-- <button @click="goAbout"
        class="btn min-h-10 w-20 h-10 rounded-[100px] bg-white text-[#825514] border-none shadow-none hover:bg-[#825514] hover:bg-opacity-[12%]"
        :class="{ '!bg-[#825514] !text-white': $route.path === '/About' }">關於我</button> -->
      <button @click="downloadpdf"
        class="btn min-h-10 w-[116px] h-10 rounded-[100px] bg-[#FFDDB9] border-none flex items-center hover:bg-[#E3C5A7]">
        <svg width="20" height="20" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path
            d="M8 11.575C7.86667 11.575 7.74167 11.554 7.625 11.512C7.50833 11.4707 7.4 11.4 7.3 11.3L3.7 7.7C3.51667 7.51667 3.425 7.28333 3.425 7C3.425 6.71667 3.51667 6.48333 3.7 6.3C3.88333 6.11667 4.12067 6.02067 4.412 6.012C4.704 6.004 4.94167 6.09167 5.125 6.275L7 8.15V1C7 0.716667 7.096 0.479 7.288 0.287C7.47933 0.0956668 7.71667 0 8 0C8.28333 0 8.521 0.0956668 8.713 0.287C8.90433 0.479 9 0.716667 9 1V8.15L10.875 6.275C11.0583 6.09167 11.296 6.004 11.588 6.012C11.8793 6.02067 12.1167 6.11667 12.3 6.3C12.4833 6.48333 12.575 6.71667 12.575 7C12.575 7.28333 12.4833 7.51667 12.3 7.7L8.7 11.3C8.6 11.4 8.49167 11.4707 8.375 11.512C8.25833 11.554 8.13333 11.575 8 11.575ZM2 16C1.45 16 0.979333 15.8043 0.588 15.413C0.196 15.021 0 14.55 0 14V12C0 11.7167 0.0956668 11.479 0.287 11.287C0.479 11.0957 0.716667 11 1 11C1.28333 11 1.521 11.0957 1.713 11.287C1.90433 11.479 2 11.7167 2 12V14H14V12C14 11.7167 14.096 11.479 14.288 11.287C14.4793 11.0957 14.7167 11 15 11C15.2833 11 15.5207 11.0957 15.712 11.287C15.904 11.479 16 11.7167 16 12V14C16 14.55 15.8043 15.021 15.413 15.413C15.021 15.8043 14.55 16 14 16H2Z"
            fill="#2B1700" />
        </svg>
        下載履歷
      </button>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue'
import { useRouter } from 'vue-router'
const router = useRouter()

//往設計案例
const goHome = () => {
  router.push('/')
}

//往關於我
const goAbout = () => {
  router.push('/About')
}

const downloadpdf = () => {
  const pdfUrl = 'https://drive.usercontent.google.com/u/0/uc?id=1fr7N2L0UB1Yhx28xANooatDU_r7CoGH8&export=download'; // PDF 文件的 URL
  const link = document.createElement('a'); // 創建一個隱藏的 <a> 標籤
  link.href = pdfUrl;
  link.setAttribute('download', 'Sylvia’s resume.pdf'); // 設置下載屬性，指定下載文件名
  document.body.appendChild(link);
  link.click(); // 模擬點擊以觸發下載
  document.body.removeChild(link); // 下載後移除標籤
}

const isSticky = ref(false) // 用來追蹤是否處於 sticky 狀態

const navbar = ref(null) // 取得 navbar 的 DOM 元素

const sentinel = ref(null); // 取得透明占位元素的 DOM 元素

onMounted(() => {
  const observerCallback = (entries) => {
    entries.forEach((entry) => {
      isSticky.value = !entry.isIntersecting; // 更新 isSticky 狀態
    });
  };

  // 設置 IntersectionObserver
  const observer = new IntersectionObserver(observerCallback, { threshold: [0] });

  // 開始觀察 navbar
  observer.observe(sentinel.value);

  // 銷毀時停止觀察
  onBeforeUnmount(() => {
    observer.disconnect();
  });
})
</script>

<style></style>