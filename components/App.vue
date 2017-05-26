<template>
  <div class="App">
    <TopNav/>
    <AppContent/>
    <MenuNav/>
  </div>
</template>

<script>
import TopNav from '~components/TopNav'
import AppContent from '~components/AppContent'
import MenuNav from '~components/MenuNav'

export default {
  components: { TopNav, AppContent, MenuNav }
}
</script>

<style>
.App {
  height: 100%;
}
</style>
