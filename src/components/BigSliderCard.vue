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

  <div class="position-relative">
    <img :src="`/img${item.src}`" :alt="item.name" @mouseover="hover = true" @mouseleave="hover = false">
    <div class="my-card-overlay" :class="hover === false ? 'my-hover' : ''">
      <strong>{{ item.name }}</strong>
      <em>{{ item.tags[0] }}, {{ item.tags[1] }}</em>
      <p>${{ item.firstPrice }} ${{ item.secondPrice }}</p>
    </div>
  </div>


</template>

<style>
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
}

.my-hover {
  opacity: 0;
}
</style>