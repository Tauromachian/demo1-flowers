<template>
  <v-footer
    id="home-footer"
    dark
    min-height="72"
    :app="app"
    class="pt-16 px-0 pb-0 footer"
  >
    <v-container class="container pb-10">
      <v-row>
        <v-col md="4" cols="12" class="pr-3">
          <h1 class="footer__title">
            Flowers
          </h1>
          <p>
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Rem odit
            quis voluptatem.
          </p>
        </v-col>

        <v-col md="4" sm="6" cols="12" class="px-3">
          <h3>
            Contacts
          </h3>
          <p>Mail: somemail@mail.mail</p>
          <p>Phone: +535456778</p>
        </v-col>

        <v-spacer />

        <v-col md="4" sm="6" cols="12" class="px-3 social-buttons">
          <v-btn
            v-for="(socialButton, index) in social"
            :key="socialButton + index"
            icon
            class="mx-5"
          >
            <v-icon color="accent" class="social-button">
              {{ "mdi-" + socialButton }}
            </v-icon>
          </v-btn>
        </v-col>
      </v-row>
    </v-container>
    <v-container fluid class="footer__copyright py-6 container">
      <v-row align-content="center">
        <v-col class="text-center" cols="12">
          Copyright &copy; {{ new Date().getFullYear() }} Flower all rights reserved
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
.footer__title {
  font-size: 4rem;
  margin-top: -0.6em;
  color: var(--accent2);
}

.social-button {
  font-size: 60px !important;
}

h3 {
  color: var(--accent2);
}

p {
  margin-bottom: 0;
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
  background-color: var(--accent2);
  right: 0;
  bottom: -33em;
  border-top: 2.4em solid var(--border2) !important;
  opacity: 0.7;
}

.social-buttons {
  text-align: center;
  margin-bottom: 2em;
  margin-top: 2em;
}
</style>
