<script>
import SpecialMomentsCard from './SpecialMomentsCard.vue'
import SpecialMomentsData from '../../../data/specialmoments.json'

export default {
  components: {
    SpecialMomentsCard
  },
  data() {
    return {
      SpecialMomentsData
    }
  }
}
</script>

<template>
  <section>
    <div class="my-container my-container-small">
      <div class="text-center mb-5">
        <p class="before-title">CORPORATE & WEDDINGS</p>
        <h3>Baking Special Moments</h3>
      </div>
    </div>
  </section>
  <div class="my-container my-container-small">
    <div class="row my-row">
      <SpecialMomentsCard v-for="data in SpecialMomentsData.cardData" :item="data"></SpecialMomentsCard>
    </div>
  </div>
</template>

<style scoped>
.my-row {
  gap: 100px;
}

h3 {
  color: var(--fifth_color);
  font-weight: 700;
}
</style>