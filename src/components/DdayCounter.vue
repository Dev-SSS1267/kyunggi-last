<template>
    <div class="flex flex-col items-center justify-center text-center text-white">
      <div class="text-3xl md:text-4xl font-bold mb-2">2025 수능 for 07</div>
      <div class="text-2xl md:text-3xl mt-2">D-{{ dDay2025 }}</div>
  
      <div class="text-3xl md:text-4xl font-bold mt-8 mb-2">2026 수능 for 08</div>
      <div class="text-2xl md:text-3xl mt-2">D-{{ dDay2026 }}</div>
    </div>
  </template>
  
  <script setup>
  import { ref, onMounted } from 'vue'
  
  // 목표 날짜 설정
  const targetDate2025 = new Date('2025-11-13') // 2025년 수능 날짜
  const targetDate2026 = new Date('2026-11-19') // 2026년 수능 날짜
  
  // 남은 날짜 계산 함수
  const calculateDday = (targetDate) => {
    const currentDate = new Date()
    const timeDiff = targetDate - currentDate
    return Math.ceil(timeDiff / (1000 * 60 * 60 * 24))
  }
  
  // D-day 상태값
  const dDay2025 = ref(calculateDday(targetDate2025))
  const dDay2026 = ref(calculateDday(targetDate2026))
  
  // 컴포넌트가 마운트되면 D-day 업데이트
  onMounted(() => {
    const updateCountdown = () => {
      dDay2025.value = calculateDday(targetDate2025)
      dDay2026.value = calculateDday(targetDate2026)
    }
    // 1초마다 D-day 업데이트
    setInterval(updateCountdown, 1000)
  })
  </script>
  
  <style>
  .text-4xl {
    font-size: 2.5rem;
  }
  .text-2xl {
    font-size: 1.5rem;
  }
  </style>
  