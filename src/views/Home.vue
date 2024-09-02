<template>
  <div>
    <!-- 標題介紹 -->
    <div class="py-20 flex flex-col justify-center borderBottom relative">
      <h2 class="text-[40px] font-bold">哈囉 ! 我是Sylvia👋</h2>
      <div class="my-6">
        <p class="text-2xl text-[#4C4136] mb-4">我是擁有13年設計領域經驗的設計師。</p>
        <p class="text-2xl text-[#4C4136]">我專注於<span class="bg-[#D7E9B8] rounded-lg p-3 mx-1">創造優質使用體驗</span>並<span
            class="bg-[#D7E9B8] rounded-lg p-3 mx-1">追求介面美感</span>，致力於將美學與功能性完美結合。</p>
      </div>
      <div class="font-bold mb-6">
        <button class="btn bg-[#825514] text-white w-24 hover:bg-[#825514] mr-4">關於我</button>
        <button class="btn bg-[#FFDDB9] w-[132px] border-none hover:bg-[#FFDDB9]">
          下載履歷
          <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path
              d="M8 11.575C7.86667 11.575 7.74167 11.554 7.625 11.512C7.50833 11.4707 7.4 11.4 7.3 11.3L3.7 7.7C3.51667 7.51667 3.425 7.28333 3.425 7C3.425 6.71667 3.51667 6.48333 3.7 6.3C3.88333 6.11667 4.12067 6.02067 4.412 6.012C4.704 6.004 4.94167 6.09167 5.125 6.275L7 8.15V1C7 0.716667 7.096 0.479 7.288 0.287C7.47933 0.0956668 7.71667 0 8 0C8.28333 0 8.521 0.0956668 8.713 0.287C8.90433 0.479 9 0.716667 9 1V8.15L10.875 6.275C11.0583 6.09167 11.296 6.004 11.588 6.012C11.8793 6.02067 12.1167 6.11667 12.3 6.3C12.4833 6.48333 12.575 6.71667 12.575 7C12.575 7.28333 12.4833 7.51667 12.3 7.7L8.7 11.3C8.6 11.4 8.49167 11.4707 8.375 11.512C8.25833 11.554 8.13333 11.575 8 11.575ZM2 16C1.45 16 0.979333 15.8043 0.588 15.413C0.196 15.021 0 14.55 0 14V12C0 11.7167 0.0956668 11.479 0.287 11.287C0.479 11.0957 0.716667 11 1 11C1.28333 11 1.521 11.0957 1.713 11.287C1.90433 11.479 2 11.7167 2 12V14H14V12C14 11.7167 14.096 11.479 14.288 11.287C14.4793 11.0957 14.7167 11 15 11C15.2833 11 15.5207 11.0957 15.712 11.287C15.904 11.479 16 11.7167 16 12V14C16 14.55 15.8043 15.021 15.413 15.413C15.021 15.8043 14.55 16 14 16H2Z"
              fill="#2B1700" />
          </svg>
        </button>
      </div>
      <p class="text-[#504539]">我熱愛學習與分享，並持續精進並回饋社群️‍️‍🌞️</p>
      <img class="w-[173px] h-[143px] absolute left-[-230px] top-[20px]" src="../assets/image/dot1.svg" alt="上點點">
      <img class="w-[173px] h-[143px] absolute right-[-160px] top-60" src="../assets/image/dot2.svg" alt="下點點">
    </div>
    <!-- 設計案例 -->
    <div class="py-20 flex flex-col items-center justify-center borderBottom">
      <p class="text-[32px] borderTitle mb-6">設計案例</p>
      <div class="my-6">
        <div>
          <div class="block border border-[#D4C4B5] rounded-lg designCase1">
            <img src="../assets/image/designCase1.svg" alt="設計案例1">
            <div class="card bg-base-100 w-96 shadow-xl designCase1Content">
              <div class="card-body">
                <h2 class="card-title">Card title!</h2>
                <p>If a dog chews shoes whose shoes does he choose?</p>
                <div class="card-actions justify-end">
                  <button class="btn btn-primary">Buy Now</button>
                </div>
              </div>
            </div>
          </div>
        </div>
        <a class="block border border-[#D4C4B5] rounded-lg"><img class="rounded-lg"
            src="../assets/image/designCase2.svg" alt="設計案例2"></a>
      </div>
      <a class="btn bg-[#825514] text-white w-[156px] hover:bg-[#825514]" target="_blank"
        href="https://www.behance.net/siyu_chen/projects">查看更多專案</a>
    </div>
    <!-- 互動  -->
    <div class="py-20 flex flex-col items-center justify-center borderBottom">
      <p class="text-[32px] borderTitle mb-6">互動/</p>
      <div class="my-6">
        <div class="grid grid-cols-2">
          <img src="../assets/image/screenityVideo.gif" alt="互動gif1">
          <img src="../assets/image/interactionGif2.gif" alt="互動gif2">
        </div>
        <div class="flex">
          <img class="w-[30%]" src="../assets/image/interactionGif3.gif" alt="互動gif3">
          <img class="w-[60%]" src="../assets/image/interactionGif4.gif" alt="互動gif4">
        </div>
      </div>
      <a class="btn bg-[#825514] text-white w-[192px] hover:bg-[#825514]" target="_blank"
        href="https://dribbble.com/Sylvia0429">查看更多設計作品</a>
    </div>
    <!-- 寫作文章 -->
    <div class="py-20 flex flex-col items-center justify-center borderBottom">
      <p class="text-[32px] borderTitle mb-6">寫作文章</p>
      <div class="grid grid-cols-3 gap-8 my-6">
        <a class="block" target="_blank" href="https://medium.com/@a0918109701/figma-animation-button-cfa5ebef4a5d">
          <div class="border border-[#D4C4B5] rounded-lg">
            <img class="rounded-lg" src="../assets/image/article1.svg" alt="寫作文章圖1">
          </div>
          <p class="text-xl font-bold mt-1">Figma五步驟輕鬆製作動畫按鈕</p>
        </a>
        <a class="block" target="_blank"
          href="https://medium.com/@a0918109701/%E4%BB%80%E9%BA%BC%E6%98%AF%E4%BD%BF%E7%94%A8%E8%80%85%E4%B8%AD%E5%BF%83%E8%A8%AD%E8%A8%88-%E5%A6%82%E4%BD%95%E8%AE%93%E4%BD%A0%E7%9A%84%E7%94%A2%E5%93%81%E7%9C%9F%E6%AD%A3%E7%82%BA%E4%BD%BF%E7%94%A8%E8%80%85%E6%9C%8D%E5%8B%99-1463ae0e9537">
          <div class="rounded-lg">
            <img class="rounded-lg" src="../assets/image/article2.svg" alt="寫作文章圖2">
          </div>
          <p class="text-xl font-bold mt-1">什麼是使用者中心設計？如何讓你的產品真正為使用者服務？</p>
        </a>
        <a class="block" target="_blank"
          href="https://medium.com/@a0918109701/%E4%BA%BA%E7%94%9F%E6%98%AF%E7%94%B1%E4%B8%80%E9%80%A3%E4%B8%B2%E7%9A%84%E9%9C%8E%E9%82%A3%E6%89%80%E7%B5%84%E6%88%90-%E8%A2%AB%E8%A8%8E%E5%8E%AD%E7%9A%84%E5%8B%87%E6%B0%A3-b691419ea8f6">
          <div class="border border-[#D4C4B5] rounded-lg">
            <img class="rounded-lg" src="../assets/image/article3.svg" alt="寫作文章圖3">
          </div>
          <p class="text-xl font-bold mt-1">人生是由一連串的霎那所組成–《被討厭的勇氣》</p>
        </a>
      </div>
      <a class="btn bg-[#825514] text-white w-[156px] hover:bg-[#825514]" target="_blank"
        href="https://medium.com/@a0918109701">查看更多文章</a>
    </div>
  </div>
</template>

<script setup>
</script>

<style>
.designCase1Content {
  display: none;
}

.designCase1:hover .designCase1Content {
  display: block;
  position: absolute;
  top: -45px;
  left: 0;
  color: #fff;
  font-size: .8em;
  background: #346e7a;
  padding: 5px;
  border-radius: 5px;
}
</style>
