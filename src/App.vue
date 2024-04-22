<script>
import { store } from './store.js'
import AppContent from './components/AppContent.vue'
import AppFooter from './components/AppFooter.vue'

export default {
  components: {
    AppContent,
    AppFooter
  },
  data() {
    return {
      store,
    }
  }
}

</script>

<template>

  <div>
    <AppContent></AppContent>
    <AppFooter></AppFooter>
  </div>

</template>

<style lang="scss">
@use './assets/style/general.scss';
@use 'bootstrap'
</style>
