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
    <hr>
    <PublicationList />
    <hr>
    <AwardList />
    <!-- <TalkList /> -->
    <hr>
    <SoftwareList />
  </main>

  <footer>
    <hr>
    <div class="row items-align-top">
      <img class="col-1" src="./assets/footer-left.jpg" style="max-width: none;" alt="personal photo">
      <div class="col" style="text-align: center; margin: auto;">
        <b>Relevant Links: </b>
        <a href="http://tns.thss.tsinghua.edu.cn/sun/" target="_blank">The <b>SUN</b> Group</a>
        | <a href="http://tns.thss.tsinghua.edu.cn/sun/members/YuanHe/" target="_blank">Prof. Yuan He</a>
        <br><br>Updated by Xin Na in June 2023. 😉
      </div>
      <img class="col-1" src="./assets/footer-right.jpg" style="max-width: none;" alt="personal photo">
  </div>
  </footer>
</template>

<style>

</style>
