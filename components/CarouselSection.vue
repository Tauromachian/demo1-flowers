<template>
  <content-section :title="title">
    <v-carousel v-if="slides.length" multiple>
      <v-carousel-item v-for="(slide, index) in slides" :key="index" />
    </v-carousel>
  </content-section>
</template>

<script>
import ContentSection from './ContentSection.vue'
export default {
  components: {
    ContentSection
  },
  props: {
    slides: {
      type: Array,
      default: () => []
    },
    title: {
      type: String,
      required: true
    }
  }
}
</script>

<style>

</style>
