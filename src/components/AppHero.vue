<script>
import AppHeader from './AppHeader.vue'

export default {
  components: {
    AppHeader,
  },
  data() {
    return {
      menuItems: [
        {
          title: 'HOME',
          anchor: '#'
        },
        {
          title: 'SHOP',
          anchor: '#'
        },
        {
          title: 'ABOUT',
          anchor: '#'
        },
        {
          title: 'GALLERY',
          anchor: '#'
        },
        {
          title: 'LOCATIONS',
          anchor: '#'
        },
        {
          title: 'JOURNAL',
          anchor: '#'
        },
        {
          title: 'CONTACT',
          anchor: '#'
        },
        {
          title: 'MY ACCOUNT',
          anchor: '#'
        },
      ]
    }
  }
}

</script>

<template>

  <section id="app-hero">
    <AppHeader :items="menuItems"></AppHeader>

    <div class="container container_small">
      <div class="row">
        <div class="col-4">
          <p class="before-title">FRESH &TASTY BAKERY EVERY DAY</p>
          <h1>The Perfect Fresh Bread</h1>
          <p class="my-3">Lorem ipsum dolor sit amet consectetur adipisicing elit. Praesentium rerum, cum earum
            consequuntur beatae
            nihil hic, quos nulla sit aliquid excepturi eveniet possimus magnam. Adipisci obcaecati repellendus
            blanditiis totam nam?</p>
          <button class="my-btn my-btn-white my-2">Explore our products</button>
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

.container_small {
  margin-top: 190px;
}
</style>