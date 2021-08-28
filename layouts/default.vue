<template>
  <v-app>
    <v-app-bar
      app
      flat
      absolute
      class="bg-transparent z-index-100 d-none d-sm-block"
    >
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

    <base-footer class="footer" />

    <v-bottom-navigation
      class="z-index-100 d-sm-none"
      fixed
      color="primary"
      horizontal
    >
      <v-btn
        v-for="(link, index) in appBarLinks"
        :key="link + index"
        text
        class="text-transform-capitalize"
      >
        {{ link }}
      </v-btn>
      <v-btn
        :to="{ name: 'Login' }"
        color="accent"
        class="text-transform-capitalize"
      >
        Iniciar Sesión
      </v-btn>
    </v-bottom-navigation>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      appBarLinks: ['Home', 'Flowers', 'Search']
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

.footer {
  margin-bottom: 56px;
}

@media screen and (min-width: 600px) {
.footer {
  margin-bottom: 0;
}
}
</style>
