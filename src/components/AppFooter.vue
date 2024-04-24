<script>
import menu from '../data/menu.json'
import { store } from '../store'

export default {
  data() {
    return {
      menu,
      store,
    }
  }
}

</script>

<template>
  <footer>
    <div class="d-flex justify-content-between">
      <div class="d-flex flex-column">
        <div class="mb-5">
          <img src="/public/img/avada-bakery-logo.png" alt="">
        </div>
        <div class="">
          <ul class="d-flex gap-4 justify-content-start ps-0">
            <li>
              <a :href="menu.menuItems[1].anchor">{{ menu.menuItems[1].title }}</a>
            </li>
            <li>
              <a :href="menu.menuItems[1].anchor">{{ menu.menuItems[2].title }}</a>
            </li>
            <li>
              <a :href="menu.menuItems[1].anchor">{{ menu.menuItems[3].title }}</a>
            </li>
            <li>
              <a :href="menu.menuItems[1].anchor">{{ menu.menuItems[4].title }}</a>
            </li>
            <li>
              <a :href="menu.menuItems[1].anchor">{{ menu.menuItems[5].title }}</a>
            </li>
            <li>
              <a :href="menu.menuItems[1].anchor">{{ menu.menuItems[6].title }}</a>
            </li>
            <li>
              <a href="#">Orders</a>
            </li>
            <li>
              <font-awesome-icon icon="fa-solid fa-cart-shopping" />
              <div class="my-shop-items">{{ store.cartItems }}</div>
            </li>
          </ul>
        </div>
        <div class="my-margin-top">
          <p class="before-title">© Copyright | 2012 - 2020 | Avada Theme by THemeFusion | All Rights Reserved | Powered
            by WordPress</p>
        </div>
      </div>
      <div class="d-flex flex-column">
        <div class="">
          <h4>Subscribe to our Newsletter</h4>
        </div>
        <div class="">
          <input type="email" class="p-2 mt-4" placeholder="Enter email address*">
          <button class="my-btn my-btn-purple ms-2">Subscribe</button>
        </div>
        <div class="my-margin-top-2">
          <ul class="d-flex gap-5 justify-content-end">
            <li><font-awesome-icon icon="fa-brands fa-instagram" /></li>
            <li><font-awesome-icon icon="fa-brands fa-twitter" /></li>
            <li><font-awesome-icon icon="fa-brands fa-facebook-f" /></li>
            <li><font-awesome-icon icon="fa-brands fa-pinterest-p" /></li>
          </ul>
        </div>
      </div>
    </div>
  </footer>

</template>

<style scoped>
footer {
  padding: 90px;
  color: var(--fifth_color);
}

h4 {
  font-weight: 700;
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

.my-margin-top {
  margin-top: 150px;
}

.my-margin-top-2 {
  margin-top: 225px;
}

.my-shop-items {
  background-color: var(--fourth_color);
  text-align: center;
  border-radius: 100%;
  padding: 0 0.5rem;
  display: inline-block;
  margin-left: 5px;
}
</style>