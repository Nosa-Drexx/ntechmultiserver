<script></script>

<template>
  <section :class="$style.hero" id="hero">
    <div :class="$style['hero-text']">
      <h1 :class="$style['hero-h1']">Welcome to the right place that boost your business</h1>
      <p :class="$style['hero-p']">
        We are professionals with the best approaches to turning your project into reality.
      </p>
    </div>
    <div :class="$style.slider">
      <v-carousel cycle hide-delimiter-background show-arrows="hover" height="100%">
        <!-- sliders -->
        <v-carousel-item cover>
          <img :class="$style.img" src="https://cdn.vuetifyjs.com/images/cards/docks.jpg" />
        </v-carousel-item>

        <v-carousel-item cover>
          <img :class="$style.img" src="https://cdn.vuetifyjs.com/images/cards/hotel.jpg"
        /></v-carousel-item>

        <v-carousel-item cover>
          <img :class="$style.img" src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
        /></v-carousel-item>
      </v-carousel>
    </div>
  </section>
</template>

<style module>
.hero {
  display: flex;
  flex-flow: row nowrap;
  justify-content: space-between;
  align-self: center;
  width: 100%;
  max-width: 800px;
  padding: 1rem;
}
.slider {
  width: 40%;
  height: 200px;
  display: none;
}
.hero-text {
  display: flex;
  flex-flow: column nowrap;
  width: 100%;
}

.hero-h1,
.hero-p {
  color: var(--white);
  font-size: 1.2rem;
  font-family: Georgia, 'Times New Roman', Times, serif;
  line-height: 2rem;
  margin: 0.5rem;
}
.hero-h1 {
  font-weight: bold;
  font-size: 1.5rem;
  line-height: 2rem;
  text-align: center;
}

/* Bigger Screens */

@media (min-width: 800px) {
  .slider {
    display: flex;
  }
  .hero-text {
    width: 60%;
  }

  .hero-h1,
  .hero-p {
    font-size: 1.5rem;
  }
  .hero-h1 {
    font-size: 2rem;
    line-height: 3rem;
  }
  .img {
    object-fit: cover;
    width: 100%;
    height: 200px;
  }
}
</style>
