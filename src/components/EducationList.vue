<script setup>
import { computed } from 'vue'
import { convertMarkdownContentToHtml } from '../utils';

import eduJson from '../content/education.json'

const eduArr = computed(() => {
  return convertMarkdownContentToHtml(eduJson)
})
const idPrefix = "education"

</script>

<template>
  <h2>🎓 Education</h2>
  <div class="row items-align-top" v-for="(education, index) in eduArr" :key="index">
    <label class="col-quarter" :for="`${idPrefix}-${index}`" style="max-width: none; text-align: center;">{{ education.date }}</label>
    <label class="col-quarter" :for="`${idPrefix}-${index}`" style="max-width: none; text-align: center;">{{ education.role }}</label>
    <div class="col tight-list" :id="`${idPrefix}-${index}`" v-html="education.content"></div>
  </div>
</template>