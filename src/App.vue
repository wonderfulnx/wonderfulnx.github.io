<script setup>
import Bio from './components/Bio.vue'
import NewsList from './components/NewsList.vue'
import EducationList from './components/EducationList.vue'
import PublicationList from './components/PublicationList.vue'
import AwardList from './components/AwardList.vue'
import SoftwareList from './components/SoftwareList.vue'
import TalkList from './components/TalkList.vue'

</script>

<template>
  <header>
    <Bio />
    <hr>
  </header>

  <main>
    <NewsList />
    <hr>
    <EducationList />
    <PublicationList />
    <AwardList />
    <!-- <TalkList /> -->
    <SoftwareList />
  </main>

  <footer>
    <hr>
    <p>
      <b>Relevant Links: </b>
      <a href="http://tns.thss.tsinghua.edu.cn/sun/" target="_blank">The System and Ubiquitous Networking (<b>SUN</b>) Group</a>
      | <a href="http://www.greenorbs.org/people/heyuan/" target="_blank">Prof. Yuan He</a>
    </p>
    <p style="text-align: center;">
      Updated by Xin Na in March 2023. 😉
    </p>
  </footer>
</template>

<style>

</style>
