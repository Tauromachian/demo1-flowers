<template>
  <content-section>
    <v-row>
      <v-col cols="6">
        <h1 class="text-uppercase section-hero__title">
          Ticket
        </h1>
        <p>
          Es la forma más fácil y rápida de gestionar su agenda de servicios.
          Convierta su nuevo cliente en un cliente habitual, ofreciendo atención
          diferenciada y sin hacerlo esperar
        </p>
        <div class="d-flex justify-center">
          <v-btn color="primary align-self-center">
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
  </content-section>
</template>

<script>
export default {}
</script>

<style scoped>
.section-hero__title {
  color: #185596;
  font-size: 3.8rem;
}
.text-uppercase {
  text-transform: uppercase;
}

.circle-outer, .circle-middle {
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
