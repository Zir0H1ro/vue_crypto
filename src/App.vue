<template>
  <div id="app">
    <TopBar />
    <div class="d-flex">
      <Sidebar />
      <MainContent />
    </div>
  </div>
</template>

<script>
import TopBar from './components/TopBar.vue'
import Sidebar from './components/Sidebar.vue'
import MainContent from './components/MainContent.vue'

export default {
  name: 'app',
  components: {
    TopBar,
    Sidebar,
    MainContent
  }
}
</script>

<style src="./styles/app_styles.css"></style>
<style lang="scss">
     @import "../node_modules/bootstrap/scss/bootstrap.scss";
</style>
