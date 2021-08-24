<template>
  <carousel-section
    title="Servicios del Hogar"
    :slides="slides"
    class="background-color-grey mb-0"
  />
</template>

<script>
import CarouselSection from './CarouselSection.vue'

export default {
  name: 'SectionHomeServices',
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
.background-color-grey {
  background-color: var(--section-background-color-primary);
}
</style>
