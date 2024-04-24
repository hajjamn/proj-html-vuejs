<script>
import AppHeader from './hero/AppHeader.vue'
import AppHero from './hero/AppHero.vue'
import BigSlider from './big slider/BigSlider.vue'
import SpecialMoments from './special moments/SpecialMoments.vue'

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