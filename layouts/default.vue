<script setup lang="ts">
import Header from '~/components/layout/Header.vue';
</script>

<template>
    <div class="container-fluid-0">
      <Header/>
      <main>
        <slot />
      </main>
    </div>
  </template>
  

  