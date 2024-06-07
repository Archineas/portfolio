<template>
    <div
      v-editable="blok"
      class="py-32 text-6xl text-[#50b0ae] font-bold text-center flex items-center justify-center"
    >
      <div>
        <img :src="getOptimizedImage(blok.image.filename, '800x0', 'webp')" alt="image" class="rounded-full neon-shadow-img"/>
      </div>
    </div>
    <div v-html="aboutContent" class="text-center neon-shadow-img max-w-xl mx-auto rounded-lg p-4"></div>
</template>
  
<script setup>
  const props = defineProps({ blok: Object })
  import { getOptimizedImage } from '../composables/get-optimized-image';
  import { computed } from "vue";
  import { renderRichText } from "@storyblok/vue";

  const aboutContent = computed(() => renderRichText(props.blok.text));
</script>

<style>
.neon-shadow-img {
  box-shadow: 0 0 10px 5px rgba(255, 20, 147, 0.7), 0 0 20px 4px rgba(255, 20, 147, 0.5);
}
h2 {
  font-size: 2rem;
  font-weight: 700;
  margin-top: 1rem;
  padding-top: 1rem;
}

p{
  padding-bottom: 1rem;
}
</style>
  