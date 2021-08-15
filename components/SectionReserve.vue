<template>
  <content-section title="Encuentra y reserva el servicio que necesitas">
    <v-form>
      <v-text-field label="Qué" />
      <v-text-field label="Dónde" />
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
