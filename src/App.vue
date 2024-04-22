<script>
import { store } from './store.js'
import AppHeader from './components/AppHeader.vue'
import AppContent from './components/AppContent.vue'
import AppFooter from './components/AppFooter.vue'

export default {
  components: {
    AppHeader,
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
    <AppHeader class="container"></AppHeader>
    <AppContent class="container"></AppContent>
    <AppFooter class="container container_footer"></AppFooter>
  </div>

</template>

<style lang="scss">
@use './assets/style/general.scss';
@use 'bootstrap'
</style>
