<template>
  <div :class="{ 'width-100': fluid }">
    <slot />
  </div>
</template>

<script>
export default {
  name: 'BaseSection',
  props: {
    fluid: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<style>
.width-100 {
  width: 100%;
}
</style>
