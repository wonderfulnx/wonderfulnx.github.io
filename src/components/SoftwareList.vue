<script setup>
import { computed } from 'vue'

import {convertNestedMarkdownContentToHtml} from '../utils'

import softwareJson from '../content/softwares.json'


const softwareArr = computed(() => {
  return convertNestedMarkdownContentToHtml(softwareJson)
})
const idPrefix = "software"

</script>

<template>
  <h2>🕹️ Selected Repositories</h2>
  <div v-for="(softwareList, listIdx) in softwareArr" :key="listIdx">
    <!-- <h3>{{ softwareList.category }}</h3> -->
    <div class="row items-align-top" v-for="(software, index) in softwareList.list" :key="index">
      <label class="col-2" :for="`${idPrefix}-${listIdx}-${index}`" style="max-width: none; text-align: center;">
        <a :href="software.url"><b>{{ software.name }}</b></a>
      </label>
      <div class="col flex-start tight-list" :id="`${idPrefix}-${listIdx}-${index}`" v-html="software.content"></div>
    </div>
  </div>
</template>