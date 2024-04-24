<script>

export default {
  data() {
    return {
      pics: '/img/social-'
    }
  }
}

</script>

<template>
  <section>
    <div class="my-container my-container-small">
      <div class="row gx-4 gy-4">
        <div class="col-3">
          <img :src="`${pics}1.jpg`" alt="">
        </div>
        <div class="col-6">
          <div class="my-info">
            <p class="before-title">MADE FOR SHARING</p>
            <h2>Let's stay in touch</h2>
            <button class="my-btn my-btn-purple"><font-awesome-icon icon="fa-brands fa-instagram" /> Follow Us</button>
          </div>
        </div>
        <div class="col-3">
          <img :src="`${pics}2.jpg`" alt="">
        </div>
        <div class="col-3">
          <img :src="`${pics}3.jpg`" alt="">
        </div>
        <div class="col-3">
          <img :src="`${pics}4.jpg`" alt="">
        </div>
        <div class="col-3">
          <img :src="`${pics}5.jpg`" alt="">
        </div>
        <div class="col-3">
          <img :src="`${pics}6.jpg`" alt="">
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
section {
  margin-bottom: 170px;
}

img {
  max-width: 100%;
}

.my-info {
  background-color: var(--second_color);
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100%;
}

h2 {
  color: var(--fifth_color);
  font-weight: 700;
  margin-bottom: 25px;
}
</style>