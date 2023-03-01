<script setup>
defineProps({
  "codeUrl": {
    type: String,
    required: true,
  }
})
</script>

<template>
  <a class="badge badge-code" v-if="codeUrl" target="_blank" :href="codeUrl">
    <i class="fa-solid fa-code" aria-hidden="true"></i>
    Code
  </a>
</template>