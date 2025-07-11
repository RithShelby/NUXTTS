<script setup lang="ts">
defineProps<{
  img: string
  title: string
  name: string
  logo: string
  topIcon: string
  bottomIcon: string
}>()
</script>

<template>
  <div class="w-[280px] rounded-[15px] overflow-hidden shadow-md border border-amber-200 mr-4">
    <div class="relative h-[187px]">
      <img :src="img" :alt="title" class="w-full h-full object-cover" />
      <div class="absolute inset-0 bg-gradient-to-t from-black/70 via-black/30 to-transparent rounded-[15px]"></div>
      <img :src="topIcon" alt="Hot" class="absolute top-0 right-0 w-[40px]" />
      <img :src="bottomIcon" alt="Sport Icon" class="absolute bottom-[50px] left-2 w-[30px] z-10 animate-[spin_2s_linear_infinite]" />
      <div class="absolute bottom-0 left-0 right-0 px-1 py-0.5 bg-gradient-to-b from-yellow-200 to-amber-200 rounded-[20px] flex items-center justify-between z-0 shadow-lg">
        <div class="text-black text-center mx-auto leading-tight">
          <p class="text-sm font-medium">{{ title }}</p>
          <p class="text-base font-extrabold uppercase tracking-wide">{{ name }}</p>
        </div>
        <img :src="logo" alt="Live" class="w-[45px] ml-2" />
      </div>
    </div>
  </div>
</template>
