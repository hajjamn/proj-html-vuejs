<script>
import ProcessCard from './ProcessCard.vue'
import processData from '../../../data/process.json'

export default {
  components: {
    ProcessCard,
  },
  data() {
    return {
      processData,
    }
  }
}

</script>

<template>

  <section>
    <div class="my-container my-container-small">
      <div class="row gy-4 gx-5">
        <div class="col-12">
          <ProcessCard :item="processData.cards[0]"></ProcessCard>
        </div>
        <div class="col-6">
          <ProcessCard :item="processData.cards[1]"></ProcessCard>
        </div>
        <div class="col-6 my-supercazzola-wrapper">
          <p class="before-title">DON'T JUST TAKE OUR WORD FOR IT</p>
          <h2 class="supercazzola">"Finally found an alternative to the mass produced products. Something that
            incorporates real organic
            ingredients, nutrient dense wellness while promoting sustainability and activity."</h2>
          <p class="before-title">Rachel Cooper, Founder</p>
        </div>
        <div class="col-12">
          <ProcessCard :item="processData.cards[2]"></ProcessCard>
        </div>
      </div>
    </div>
  </section>

</template>

<style scoped>
.my-supercazzola-wrapper {
  background-color: var(--fourth_color);
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 0 85px
}

.supercazzola {
  color: var(--fifth_color);
  font-weight: 700;
  margin: 54px 0;
}
</style>