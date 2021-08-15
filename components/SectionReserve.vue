<template>
  <page-section title="Encuentra y reserva el servicio que necesitas">
    <v-form>
      <v-text-field label="Qué" />
      <v-text-field label="Dónde" />
      <v-btn>Buscar</v-btn>
    </v-form>
  </page-section>
</template>

<script>
import PageSection from './PageSection.vue'

export default {
  components: {
    PageSection
  }
}
</script>

<style>

</style>
