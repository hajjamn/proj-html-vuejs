<script>
import AppHeader from './AppHeader.vue'

export default {
  components: {
    AppHeader,
  },
  data() {
    return {
      name: 'Content'
    }
  }
}

</script>

<template>

  <section id="app-hero">
    <AppHeader></AppHeader>
    Hello I am the app hero
  </section>


  <div>
    <h1>I am the {{ name }}</h1>
  </div>

</template>

<style></style>