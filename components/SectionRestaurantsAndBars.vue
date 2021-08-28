<template>
  <carousel-section :slides="slides" class="section">
    <template #title>
      <span class="section__title">
        Bares y restaurantes
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
          img: 'picture.png',
          serviceName: 'Nombre',
          establishmentName: 'Nombre del establecimiento',
          description: 'Lorem ipsum dolorem sit amet consecuteur'
        },
        {
          img: 'picture.png',
          serviceName: 'Nombre',
          establishmentName: 'Nombre del establecimiento',
          description: 'Lorem ipsum dolorem sit amet consecuteur'
        },
        {
          img: 'picture.png',
          serviceName: 'Nombre',
          establishmentName: 'Nombre del establecimiento',
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
  background-position-y: center;
}

.section__title {
  color: var(--color-quaternary);
}
</style>
