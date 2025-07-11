<script setup lang="ts">
import { cardItem } from '~/composables/dummy'
import CustomCard from './CustomCard.vue';
import arrowright from '~/assets/icons/arrowright.svg'
</script>

<template>
  <!-- Top right "Xem tất cả" outside the bordered container -->
  <div class="w-[1440px] px-20 m-auto flex justify-end mt-10">
    <span class="flex items-center gap-2 custom-text-black font-bold cursor-pointer">
      <p>Xem tất cả</p>
      <img :src="arrowright" alt="">
    </span>
  </div>

  <!-- Bordered Carousel container -->
  <div class="w-[1440px] overflow-hidden px-20 m-auto border-t-2 rounded-t-2xl border-amber-200 pt-5">
    <UCarousel 
      v-slot="{ item }"
      loop
      arrows
      dots
      :items="cardItem"
      :ui="{ item: 'basis-[calc(100%/4.5)] sm:basis-[calc(100%/4.5)]' }"
    >
      <CustomCard
        :img="item.img"
        :title="item.title"
        :name="item.name"
        :logo="item.logo"
        :topIcon="item.topIcon"
        :bottomIcon="item.bottomIcon"
      />
    </UCarousel>
  </div>
</template>

