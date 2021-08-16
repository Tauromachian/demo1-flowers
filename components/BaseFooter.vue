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
        <v-col
          cols="3"
          class="pr-3"
        >
          <h1>Ticket</h1>
          <p>
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Rem odit quis voluptatem.
          </p>
        </v-col>

        <v-col
          cols="3"
          class="px-3"
        >
          <h3 class="mb-5">
            Síguenos en
          </h3>
          <v-btn icon>
            <v-icon>
              mdi-twitter
            </v-icon>
          </v-btn>
          <v-btn icon>
            <v-icon>
              mdi-instagram
            </v-icon>
          </v-btn>
          <v-btn icon>
            <v-icon>
              mdi-facebook
            </v-icon>
          </v-btn>
        </v-col>

        <v-col
          cols="3"
          class="px-3"
        >
          <h3 class="mb-5">
            Contactos
          </h3>
          <p>Correo electrónico</p>
          <p>Teléfono</p>
        </v-col>

        <v-col
          cols="3"
          class="d-flex flex-column justify-center pl-3"
        >
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
    <v-container
      fluid
      class="footer__copyright py-6 container"
    >
      <v-row

        align-content="center"
      >
        <v-col
          class="text-center"
          cols="12"
        >
          Copyright &copy; {{ (new Date()).getFullYear() }} Ticket Todos los derechos reservados
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
    social: [
      // 'Facebook',
      // 'Twitter',
      // 'Instagram',
      // 'Linkedin',
    ]
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
  background-color:RGB(0, 191, 165, 0.4) !important;
}

.container {
  z-index: 10;
}

.footer {
  background-color: #185596 !important;
  overflow: hidden;
}

.footer__copyright {
  background-color: rgba(17, 81, 145, 0.7);
}

.footer::before {
  content: '';
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
