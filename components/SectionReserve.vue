<template>
  <content-section title="Encuentra y reserva el servicio que necesitas" fluid>
    <div class="blue">
      <v-container>
        <v-form>
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
          <div class="d-flex justify-center">
            <v-btn>
              Buscar
            </v-btn>
          </div>
        </v-form>
      </v-container>
    </div>
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
