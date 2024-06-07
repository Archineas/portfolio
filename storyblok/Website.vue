<template>
    <div
    v-editable="blok"
    class="text-center neon-shadow-img p-8 m-12 max-w-xl mx-auto items-center justify-center rounded-lg"
  >
    <a :href="blok.link.url" target="_blank" class="items-center justify-center p-2">
        <h2 class="text-2xl font-bold">
      {{ blok.title }}
      </h2>
      <p>{{ blok.description }}</p>
    </a>
  </div>
</template>
    
<script setup>
    import { getOptimizedImage } from '../composables/get-optimized-image';
    defineProps({ blok: Object });
</script>
  
<style>
  @keyframes rainbowShadow {
  0% {
    box-shadow: 0 0 10px 5px rgba(255, 0, 0, 0.7), 0 0 20px 4px rgba(255, 0, 0, 0.5); /* Red */
  }
  17% {
    box-shadow: 0 0 10px 5px rgba(255, 127, 0, 0.7), 0 0 20px 4px rgba(255, 127, 0, 0.5); /* Orange */
  }
  34% {
    box-shadow: 0 0 10px 5px rgba(255, 255, 0, 0.7), 0 0 20px 4px rgba(255, 255, 0, 0.5); /* Yellow */
  }
  51% {
    box-shadow: 0 0 10px 5px rgba(0, 255, 0, 0.7), 0 0 20px 4px rgba(0, 255, 0, 0.5); /* Green */
  }
  68% {
    box-shadow: 0 0 10px 5px rgba(0, 0, 255, 0.7), 0 0 20px 4px rgba(0, 0, 255, 0.5); /* Blue */
  }
  85% {
    box-shadow: 0 0 10px 5px rgba(75, 0, 130, 0.7), 0 0 20px 4px rgba(75, 0, 130, 0.5); /* Indigo */
  }
  100% {
    box-shadow: 0 0 10px 5px rgba(148, 0, 211, 0.7), 0 0 20px 4px rgba(148, 0, 211, 0.5); /* Violet */
  }
}

.neon-shadow-img {
    animation: rainbowShadow 5s infinite linear;
}

</style>