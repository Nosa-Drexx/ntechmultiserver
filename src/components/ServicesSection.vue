<script>
import Truck from '@/assets/images/truck.jpg'

export default {
  data: () => ({
    Truck
  })
}
</script>

<template>
  <section :class="$style.services">
    <div :class="$style['img-container']">
      <a href="#" :class="$style['services-link']"><img :src="Truck" :class="$style.img" /></a>
      <h2 :class="$style.h2">IT Solutions</h2>
    </div>
    <div :class="$style['img-container']">
      <a href="#" :class="$style['services-link']"><img :src="Truck" :class="$style.img" /></a>
      <h2 :class="$style.h2">First Class Transportation</h2>
    </div>
    <div :class="$style['img-container']">
      <a href="#" :class="$style['services-link']"><img :src="Truck" :class="$style.img" /></a>
      <h2 :class="$style.h2">Event Management and Catering Sevices</h2>
    </div>
    <div :class="$style['img-container']">
      <a href="#" :class="$style['services-link']"><img :src="Truck" :class="$style.img" /></a>
      <h2 :class="$style.h2">Towing</h2>
    </div>
  </section>
</template>

<style module>
.services {
  display: flex;
  flex-flow: column nowrap;
  gap: 1.5rem;
  padding: 1rem;
  margin: 0;
  max-width: 800px;
  width: 100%;
}
.services-link {
  display: flex;
  align-items: center;
  justify-content: center;
  border: 10px solid var(--lightGray);
  border-radius: 10px;
  width: 90%;
  margin: auto;
  height: 200px;
}
.h2 {
  font-size: 1.5rem;
  margin: 0;
  padding: 0;
  color: var(--orange);
  font-family: sans-serif;
  text-transform: capitalize;
  font-weight: bold;
  text-align: center;
}
.img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

@media (min-width: 800px) {
  .services {
    display: flex;
    flex-flow: row nowrap;
    gap: 1.5rem;
    padding: 1rem;
    margin: 0;
    max-width: 800px;
    width: 100%;
  }

  .img-container {
    width: 25%;
    height: 100px;
  }
  .services-link {
    width: 100%;
    height: 100%;
    border: 8px solid var(--lightGray);
  }

  .h2 {
    font-size: 1.1rem;
  }
}
</style>
