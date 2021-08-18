<template>
  <content-section :title="title">
    <v-carousel v-if="slides.length">
      <v-carousel-item
        v-for="(slide, index) in slides"
        :key="slide.img + index"
      >
        <v-card>
          <v-img :src="slide.img" alt="" />
          <v-card-text>
            <v-card-title>
              {{ slide.serviceName }}
            </v-card-title>
            <v-card-title>
              {{ slide.establishmentName }}
            </v-card-title>
            <p>
              {{ slide.description }}
            </p>
          </v-card-text>
          <v-card-actions>
            <v-btn text>
              Reservar ya
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-carousel-item>
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

<style></style>
