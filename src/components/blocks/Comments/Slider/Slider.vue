<template>
  <div class="slider">
    <div class="slider__box">
      <div class="slider__comment">
        <ul class="slider__stars">
          <Star v-for="star in comment.stars" :key="star" :star="star" />
        </ul>
        <figure>
          <blockquote>
            <q class="slider__comment_text">
              {{ comment.text }}
            </q>
            <div class="slider__comment__contact">
              <div class="slider__comment__avatar">
                <img :src="comment.avatar" alt="Sandra" loading="lazy" />
              </div>
              <figcaption>
                {{ comment.name }} <cite> {{ comment.city }}</cite>
              </figcaption>
            </div>
          </blockquote>
        </figure>
      </div>
    </div>
    <div class="slider__pagination">
      <div class="slider__pagination__links">
        <button
          href="#"
          class="first"
          @click="this.$emit('ChangePagination', { type: 'prev' })"
          :class="{ disabled: isPrevValida }"
          :disabled="isPrevValida"
        >
          Previous
        </button>
        <button
          href="#"
          class="second"
          @click="this.$emit('ChangePagination', { type: 'next' })"
          :class="{ disabled: isNextValida }"
          :disabled="isNextValida"
        >
          Next
        </button>
      </div>
      <ul class="slider__pagination__progress">
        <li
          v-for="item in 4"
          :key="item"
          :class="{ active: item === pagination + 1 }"
          @click="this.$emit('ChangePagination', { type: 'this', value: item })"
        ></li>
      </ul>
    </div>
  </div>
</template>

<script>
import Star from './Star/Star.vue'
export default {
  props: {
    comment: {
      type: Object,
      required: true
    },
    pagination: {
      type: Number
    },
    commentsLength: {
      type: Number
    }
  },
  computed: {
    isPrevValida () {
      return this.$props.pagination <= 0
    },
    isNextValida () {
      return this.$props.pagination >= this.$props.commentsLength - 1
    }
  },
  components: { Star }
}
</script>
