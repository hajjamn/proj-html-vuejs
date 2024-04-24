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
  <div class="position-relative">
    <img :src="item.src" alt="">
    <div class="my-overlay">
      <div class="row gx-5 gy-5 text-white w-100 h-100 p-5">
        <div class="col-6">
          <h2 class="pe-5">{{ item.title }}</h2>
        </div>
        <div class="col-6 text-end">
          <p class="number fw-light">{{ item.number }}</p>
        </div>
        <div class="col-6">
          <div v-if="item.textLocation === 'bottom-left'" class="pt-4">
            <p class="before-title">{{ item.comment }}</p>
            <p class="text-bottom">{{ item.text }}</p>
          </div>
        </div>
        <div class="col-6">
          <div v-if="item.textLocation === 'bottom-right'" class="pt-4">
            <p class="before-title">{{ item.comment }}</p>
            <p class="text-bottom">{{ item.text }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.col-6 {
  height: 50%;
}

.my-overlay {
  position: absolute;
  background-color: rgba(50, 50, 50, 0.35);
  width: 100%;
  height: 100%;
  top: 0;
}

h2 {
  font-size: 50px;
}

.number {
  font-size: 64px;
}
</style>