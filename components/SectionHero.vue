<template>
  <content-section class="section-hero">
    <v-container>
      <v-row class="z-index-10">
        <v-col cols="12" sm="6" class="d-flex flex-column justify-center">
          <h1 class="text-uppercase section-hero__title">
            Flowers
          </h1>
          <p>
            Flowers are beautiful and make our lives rich. The colors and smells
            really add to what we love.
            We sell flowers in their own vessel for you to help it grow.
            Want to have your own flower?
          </p>
          <div class="d-flex">
            <v-btn color="primary align-self-center" x-large>
              Get your flower
            </v-btn>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </content-section>
</template>

<script>
export default {
  name: 'SectionHero'
}
</script>

<style scoped>
* {
  z-index: 20;
}

.section-hero {
  position: relative;
  overflow: hidden;
  background-image: linear-gradient(
      90deg,
      var(--overlay-color4) 60%,
      var(--overlay-color5)
    ),
    url("~/static/office.jpg");
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
  left: -20em;
  bottom: -20em;
  border-top: 15px solid var(--border) !important;
  background-color: var(--color-quaternary);
}

@media screen and (min-width: 600px) {
  .section-hero::before {
    left: -50em;
  }
}

@media screen and (min-width: 960px) {
  .section-hero::before {
    height: 100em;
    width: 200em;
    left: -40em;
    bottom: -90em;
  }
}

.section-hero::after {
  z-index: 10;
  height: 40em;
  width: 60em;
  transform: rotate(-35deg);
  background-color: var(--color-tertiary);
  right: -20em;
  bottom: -35em;
  background: linear-gradient(
    180deg,
    rgba(34, 110, 186, 0.4) 4%,
    rgba(16, 69, 124, 1) 4%
  );
}

@media screen and (min-width: 960px) {
  .section-hero::after {
    height: 50em;
  }
}

.section-hero__title {
  color: var(--color-primary);
  font-size: 3.8rem;
}
.text-uppercase {
  text-transform: uppercase;
}

.circle__wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
}

.circle {
  position: relative;
  width: 80%;
  padding-top: 80%;
  border-radius: 50%;
  justify-content: center;
  align-items: center;
  border: 5px solid var(--color-quaternary);
  box-shadow: var(--shadow-color1) 0px 7px 29px 0px;
}

.circle__img {
  position: absolute;
  top: 40%;
  right: 28%;
  width: 50%;
}

.circle:before {
  content: " ";
  position: absolute;
  border-radius: inherit;
  z-index: -1;
  top: 40px;
  left: 40px;
  right: 40px;
  bottom: 40px;
  border: 5px solid var(--color-quaternary);
  box-shadow: var(--shadow-color1) 0px 7px 29px 0px;
}

.circle:after {
  background-color: var(--color-primary);
  content: " ";
  position: absolute;
  border-radius: inherit;
  z-index: -1;
  top: 80px;
  left: 80px;
  right: 80px;
  bottom: 80px;
}
</style>
