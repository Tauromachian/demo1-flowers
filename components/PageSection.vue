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

<style>
.page-section__title {
  text-transform: uppercase;
  text-align: center;
}
</style>
