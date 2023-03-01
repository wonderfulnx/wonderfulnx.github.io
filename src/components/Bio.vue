<script setup>
import { ref, computed } from 'vue'
import { convertMarkdownToHtml } from '../utils'
import metaJson from '../content/meta.json'

const metaContent = ref(metaJson)
const description = computed(() => {
  return convertMarkdownToHtml(metaContent.value.description)
})
</script>

<template>
  <div class="row items-align-center">
    <div class="col-f4">
      <h1>{{ metaContent.name }}</h1>
      <div style="font-size: 13.5pt;" v-html="description"></div>
    </div>
    <div>
      <img class="col" src="../assets/personal-photo.jpg" width="160" alt="personal photo" style="margin: 20px 10px 0px 10px;">
    </div>
  </div>
  <div class="row flex-start">
    <div class="m-r1 m-tb-05" v-for="(contact, key) in metaContent.contact" :key="key">
      <i :class="contact.icon"></i>
      <a v-if="contact.url !== undefined" :href="contact.url" target="_blank">{{ key }}</a>
      <a v-if="contact.content !== undefined">{{ contact.content }}</a>
    </div>
  </div>
</template>