<template>
  <div class="we-have__card">
    <div class="we-have__card-bg">
      <img :src="img" alt="desk" loading="lazy" />
    </div>
    <h3 class="we-have__card__title">{{ title }}</h3>
    <Btn>Shop Now</Btn>
  </div>
</template>

<script>
import Btn from '@/components/commons/Btn.vue'
export default {
  props: {
    title: {
      type: String,
      required: true
    },
    img: {
      type: String,
      required: true
    }
  },
  components: { Btn }
}
</script>

<style >
</style>
