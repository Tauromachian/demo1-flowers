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
            <v-btn color="accent" class="align-self-center" x-large>
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
  color: var(--accent);
  font-size: 3.8rem;
}
.text-uppercase {
  text-transform: uppercase;
}
</style>
