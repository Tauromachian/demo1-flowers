<template>
  <content-section fluid>
    <template #title>
      <span class="section__title max-width-600">
        Find your favorite flower
      </span>
    </template>
    <v-form>
      <div class="section__form">
        <v-container class="max-width-600">
          <v-label>
            <span class="white--text">
              <h3 class="mb-3 ml-3">
                Name
              </h3>
            </span>
          </v-label>
          <v-text-field solo label="Sunflower, rose, margarita" />
          <v-label>
            <span class="white--text">
              <h3 class="mb-3 ml-3">
                Color
              </h3>
            </span>
          </v-label>
          <v-text-field solo label="Yellow, blue, red" />
        </v-container>
      </div>
      <div class="d-flex justify-center">
        <v-btn x-large color="primary" class="mt-5">
          Search
        </v-btn>
      </div>
    </v-form>
  </content-section>
</template>

<script>
import ContentSection from './ContentSection.vue'

export default {
  components: {
    ContentSection
  }
}
</script>

<style scoped>
.max-width-600 {
  max-width: 600px !important;
}

.section__form {
  position: relative;
  background-image: linear-gradient(
      90deg,
      var(--overlay-color1),
      var(--overlay-color1)
    ),
    url("~/static/compass.jpg");
  background-size: 100% auto;
  background-position-y: center;
}

.section__title {
  display: inline-block;
}
</style>
