<template>
    <div
      v-editable="blok" class="text-center"
    >
    <h1 class="mb-4 text-4xl font-extrabold text-[#39ff14b3]">{{ blok.title }}</h1>
    <p>{{ blok.description }}</p>
    <div>
      <StoryblokComponent
      v-for="blok in blok.websites"
      :key="blok._uid"
      :blok="blok"
    />
    </div>

    </div>
  </template>
  
  <script setup>
  import { getOptimizedImage } from '../composables/get-optimized-image';
  
  defineProps({ blok: Object });
  </script>