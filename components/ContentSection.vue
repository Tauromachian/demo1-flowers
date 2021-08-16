<template>
  <base-section>
    <h1 class="page-section__title">
      {{ title }}
    </h1>
    <slot />
  </base-section>
</template>

<script>
import BaseSection from './BaseSection.vue'

export default {
  name: 'ContentSection',
  components: {
    BaseSection
  },
  props: {
    title: {
      type: String,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
.page-section__title {
  text-transform: uppercase;
  text-align: center;
  color: #185596;
}
</style>
