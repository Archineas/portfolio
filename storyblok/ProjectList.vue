<template>
    <div
      v-editable="blok"
    >
    <div>
      <StoryblokComponent
      v-for="blok in blok.project"
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