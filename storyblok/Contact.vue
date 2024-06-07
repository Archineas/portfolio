<template>
    <div
      v-editable="blok"
      class="py-32 text-6xl text-[#50b0ae] font-bold text-center flex items-center justify-center"
    >

    <a :href="blok.link.url" target="_blank" class="flex flex-col items-center justify-center neon-shadow-img p-4 rounded-lg">
    <img :src="getOptimizedImage(blok.logo.filename, '200x0', 'webp')" alt="image" class="rounded-lg bg-white"/>
    <h2 class="text-white">{{ blok.title }}</h2>
    </a>

    </div>
</template>
  
<script setup>
  const props = defineProps({ blok: Object })
  import { getOptimizedImage } from '../composables/get-optimized-image';
</script>

<style>
.neon-shadow-img {
  box-shadow: 0 0 10px 5px rgba(255, 20, 147, 0.7), 0 0 20px 4px rgba(255, 20, 147, 0.5);
}

</style>
  