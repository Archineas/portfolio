<template>
  <div
    v-editable="blok"
    class="py-32 text-6xl font-bold text-center"
  >
    {{ blok.headline }}
  </div>
</template>

<script setup>
defineProps({ blok: Object })
</script>
