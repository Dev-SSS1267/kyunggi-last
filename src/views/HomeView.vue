<script setup>
import DdayCounter from '@/components/DdayCounter.vue'
</script>

<template>
  <div class="absolute inset-0 flex flex-col items-center justify-center z-20 text-center text-white space-y-6">
    <!-- 상단 문구 -->
    <div class="text-xl md:text-4xl font-semibold mb-[5rem]">
      believe in yourself, and your dreams will come true.
    </div>

    <!-- D-day 카운터 -->
    <DdayCounter />
  </div>
  <!-- 하단 로고 배치 -->
  <div class="z-20 absolute bottom-5 w-full flex flex-col md:flex-row items-center justify-center space-y-4 md:space-y-0 md:space-x-20 pb-4">
    <img src="https://cdn.lunaiz.com/kghs/kghs.svg" alt="경기고등학교" class="w-[7.5rem] md:w-[13rem]" />
    <img src="https://cdn.lunaiz.com/kghs/khbs.svg" alt="경기고등학교 방송부" class="w-[5rem] md:w-[7.5rem]" />
    <img src="https://cdn.lunaiz.com/lunaiz_logo/logo-d.svg" alt="lunaiz" class="w-[5rem] md:w-[7.5rem]" />
  </div>
</template>

<style>
/* 화면이 작을 때는 세로 배치, 화면이 클 때는 가로 배치를 적용하는 Tailwind CSS 설정 */
</style>
