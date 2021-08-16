<template>
  <content-section title="Encuentra y reserva el servicio que necesitas">
    <v-form>
      <v-label>Qué</v-label>
      <v-text-field solo label="Nombre del servicio o del proveedor" />
      <v-label>Dónde</v-label>
      <v-text-field solo label="Provincia, municipio, concejo popular" />
      <v-btn>Buscar</v-btn>
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

<style>

</style>
