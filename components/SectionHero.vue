<template>
  <content-section class="section-hero">
    <v-container>
      <v-row class="z-index-10">
        <v-col cols="6" class="d-flex flex-column justify-center">
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
          <p>
            Y pruebe gratis por 15 días
          </p>
        </v-col>
        <v-col cols="6">
          <div class="circle" />
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
  background-image:   linear-gradient(90deg, rgba(16, 68, 122, 0.95), rgba(24, 85, 150, 0.8)), url("~/static/office.jpg");
  background-size: 100% auto;
}

.section-hero::before,
.section-hero::after {
  content: "";
  display: block;
  position: absolute;
}

.section-hero::before {
  z-index: 0;
  height: 50em;
  width: 100em;
  transform: rotate(28deg);
  left: -10em;
  bottom: -20em;
  background: linear-gradient(180deg, rgba(151, 151, 151, 0.4) 3%, white 3%);
}

.section-hero::after {
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

.section-hero__title {
  color: #185596;
  font-size: 3.8rem;
}
.text-uppercase {
  text-transform: uppercase;
}

.circle {
  position: relative;
  width: 80%;
  padding-top: 80%;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  border: 5px solid white;
}

.circle:before {
  content: " ";
  position: absolute;
  border-radius: inherit;
  z-index: -1;
  top: 20px;
  left: 20px;
  right: 20px;
  bottom: 20px;
  border: 5px solid white;
}

.circle:after {
  background-color: #185596;
  content: " ";
  position: absolute;
  border-radius: inherit;
  z-index: -1;
  top: 50px;
  left: 50px;
  right: 50px;
  bottom: 50px;
}
</style>
