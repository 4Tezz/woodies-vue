<template>
  <header class="header header-root">
    <div class="container">
      <div class="nav__brand">
        <img src="@/assets/images/woodies-logo.jpg" alt="logo" />
      </div>
      <nav class="nav" :class="{ active: burger }">
        <ul class="nav__list">
          <li class="nav__item">
            <a href="#" class="nav__link active"> Home </a>
          </li>
          <li class="nav__item">
            <a href="#" class="nav__link"> About Us </a>
          </li>
          <li class="nav__item">
            <a href="#" class="nav__link"> How it works </a>
          </li>
          <li class="nav__item">
            <a href="#" class="nav__link"> Categories </a>
          </li>
          <li class="nav__item">
            <a href="#" class="nav__link"> Testimony </a>
          </li>
        </ul>
      </nav>
      <Btn className="nav__sign-up">SIGN UP</Btn>
      <button
        class="btn-toggler"
        :class="{ active: burger }"
        @click="burgerToggler"
      >
        <span></span>
      </button>
    </div>
  </header>
</template>

<script>
import Btn from '@/components/commons/Btn.vue'
export default {
  data () {
    return {
      burger: false
    }
  },
  methods: {
    burgerToggler () {
      this.burger = !this.burger
    }
  },
  components: { Btn }
}
</script>
