<script setup>
import Bio from './components/Bio.vue'
import NewsList from './components/NewsList.vue'
import EducationList from './components/EducationList.vue'
import PublicationConfList from './components/PublicationConfList.vue'
import PublicationJourList from './components/PublicationJourList.vue'
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
    <hr>
    <PublicationConfList />
    <hr>
    <PublicationJourList />
    <hr>
    <AwardList />
    <!-- <TalkList /> -->
    <hr>
    <SoftwareList />
  </main>

  <footer>
    <hr>
    <div class="row items-align-top">
      <img class="col-1" src="./assets/footer-avatar-3.jpg" style="width: 76px;" alt="personal photo">
      <div class="col" style="text-align: center; margin: auto;">
        <b>Relevant Links: </b>
        <a href="http://tns.thss.tsinghua.edu.cn/sun/" target="_blank">The <b>SUN</b> Group</a>
        | <a href="http://tns.thss.tsinghua.edu.cn/sun/members/YuanHe/" target="_blank">Prof. Yuan He</a>
        <br><br>Updated by Xin Na in May 2025. 😉
      </div>
      <img class="col-1" src="./assets/footer-avatar-4.jpg" style="width: 76px;" alt="personal photo">
  </div>
  </footer>
</template>

<style>

</style>
