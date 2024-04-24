<script>
import SmallSliderCard from './SmallSliderCard.vue'
import products from '../../../data/products.json'

export default {
  components: {
    SmallSliderCard
  },
  data() {
    return {
      products,
      index: 0,
      maxIndex: products.products.length - 1,
    }
  },
  computed: {
  },
  methods: {
    getCardIndex(n) {
      if (this.index + n - 1 <= this.maxIndex) {
        return this.index + n - 1
      } else {
        return (this.index + n - 1) - this.maxIndex - 1
      }
    },
    decreaseIndex() {
      if (this.index > 0) {
        this.index--
      } else {
        this.index = this.maxIndex
      }
    },
    increaseIndex() {
      if (this.index < this.maxIndex) {
        this.index++
      } else {
        this.index = 0
      }
    }
  }
}

</script>

<template>

  <section>
    <div class="my-container my-container-small">
      <div class="row">
        <div class="col-3 my-info-wrapper pt-5 px-5 mt-5">
          <h3>Find a freshly baked product perfect for you</h3>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Aut consequuntur molestiae a aspernatur
            voluptates.</p>
          <button class="my-btn my-btn-purple">Shop All Products</button>
        </div>
        <div class="col-9">
          <div class="my-slider">
            <button class="my-slider-btn start-0 z-3" @click="decreaseIndex()"><span>
                < </span></button>
            <button class="my-slider-btn end-0 z-3" @click="increaseIndex()"><span> > </span></button>
            <SmallSliderCard :item="products.products[getCardIndex(1)]"></SmallSliderCard>
            <SmallSliderCard :item="products.products[getCardIndex(2)]"></SmallSliderCard>
            <SmallSliderCard :item="products.products[getCardIndex(3)]"></SmallSliderCard>
            <SmallSliderCard :item="products.products[getCardIndex(4)]"></SmallSliderCard>
          </div>
        </div>
      </div>
    </div>
  </section>

</template>

<style scoped>
section {
  margin: 220px 0;
}

h3 {
  color: var(--fifth_color);
  font-weight: 700;
}

.my-info-wrapper {
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>