<template>
  <carousel-section :slides="slides" class="section">
    <template #title>
      <span class="section__title">
        Newly adquired
      </span>
    </template>
  </carousel-section>
</template>

<script>
import CarouselSection from './CarouselSection.vue'

export default {
  name: 'SectionRestaurantsAndBars',
  components: {
    CarouselSection
  },
  data () {
    return {
      slides: [
        {
          img: 'yellowflower1.jpg',
          serviceName: 'Name',
          establishmentName: 'Flower name',
          description: 'Lorem ipsum dolorem sit amet consecuteur'
        },
        {
          img: 'yellowflower1.jpg',
          serviceName: 'Name',
          establishmentName: 'Flower name',
          description: 'Lorem ipsum dolorem sit amet consecuteur'
        },
        {
          img: 'yellowflower1.jpg',
          serviceName: 'Name',
          establishmentName: 'Flower name',
          description: 'Lorem ipsum dolorem sit amet consecuteur'
        }
      ]
    }
  }
}
</script>

<style scoped>
.section {
  background-image: url("~/static/sunflower1.jpg");
  background-size: 100% auto;
  background-position-y: top;
}

.section__title {
  color: var(--title2);
  font-weight: bold;
}
</style>
