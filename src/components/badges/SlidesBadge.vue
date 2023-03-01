<script setup>
defineProps({
  "slidesUrl": {
    type: String,
    required: true,
  }
})
</script>

<template>
  <a class="badge badge-slides" v-if="slidesUrl" target="_blank" :href="slidesUrl">
    <i class="bi bi-file-slides-fill" aria-hidden="true"></i>
    Slides
  </a>
</template>