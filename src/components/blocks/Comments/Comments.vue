<template>
  <section class="comments">
    <div class="container">
      <div class="comments__container">
        <h2 class="comments__title title">What they say</h2>
        <div class="comments__content">
          <div class="comments__images">
            <img
              src="@/assets/images/bedroom.png"
              alt="bedroom"
              loading="lazy"
              class="first"
            />
            <img
              src="@/assets/images/kitchen.png"
              alt="kitchen"
              loading="lazy"
              class="second"
            />
          </div>
          <Slider
            :comment="comments[pagination]"
            :pagination="pagination"
            :commentsLength="comments.length"
            @ChangePagination="ChangePagination"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Slider from './Slider/Slider.vue'
export default {
  props: {
    comments: {
      type: Array,
      required: true
    }
  },
  data () {
    return {
      pagination: 0
    }
  },
  methods: {
    ChangePagination ({ type, value }) {
      if (type === 'this') {
        this.pagination = value - 1
        return
      }
      this.pagination += type === 'next' ? 1 : -1
    }
  },
  components: { Slider }
}
</script>
