<template>
  <div
    v-editable="blok"
    class="text-center neon-shadow-img p-8 m-12 max-w-xl mx-auto items-center justify-center rounded-lg"
  >
    <a :href="blok.link.url" target="_blank" class="flex items-center justify-center p-2">
      <img :src="getOptimizedImage(blok.image.filename, '300x0', 'webp')" alt="image" class="bg-white rounded-lg"/>
    </a>
      <h3 class="text-2xl font-bold">
      {{ blok.title }}
      </h3>
      <p>{{ blok.description }}</p>
  </div>
</template>
  
<script setup>
import { getOptimizedImage } from '../composables/get-optimized-image';
defineProps({ blok: Object });
</script>

<style>
.neon-shadow-img {
  box-shadow: 0 0 10px 5px rgba(255, 20, 147, 0.7), 0 0 20px 4px rgba(255, 20, 147, 0.5);
}
</style>