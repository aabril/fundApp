<template>
  <div class="LemoorApp">
    <TopNav/>
    <AppContent/>
    <MenuNav/>
  </div>
</template>

<script>
import TopNav from '~components/LemoorApp/TopNav'
import AppContent from '~components/LemoorApp/AppContent'
import MenuNav from '~components/LemoorApp/MenuNav'

export default {
  components: { TopNav, AppContent, MenuNav }
}
</script>

<style>
.LemoorApp {
  height: 100%;
}
</style>
