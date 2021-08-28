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
        <v-col md="4" cols="12" class="pr-3">
          <h1>Ticket</h1>
          <p>
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Rem odit
            quis voluptatem.
          </p>
        </v-col>

        <v-col md="3" cols="6" class="px-3">
          <h3 class="mb-5">
            Contacts
          </h3>
          <p>Mail</p>
          <p>Phone</p>
        </v-col>

        <v-spacer />

        <v-col md="3" cols="6" class="px-3">
          <v-btn
            v-for="(socialButton, index) in social"
            :key="socialButton + index"
            icon
            x-large
          >
            <v-icon x-large color="accent">
              {{ "mdi-" + socialButton }}
            </v-icon>
          </v-btn>
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
  text-transform: capitalize;
}

.container {
  z-index: 10;
}

.footer {
  background: linear-gradient(
    90deg,
    var(--color-quaternary) 6%,
    var(--color-primary) 89%
  );
  overflow: hidden;
}

.footer__copyright {
  background-color: var(--color-primary);
  opacity: 0.6;
}

.footer::before {
  content: "";
  display: block;
  position: absolute;
  height: 40em;
  width: 60em;
  transform: skewY(-24deg);
  background-color: var(--color-tertiary);
  right: 0;
  bottom: -33em;
  border-top: 2.4em solid var(--border2) !important;
}
</style>
