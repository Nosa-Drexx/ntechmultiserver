<script>
import work from '@/assets/images/work.jpg'
export default {
  data: () => ({
    work
  })
}
</script>

<template>
  <section :class="$style['about-us']" id="About-us">
    <h1 :class="$style.h1">About Us</h1>
    <div :class="$style.about">
      <div :class="$style.text">
        <h2 :class="$style.h2">Company Overview</h2>
        <p :class="$style.p">
          Ntech Multiserve Limited is number one in providing innovative and professional solutions
          to your projects in logistics, computer services, event management, catering, and road
          side assistance. With our HQ based in Abuja we cover all states in the entire Nigeria.
        </p>
        <p :class="$style.p">
          We are a Nigerian multiservice IT and logistics company with businesses and interests that
          covers various sectors of the Nigerian economy from Information technology solutions to
          first-class transportation, foods & catering, event management, tow and crane,
          construction, and maintenance. With globally respected partners and an iconic brand
          portfolio, Ntech Multiserve Ltd has continued to be a considerable contributor to
          Nigeria's economy. Ntech Multiserve Ltd was founded in 2010 with the intention to be the
          number one leading professional multiservice company in Nigeria delivering excellent
          world-class services to her customers, giving them the highest value for their money while
          contributing to societal development and progress.
        </p>
      </div>
      <img :src="work" :class="$style.img" />
    </div>
  </section>
</template>
<style module>
.about-us {
  width: 100%;
  max-width: 800px;
  padding: 1rem;
  color: var(--white);
}
.h1 {
  font-size: 3rem;
  font-family: 'Courier New', Courier, monospace;
}
.about {
  display: flex;
  flex-flow: column nowrap;
}
.text {
  font-size: 1.2rem;
  margin: 1rem;
  display: flex;
  flex-flow: column nowrap;
  gap: 1rem;
}
.img {
  margin: auto;

  width: 70%;
  height: 200px;
  object-fit: cover;
}
@media (min-width: 800px) {
  .about {
    display: flex;
    flex-flow: row nowrap;
  }
  .text {
    width: 55%;
  }
  .img {
    margin: none;
    align-self: flex-start;
    width: 40%;
    height: 250px;
  }
}
</style>
