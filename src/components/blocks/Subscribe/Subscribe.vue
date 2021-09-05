<template>
  <section class="subscribe">
    <div class="container">
      <div class="subscribe__container">
        <div class="subscribe__content">
          <h3 class="subscribe__title">Subscribe to our newsletter</h3>
          <p class="subscribe__text">
            A monthly digest of the new WOODIES products, hot offers, and
            resources.
          </p>
        </div>

        <form class="subscribe__form">
          <span>
            <input
              type="email"
              class="subscribe__form__control"
              placeholder="Your email address"
              required
            />
            <Btn variant="orange">Subscribe</Btn>
          </span>
        </form>
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
