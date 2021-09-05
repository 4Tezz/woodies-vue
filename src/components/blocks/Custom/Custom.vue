<template>
  <section class="custom">
    <div class="container">
      <div class="custom__container">
        <h2 class="custom__title title">How to custom</h2>
        <div class="custom__content">
          <div class="custom__card">
            <div class="custom__card__image">
              <img src="@/assets/images/card.png" alt="design" loading="lazy" />
            </div>
            <h3 class="custom__card__title">Choose Design</h3>
          </div>
          <div class="custom__card">
            <div class="custom__card__image">
              <img
                src="@/assets/images/ruler.png"
                alt="design"
                loading="lazy"
              />
            </div>
            <h3 class="custom__card__title">Area measuring</h3>
          </div>
          <div class="custom__card">
            <div class="custom__card__image">
              <img
                src="@/assets/images/calculate.png"
                alt="design"
                loading="lazy"
              />
            </div>
            <h3 class="custom__card__title">Budgeting</h3>
          </div>
          <div class="custom__card">
            <div class="custom__card__image">
              <img
                src="@/assets/images/human.png"
                alt="design"
                loading="lazy"
              />
            </div>
            <h3 class="custom__card__title">Production</h3>
          </div>
        </div>
        <Btn variant="orange">Get Personalized Now</Btn>
      </div>
    </div>
  </section>
</template>

<script >
import Btn from '@/components/commons/Btn.vue'
export default {
  components: { Btn }
}
</script>
