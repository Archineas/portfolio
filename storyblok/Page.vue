<template>
  <!-- Die Nav über mein Config hat nicht funktioniert, das Plugin aus den Folien konnte ich nicht nehmen, da es lauter Fehler geworfen hat.
  Google wusste auch nicht weiter und ChatGPT auch nicht, daher jetzt halt so -->
  <div>
    <nav class="fixed top-0 left-0 right-0 bg-black neon-shadow z-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-center h-16">
        <div class="flex space-x-8">
          <a href="/about" class="border-transparent text-white hover:border-gray-300 hover:text-gray-300 inline-flex items-center px-1 pt-1 border-b-2 text-sm font-medium">
            About
          </a>
          <a href="/home" class="border-transparent text-white hover:border-gray-300 hover:text-gray-300 inline-flex items-center px-1 pt-1 border-b-2 text-sm font-medium">
            Home
          </a>
          <a href="/projects" class="border-transparent text-white hover:border-gray-300 hover:text-gray-300 inline-flex items-center px-1 pt-1 border-b-2 text-sm font-medium">
            Projects
          </a>
        </div>
      </div>
    </div>
  </nav>
  <div v-editable="blok" class="px-4">
    <StoryblokComponent v-for="blok in blok.body" :key="blok._uid" :blok="blok" />
  </div>
  </div>
</template>

<script setup>
defineProps({ blok: Object })
</script>

<style>
/* Plan war eigentlich mit den ganzen Frames im assets folder den Mauszeiger mit Nyan Cat zu animieren...geht leider nicht. */
html, body {
    cursor: url('https://tenor.com/de/view/nyan-cat-gif-9252182'), auto;
}

.neon-shadow {
      box-shadow: 0 4px 6px -1px rgba(57, 255, 20, 0.702), 0 2px 4px -2px rgba(57, 255, 20, 0.7);
}
</style>
