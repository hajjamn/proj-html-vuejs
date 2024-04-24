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
  <div class="text-center">
    <img :src="`/img/${item.src}.jpg`" :alt="item.name">
    <h5>{{ item.name }}</h5>
    <p>${{ item.firstPrice }} - ${{ item.secondPrice }}</p>
  </div>
</template>

<style scoped>
h5 {
  color: var(--fifth_color);
  font-weight: 700;
}
</style>