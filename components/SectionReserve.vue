<template>
  <content-section fluid>
    <template #title>
      <span class="section__title max-width-600">
        Encuentra y reserva el servicio que necesitas
      </span>
    </template>
    <v-form>
      <div class="blue">
        <v-container class="max-width-600">
          <v-label>
            <span class="white--text">
              <h3 class="mb-3 ml-3">
                Qué
              </h3>
            </span>
          </v-label>
          <v-text-field solo label="Nombre del servicio o del proveedor" />
          <v-label>
            <span class="white--text">
              <h3 class="mb-3 ml-3">
                Dónde
              </h3>
            </span>
          </v-label>
          <v-text-field solo label="Provincia, municipio, concejo popular" />
        </v-container>
      </div>
      <div class="d-flex justify-center">
        <v-btn x-large color="primary" class="mt-5">
          Buscar
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

.section__title {
  display: inline-block;
}
</style>
