<script>

export default {
  data() {
    return {
      hover: false
    }
  },
  props: {
    item: Object
  }
}
</script>

<template>
  <div class="col position-relative" @mouseover="hover = true" @mouseleave="hover = false">
    <img :src="hover === false ? `/img/${item.firstImage}` : `/img/${item.secondImage}`" alt="">
    <div class="my-overlay" :class="hover === true ? 'my-active' : ''">
      <p class=" before-title">{{ item.description }}</p>
      <h2 class="text-white my-4">{{ item.title }}</h2>
      <button class="my-btn my-btn-purple">Explore more</button>
    </div>
  </div>
</template>

<style scoped>
.col {
  display: flex;
  justify-content: center;
  align-items: center;
}

.my-overlay {
  text-align: center;
  position: absolute;
  margin: auto;
  padding: 0 12px;
  opacity: 0;
  transition: opacity 0.5s ease-in-out;
}

.my-active {
  opacity: 1;
}
</style>