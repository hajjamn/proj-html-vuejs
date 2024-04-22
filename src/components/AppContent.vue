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

  <AppHeader></AppHeader>

  <div>
    <h1>I am the {{ name }}</h1>
  </div>

</template>

<style></style>