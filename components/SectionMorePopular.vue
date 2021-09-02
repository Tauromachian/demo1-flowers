<template>
  <div class="section-beauty">
    <carousel-section
      title="Servicios de belleza"
      :slides="slides"
      class="section pt-15"
    >
      <template #title>
        <span class="section__title">
          More Popular
        </span>
      </template>
    </carousel-section>
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
          img: 'purpleflower1.jpg',
          serviceName: 'Name',
          establishmentName: 'Flower name',
          description: 'Lorem ipsum dolorem sit amet consecuteur'
        },
        {
          img: 'purpleflower1.jpg',
          serviceName: 'Name',
          establishmentName: 'Flower name',
          description: 'Lorem ipsum dolorem sit amet consecuteur'
        },
        {
          img: 'purpleflower1.jpg',
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
  background-image: url("~/static/sunflower2.jpg");
  background-size: 100% auto;
  background-position-y: top;
}

.section__title {
  color: var(--accent2);
}

@media screen and (min-width: 960px) {
  .section__title {
    color: var(--title1);
  }
}

.section-beauty {
  position: relative;
}

.bottom-line {
  position: absolute;
  background-color: var(--color-primary);
  height: 240px;
  width: 100%;
  bottom: 0;
}
</style>
