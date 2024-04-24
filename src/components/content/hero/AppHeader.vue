<script>

export default {
  data() {
    return {
      name: 'Header'
    }
  },
  props: {
    items: Object,
  }
}

</script>

<template>
  <header>
    <div class="d-flex justify-content-between align-items-center">
      <div>
        <img src='/public/img/avada-bakery-logo-retina-200x97.png' alt="">
      </div>
      <div>
        <ul class="d-flex">
          <li class="mx-3" v-for="item in items.menuItems"><a :href="`${item.anchor}`">{{ item.title }}</a>
          </li>
          <li class="mx-3"><a href="#"><font-awesome-icon icon="fa-solid fa-cart-shopping" /></a></li>
        </ul>
      </div>
    </div>
  </header>
</template>

<style scoped>
header {
  padding: 15px 30px;
  color: var(--fifth_color);
}

ul {
  list-style-type: none;
}

a {
  text-decoration: none;
  color: currentColor;
}

li:hover {
  text-decoration: underline;
}
</style>