<template>
  <div
    v-editable="blok"
    class="w-full p-12 bg-[#f7f6fd] rounded-[5px] text-center"
  >
    <h3 class="text-2xl text-[#1d243d] font-bold">
      {{ blok.title }}
    </h3>
    <img :src="getOptimizedImage(blok.image.filename, '800x0', 'webp')" alt="image" />
  </div>
</template>

<script setup>
import { getOptimizedImage } from '../composables/get-optimized-image';

defineProps({ blok: Object });
</script>
