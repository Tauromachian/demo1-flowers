<template>
  <div class="section-beauty">
    <carousel-section
      title="Servicios de belleza"
      :slides="slides"
      class="section"
    >
      <template #title>
        <span class="section__title">
          Servicios de belleza
        </span>
      </template>
    </carousel-section>
    <div class="bottom-line" />
  </div>
</template>

<script>
import CarouselSection from './CarouselSection.vue'

export default {
  name: 'SectionBeauty',
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
  background-image: linear-gradient(
      90deg,
      rgba(34, 110, 186, 0.4),
      rgba(34, 110, 186, 0.4)
    ),
    url("~/static/eyes-makeup.jpg");
  background-size: 100% auto;
  background-position-y: center;
}

.section__title {
  color: white;
}

.section-beauty {
  position: relative;
}

.bottom-line {
  position: absolute;
  background-color: #185596;
  height: 240px;
  width: 100%;
  bottom: 0;
}
</style>
