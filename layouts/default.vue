<template>
  <v-app>
    <v-app-bar app />

    <v-main>
      <v-container>
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
