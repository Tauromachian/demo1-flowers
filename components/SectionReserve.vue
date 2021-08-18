<template>
  <content-section title="Encuentra y reserva el servicio que necesitas" fluid>
    <v-form>
      <div class="blue">
        <v-container>
          <v-label>
            <span class="white--text">
              Qué
            </span>
          </v-label>
          <v-text-field solo label="Nombre del servicio o del proveedor" />
          <v-label>
            <span class="white--text">
              Dónde
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
