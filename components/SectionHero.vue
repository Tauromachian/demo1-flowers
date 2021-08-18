<template>
  <content-section class="section-hero">
    <v-container>
      <v-row class="z-index-10">
        <v-col cols="6">
          <h1 class="text-uppercase section-hero__title">
            Ticket
          </h1>
          <p>
            Es la forma más fácil y rápida de gestionar su agenda de servicios.
            Convierta su nuevo cliente en un cliente habitual, ofreciendo
            atención diferenciada y sin hacerlo esperar
          </p>
          <div class="d-flex">
            <v-btn color="primary align-self-center" x-large>
              Registre su negocio
            </v-btn>
          </div>
          <v-btn text>
            Y pruebe gratis por 15 días
          </v-btn>
        </v-col>
        <v-col cols="6">
          <div class="circle-outer">
            <div class="circle-middle">
              <div class="circle-inner">
                <p>
                  Ticket
                </p>
              </div>
            </div>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </content-section>
</template>

<script>
export default {}
</script>

<style scoped>
* {
  z-index: 20;
}

.section-hero {
  position: relative;
  overflow: hidden;
}

.section-hero::before,
.section-hero::after {
  content: "";
  display: block;
  position: absolute;
}

.section-hero::before {
  z-index: 10;
  height: 40em;
  width: 60em;
  transform: rotate(-35deg);
  background-color: #226eba;
  right: -20em;
  bottom: -35em;
  background: linear-gradient(
    180deg,
    rgba(34, 110, 186, 0.4) 4%,
    rgba(16, 69, 124, 1) 4%
  );
}

.section-hero::after {
  z-index: 0;
  height: 40em;
  width: 80em;
  transform: rotate(28deg);
  background-color: rgb(233, 227, 227);
  left: -10em;
  bottom: -20em;
  background: linear-gradient(
    180deg,
    rgba(151, 151, 151, 0.4) 3%,
    rgb(233, 227, 227) 3%
  );
}

.section-hero__title {
  color: #185596;
  font-size: 3.8rem;
}
.text-uppercase {
  text-transform: uppercase;
}

.circle-outer,
.circle-middle {
  border-radius: 50%;
  opacity: 1;
  height: 100%;
  width: auto;
  border: 1px solid black;
}

.circle-outer {
  display: flex;
  justify-content: center;
  align-items: center;
}

.circle-middle {
  height: 80%;
  padding: 3em;
}

.circle-inner {
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 50%;
  background-color: #185596;
  text-align: center;
  height: 100%;
  width: 100%;
}
</style>
