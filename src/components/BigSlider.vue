<script>

import products from '../data/products.json'
import BigSliderCard from './BigSliderCard.vue'

export default {
  components: {
    BigSliderCard,
  },
  data() {
    return {
      products,
      currentIndex: 0,
      isNextSlide: false,
      isPrevSlide: false,
    }
  },
  computed: {
    nextIndex() {
      if (this.currentIndex < this.products.products.length - 1) {
        return this.currentIndex + 1
      } else {
        return 0
      }
    },
    nextCurrentIndex() {
      if (this.isNextSlide === true) {
        //se viene pigiato nextSlide devo far comparire currentIndex + 2  che arriva da destra, oppure lo 0
      }
    },
    prevCurrentIndex() {
      if (this.isPrevSlide === true) {
        //se viene pigiato prevSlide devo far comparire currentIndex - 2 che arriva da sinistra, oppure producs.products.length - 1
      }
    },
    firstCard() {
      return document.getElementById(`product-${this.currentIndex}`)
    },
    secondCard() {
      return document.getElementById(`product-${this.nextIndex}`)
    }
  },
  methods: {
    nextSlide() {
      this.isNextSlide = true
      this.firstCard.classList.add('slide-out-left')
      this.secondCard.classList.add('slide-out-left')
      setTimeout(this.increaseIndex, 500)
    },
    increaseIndex() {
      if (this.currentIndex < this.products.products.length - 1) {
        this.currentIndex++
      } else {
        this.currentIndex = 0
      }
      /*       this.firstCard.classList.remove('slide-out-left')
            this.secondCard.classList.remove('slide-out-left')
            this.isNextSlide = false */
    },
    prevSlide() {
      this.isPrevSlide = true
      this.firstCard.classList.add('slide-out-right')
      this.secondCard.classList.add('slide-out-right')
      setTimeout(this.decreaseIndex(), 500)
    },
    decreaseIndex() {
      if (this.currentIndex > 0) {
        this.currentIndex--
      } else {
        this.currentIndex = this.products.products.length - 1
      }
      /*       this.firstCard.classList.remove('slide-out-right')
            this.secondCard.classList.remove('slide-out-right')
            this.isPrevSlide = false */
    }
  }
}
</script>

<template>
  <section>
    <div class="my-container my-container-small">
      <div class="row">
        <div class="col-4 pe-5" id="ciao">
          <p class="before-title">OUR PRODUCTS</p>
          <h2>All our delectable pastries are baked fresh in our Kitchen every morning, and are made with all-natural,
            all organic ingredients.</h2>
          <button class="my-btn my-btn-purple mt-5">Start Shopping</button>
        </div>
        <div class="col-8">
          <div class="my-slider">
            <button class="my-slider-btn start-0 z-3" @click="decreaseIndex()"><span>
                < </span></button>
            <button class="my-slider-btn end-0 z-3" @click="increaseIndex()"><span> > </span></button>
            <!-- <BigSliderCard v-for="(product, i) in products.products" :item="product" :id="`product-${i}`">
            </BigSliderCard> -->
            <BigSliderCard :item="products.products[currentIndex]" :id="`product-${currentIndex}`"></BigSliderCard>
            <BigSliderCard :item="products.products[nextIndex]" :id="`product-${nextIndex}`"></BigSliderCard>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
section {
  margin-top: 170px;
  margin-bottom: 230px;
}

h2 {
  color: var(--fifth_color);
  font-weight: 700;
}

.my-slider img {
  max-width: 526px;
}
</style>