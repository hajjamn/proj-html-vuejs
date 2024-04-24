<script>
export default {
  data() {
    return {

    }
  },
  props: {
    item: Object,
  }
}
</script>

<template>
  <div>
    <img :src="item.src" alt="">
    <div class="row text-center">
      <div class="col-12">
        <h2>{{ item.city }}</h2>
      </div>
      <div class="col-4">
        <p class="before-title">CALL US</p>
        <p class="before-title">{{ item.phone }}</p>
      </div>
      <div class="col-4">
        <p class="before-title">OPEN ALL WEEK</p>
        <p class="before-title">{{ item.openingTime }} - {{ item.closingTime }}</p>
      </div>
      <div class="col-4">
        <button class="my-btn my-btn-white">View Map</button>
      </div>
    </div>
  </div>
</template>

<style scoped>
h2 {
  margin-top: 40px;
  color: var(--fifth_color);
  font-weight: 700;
  margin-bottom: 25px;
}

p {
  margin: 0;
}
</style>