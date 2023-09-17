<template>
  <div class="max-w-[700px] w-full mt-10 mb-16 mx-auto">
    <VueformUiKit />
  </div>
</template>

<script setup>
const title = ref('Vueform + Nuxt + Tailwind')
const description = ref('My App Description')

// This will be reactive even you change title/description above
useHead({
  title,
  meta: [{
    name: 'description',
    content: description
  }],
  script: [
    {
      src: 'https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&amp;libraries=places&amp;callback=initMaps',
      defer: true,
    },
    {
      src: '/initMaps.js',
    },
  ]
})
</script>