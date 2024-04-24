<script>
import AppHeader from './AppHeader.vue'
import menuItems from '../../../data/menu.json'

export default {
  components: {
    AppHeader,
  },
  data() {
    return {
      menuItems,
    }
  }
}

</script>

<template>

  <section id="app-hero">
    <AppHeader :items="menuItems"></AppHeader>
    <div class="the-stuff-that-is-not-the-header position-relative">
      <div class="position-absolute top-0 end-0 px-2">
        <div class="my-square mb-2">
          <font-awesome-icon :icon="['fas', 'folder']" />
          <span>Demos</span>
        </div>
        <div class="my-square green">
          <div class="green-price d-flex">
            <span class="dollar-sign">$</span>
            <span class="price">39</span>
          </div>
          <span>On Sale</span>
        </div>
      </div>
      <div class="my-container my-container-small" id="hero">
        <div class="row">
          <div class="col-4">
            <p class="before-title">FRESH & TASTY BAKERY EVERY DAY</p>
            <h1>The Perfect Fresh Bread</h1>
            <p class="my-3">Lorem ipsum dolor sit amet consectetur adipisicing elit. Praesentium rerum, cum earum
              consequuntur beatae
              nihil hic, quos nulla sit aliquid excepturi eveniet possimus magnam. Adipisci obcaecati repellendus
              blanditiis totam nam?</p>
            <button class="my-btn my-btn-white my-2">Explore our products</button>
          </div>
        </div>
      </div>
    </div>
  </section>

</template>

<style scoped>
h1 {
  color: var(--fifth_color);
  font-weight: 700;
}

#hero {
  padding-top: 190px;
}

.my-square {
  background-color: var(--first_color);
  border-radius: 5px;
  padding: 10px 5px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  box-shadow: 0 0 3px #000000;
  color: var(--fifth_color);
  cursor: pointer;
}

.green-price {
  color: green;
}

.dollar-sign {
  margin-top: 0;
  display: inline-block;
}

.price {
  margin-top: 2px;
  display: inline-block;
  font-size: large;
}
</style>