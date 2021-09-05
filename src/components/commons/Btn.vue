<template>
  <button :class="`${className || ''} ${variantValidate || 'btn'}`">
    <slot></slot>
  </button>
</template>

<script>
export default {
  props: {
    className: {
      type: String
    },
    variant: {
      type: String
    }
  },
  computed: {
    variantValidate () {
      if (this.$props.variant === 'orange') {
        return 'btn-orange'
      }
      return false
    }
  }
}
</script>

<style lang="scss" scoped>
</style>
