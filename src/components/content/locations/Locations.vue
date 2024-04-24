<script>
import LocationsCard from './LocationsCard.vue'
import locationsData from '../../../data/locations.json'

export default {
  components: {
    LocationsCard,
  },
  data() {
    return {
      locationsData,
    }
  }
}
</script>

<template>
  <section>
    <div class="my-container my-container-small text-center">
      <p class="before-title">LOCATIONS</p>
      <h2 class="mb-5">Visit our Bakeries</h2>
    </div>
    <div class="my-container my-container-small">
      <div class="row">
        <div class="col p-0" v-for="location in locationsData.locations">
          <LocationsCard :item="location"></LocationsCard>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
section {
  margin: 200px 0;
}

h2 {
  color: var(--fifth_color);
  font-weight: 700;
}
</style>