<script>

export default {
  data() {
    return {
      hover: false,
    }
  },
  props: {
    item: Object,
  }
}
</script>

<template>
  <div class="text-center" @mouseover="hover = true" @mouseleave="hover = false">
    <div class="my-wrapper">
      <img :src="`/img/${item.src}.jpg`" :alt="item.name">
      <div class="my-overlay" :class="hover === true ? 'my-active' : ''">
        <p>SELECT OPTIONS / QUICK VIEW</p>
      </div>
    </div>
    <h5>{{ item.name }}</h5>
    <p>${{ item.firstPrice }} - ${{ item.secondPrice }}</p>
  </div>
</template>

<style scoped>
h5 {
  color: var(--fifth_color);
  font-weight: 700;
}

.my-wrapper {
  text-align: center;
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.my-overlay {
  height: 100%;
  width: 100%;
  position: absolute;
  background-color: rgba(0, 0, 0, 0.5);
  color: white;
  opacity: 0;
  transition: opacity 0.5s ease-in-out;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.my-active {
  opacity: 1;
}
</style>