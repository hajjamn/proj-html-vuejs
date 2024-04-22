<script>
import AppHeader from './AppHeader.vue'
import AppHero from './AppHero.vue'

export default {
  components: {
    AppHeader,
    AppHero,
  },
  data() {
    return {
      name: 'Content'
    }
  }
}

</script>

<template>

  <AppHero></AppHero>


  <div>
    <h1>I am the {{ name }}</h1>
  </div>

</template>

<style></style>