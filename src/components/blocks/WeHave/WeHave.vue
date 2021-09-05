<template>
  <section class="we-have">
    <div class="container">
      <div class="we-have__container">
        <h2 class="we-have__title title">What we have</h2>
        <div class="we-have__content">
          <Card v-for="item in supplies" :key="item.title" :title="item.title" :img="item.img"/>
          <!-- <div class="we-have__card">
            <div class="we-have__card-bg">
              <img
                src="@/assets/images/desk-card.jpg"
                alt="desk"
                loading="lazy"
              />
            </div>
            <h3 class="we-have__card__title">Desk</h3>
             <Btn>Shop Now</Btn>
          </div>
          <div class="we-have__card">
            <div class="we-have__card-bg">
              <img
                src="@/assets/images/chair-card.jpg"
                alt="desk"
                loading="lazy"
              />
            </div>
            <h3 class="we-have__card__title">Chair</h3>
            <Btn>Shop Now</Btn>
          </div>
          <div class="we-have__card">
            <div class="we-have__card-bg">
              <img
                src="@/assets/images/kitchenware-card.jpg"
                alt="desk"
                loading="lazy"
              />
            </div>
            <h3 class="we-have__card__title">Kitchenware</h3>
            <Btn>Shop Now</Btn>
          </div>
          <div class="we-have__card">
            <div class="we-have__card-bg">
              <img
                src="@/assets/images/book-shelf-card.jpg"
                alt="desk"
                loading="lazy"
              />
            </div>
            <h3 class="we-have__card__title">Book Shelf</h3>
            <Btn>Shop Now</Btn>
          </div>
          <div class="we-have__card">
            <div class="we-have__card-bg">
              <img
                src="@/assets/images/electronics.jpg"
                alt="desk"
                loading="lazy"
              />
            </div>
            <h3 class="we-have__card__title">Electronics</h3>
            <Btn>Shop Now</Btn>
          </div> -->
        </div>
      </div>
    </div>
  </section>
</template>

<script>

import Card from './Card/Card.vue'
export default {
  props: {
    supplies: {
      type: Array
    }
  },
  components: { Card }
}
</script>
