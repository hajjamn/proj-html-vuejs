<script>

export default {
  data() {
    return {
      hover: false
    }
  },
  props: {
    item: Object,
  }
}
</script>

<template>

  <div class="position-relative my-card">
    <img :src="`/img/${item.src}.jpg`" :alt="item.name" @mouseover="hover = true" @mouseleave="hover = false">
    <div class="my-card-overlay" :class="hover === false ? 'my-hover' : ''">
      <div class="my-info-wrapper">
        <h4>{{ item.name }}</h4>
        <em class="mb-3">{{ item.tags[0] }}, {{ item.tags[1] }}</em>
        <h5>${{ item.firstPrice }} ${{ item.secondPrice }}</h5>
      </div>
    </div>
  </div>


</template>

<style>
.my-card {
  width: 50%;
  flex-shrink: 0;
}

img {
  max-width: 100%;
}

.my-card-overlay {
  background-color: rgba(0, 0, 0, 0.5);
  position: absolute;
  right: 0;
  left: 0;
  top: 0;
  bottom: 0;
  margin: auto;
  color: white;
  pointer-events: none;
  opacity: 1;
  transition: opacity 0.5s ease;
  display: flex;
}

.my-hover {
  opacity: 0;
}

.my-info-wrapper {
  margin: auto;
  display: flex;
  flex-direction: column;
  text-align: center;
}
</style>