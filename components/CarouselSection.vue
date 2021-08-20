<template>
  <content-section :title="title">
    <vueper-slides
      v-if="slides.length"
      class="w-full no-shadow"
      arrows-outside
      transition-speed="250"
      fixed-height="28em"
      bullets-outside
      :breakpoints="breakpoints"
      :gap="2"
    >
      <vueper-slide
        v-for="(slide, index) in slides"
        :key="slide.img + index"
      >
        <template #content>
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
        </template>
      </vueper-slide>
    </vueper-slides>
  </content-section>
</template>

<script>
import { VueperSlides, VueperSlide } from 'vueperslides'
import ContentSection from './ContentSection.vue'

export default {
  components: {
    ContentSection,
    VueperSlides,
    VueperSlide
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
  },
  data () {
    return {
      breakpoints: {
        4000: {
          visibleSlides: 3,
          slideMultiple: 3
        },
        1100: {
          visibleSlides: 2,
          slideMultiple: 2
        },
        690: {
          visibleSlides: 2,
          slideMultiple: 2,
          arrows: false,
          bulletsOutside: true
        },
        600: {
          arrows: false,
          bulletsOutside: true
        }
      }
    }
  }
}
</script>

<style>
.w-full {
  width: 100% !important;
}

</style>
