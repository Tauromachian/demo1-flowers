<template>
  <content-section :title="title" class="justify-center">
    <v-container>
      <vueper-slides
        v-if="slides.length"
        class="w-full no-shadow"
        arrows-outside
        transition-speed="250"
        fixed-height="30em"
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
              <v-card-title>
                {{ slide.serviceName }}
              </v-card-title>
              <v-card-subtitle>
                {{ slide.establishmentName }}
              </v-card-subtitle>
              <v-card-text>
                {{ slide.description }}
              </v-card-text>
              <v-card-actions class="justify-center">
                <v-btn text color="primary" class="text-transform-capitalize">
                  Reservar ya
                </v-btn>
              </v-card-actions>
            </v-card>
          </template>
        </vueper-slide>
      </vueper-slides>
    </v-container>
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
