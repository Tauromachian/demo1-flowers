<template>
  <base-section v-bind="$attrs">
    <h1 v-if="title || $slots.title" class="page-section__title mb-5">
      <slot name="title">
        {{ title }}
      </slot>
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
      default: ''
    }
  }
}
</script>

<style lang="scss" scoped>
.page-section__title {
  text-transform: uppercase;
  text-align: center;
  color: #185596;
  font-weight: initial;
}
</style>
