<script>
import AppHeader from './AppHeader.vue'
import AppHero from './AppHero.vue'
import BigSlider from './BigSlider.vue'
import SpecialMoments from './SpecialMoments.vue'

export default {
  components: {
    AppHeader,
    AppHero,
    BigSlider,
    SpecialMoments,
  },
  data() {
    return {
    }
  }
}

</script>

<template>

  <AppHero></AppHero>
  <BigSlider></BigSlider>
  <SpecialMoments></SpecialMoments>

</template>

<style></style>