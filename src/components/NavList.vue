<script>
export default {
  data: () => ({
    navList: ['Home', 'About-us', 'IT-solutions', '+ Transportation', 'Event & Catering', 'Towing']
  }),
  methods: {
    async closeNav() {
      //Wait for animation for emiting false to close nav
      await new Promise((resolve) => {
        this.$refs.nav.style.left = '-60vw'
        this.$refs.nav.style.opacity = '0'
        setTimeout(() => {
          resolve()
        }, 500)
      })
      return this.$emit('closeNav', false)
    }
  }
}
</script>

<template>
  <nav :class="$style.nav" ref="nav">
    <button @click="closeNav"><span class="fa-solid fa-x"></span></button>
    <ul>
      <li :class="$style.list" v-for="list in navList" :key="list">
        <a :href="`#${list}`">{{ list }}</a>
      </li>
    </ul>
  </nav>
</template>

<style module>
.nav {
  display: flex;
  flex-flow: column nowrap;
  gap: 5%;
  position: fixed;
  padding: 20px 10px;
  top: 0;
  left: 0;
  height: 100vh;
  width: 60vw;
  opacity: 1;
  background: var(--gray);
  transition: left 0.5s, opacity 0.3s;
  animation-name: slide;
  animation-duration: 0.5s;
}

@keyframes slide {
  from {
    left: -60vw;
  }
  to {
    left: 0;
  }
}
.nav ul {
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
}
.nav button {
  width: 30px;
  height: 30px;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 1.3rem;
  background: none;
  border: 1px solid var(--lightGray);
}
.nav span {
  font-size: 1.5rem;
  color: var(--red);
}
.list {
  list-style-type: none;
  font-size: 1.5rem;
  width: 100%;
  padding: 1rem 5px;
  border-bottom: 1px solid var(--white);
}
.list:last-child {
  border-bottom: none;
}
.list a {
  text-decoration: none;
  color: var(--white);
}
</style>
