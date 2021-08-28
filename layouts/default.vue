<template>
  <v-app>
    <v-app-bar app flat absolute class="bg-transparent z-index-100">
      <v-spacer />
      <v-btn
        v-for="(link, index) in appBarLinks"
        :key="link + index"
        text
        class="text-transform-capitalize"
      >
        {{ link }}
      </v-btn>

      <!-- Login button -->
      <v-btn
        :to="{ name: 'Login' }"
        color="accent"
        class="text-transform-capitalize"
      >
        Iniciar Sesión
      </v-btn>
    </v-app-bar>

    <v-main class="pt-0">
      <v-container fluid class="px-0 py-0">
        <Nuxt />
      </v-container>
    </v-main>

    <base-footer />
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      appBarLinks: [
        'Funcionamiento',
        'Buscar',
        'Servicios',
        'Precios',
        'Para quién',
        'Descargar'
      ],
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      title: 'Vuetify.js'
    }
  }
}
</script>

<style lang="scss">
@import "vueperslides/dist/vueperslides.css";

.z-index-100 {
  z-index: 100 !important;
}

.bg-transparent {
  background-color: transparent !important;
}

.text-transform-capitalize {
  text-transform: capitalize !important;
}
</style>
