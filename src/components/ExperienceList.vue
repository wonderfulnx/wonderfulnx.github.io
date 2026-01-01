<script setup>
import { computed } from 'vue'
import { convertMarkdownContentToHtml } from '../utils';

import expJson from '../content/experience.json'

const expArr = computed(() => {
  return convertMarkdownContentToHtml(expJson)
})
const idPrefix = "experience"

</script>

<template>
  <h2>💼 Experience</h2>
  <div class="row items-align-top" v-for="(experience, index) in expArr" :key="index">
    <label class="col-quarter" :for="`${idPrefix}-${index}`" style="max-width: none; text-align: center;">{{ experience.date }}</label>
    <label class="col-quarter" :for="`${idPrefix}-${index}`" style="max-width: none; text-align: center;">{{ experience.role }}</label>
    <div class="col tight-list" :id="`${idPrefix}-${index}`" v-html="experience.content"></div>
  </div>
</template>