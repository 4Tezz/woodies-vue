<template>
  <li>
    <img src="@/assets/images/star.svg" :alt="`star-${star}`" />
  </li>
</template>

<script>
export default {
  props: {
    star: {
      type: Number
    }
  }
}
</script>

<style lang="scss" scoped>
</style>
