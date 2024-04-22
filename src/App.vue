<script>
import { store } from './store.js'

export default {
  data() {
    return {
      store,
    }
  }
}

</script>

<template>

  <div>
    {{ store.message }}
  </div>

</template>

<style lang="scss">
@use './assets/style/general.scss'
</style>
