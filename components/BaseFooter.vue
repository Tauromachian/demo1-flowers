<template>
  <v-footer
    id="home-footer"
    dark
    min-height="72"
    :app="app"
    class="pt-16 px-0 pb-0 footer"
  >
    <v-container class="container">
      <v-row>
        <v-col md="3" cols="12" class="pr-3">
          <h1>Ticket</h1>
          <p>
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Rem odit
            quis voluptatem.
          </p>
        </v-col>

        <v-col md="3" cols="6" class="px-3">
          <h3 class="mb-5">
            Síguenos en
          </h3>
          <v-btn
            v-for="(socialButton, index) in social"
            :key="socialButton + index"
            icon
          >
            <v-icon>
              {{ "mdi-" + socialButton }}
            </v-icon>
          </v-btn>
        </v-col>

        <v-col md="3" cols="6" class="px-3">
          <h3 class="mb-5">
            Contactos
          </h3>
          <p>Correo electrónico</p>
          <p>Teléfono</p>
        </v-col>

        <v-col md="3" cols="12" class="d-flex flex-column justify-center pl-3">
          <v-btn class="mb-2 last-update-btn">
            Fecha: 8-7-2021
          </v-btn>
          <div />
          <v-btn class="mb-2 last-update-btn">
            Hora: 2:00PM
          </v-btn>
          <p class="align-self-center">
            Última actualización
          </p>
        </v-col>
      </v-row>
    </v-container>
    <v-container fluid class="footer__copyright py-6 container">
      <v-row align-content="center">
        <v-col class="text-center" cols="12">
          Copyright &copy; {{ new Date().getFullYear() }} Ticket Todos los
          derechos reservados
        </v-col>
      </v-row>
    </v-container>
    <div class="triangle" />
  </v-footer>
</template>

<script>
export default {
  name: 'HomeFooter',
  props: {
    app: {
      type: Boolean,
      default: false
    }
  },

  data: () => ({
    social: ['twitter', 'instagram', 'facebook']
  })
}
</script>

<style lang="scss" scoped>
h1 {
  font-size: 4rem;
  margin-top: -0.6em;
}

h3 {
  text-transform: uppercase;
}

p {
  font-weight: bold;
}

.last-update-btn {
  background-color: var(--info) !important;
  opacity: 0.7;
}

.container {
  z-index: 10;
}

.footer {
  background: rgb(31, 103, 177);
  background: linear-gradient(
    90deg,
    rgba(31, 103, 177, 1) 6%,
    rgba(7, 46, 89, 1) 89%
  );
  overflow: hidden;
}

.footer__copyright {
  background-color: rgb(7, 46, 89, 0.6);
}

.footer::before {
  content: "";
  display: block;
  position: absolute;
  height: 40em;
  width: 60em;
  transform: skewY(-24deg);
  background-color: #226eba;
  right: 0;
  bottom: -33em;
  border-top: 2.4em solid #10457c !important;
}
</style>
