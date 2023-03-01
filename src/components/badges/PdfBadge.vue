<script setup>
defineProps({
  "pdfUrl": {
    type: String,
    required: true,
  }
})
</script>

<template>
  <a class="badge badge-pdf" v-if="pdfUrl" target="_blank" :href="pdfUrl">
    <i class="fa-solid fa-file" aria-hidden="true"></i>
    PDF
  </a>
</template>