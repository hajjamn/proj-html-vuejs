<script>
import AppHeader from './hero/AppHeader.vue'
import AppHero from './hero/AppHero.vue'
import BigSlider from './big slider/BigSlider.vue'
import SpecialMoments from './special moments/SpecialMoments.vue'
import SmallSlider from './small slider/SmallSlider.vue'
import Process from './process/Process.vue'
import Locations from './locations/Locations.vue'
import Socials from './socials/Socials.vue'

export default {
  components: {
    AppHeader,
    AppHero,
    BigSlider,
    SpecialMoments,
    SmallSlider,
    Process,
    Locations,
    Socials,
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
  <SmallSlider></SmallSlider>
  <Process></Process>
  <Locations></Locations>
  <Socials></Socials>

</template>

<style></style>