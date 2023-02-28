<script>
export default {
  data: () => ({
    navList: ['Home', 'About-us', 'IT-solutions', 'Transportation', 'More']
  })
  //   methods: {
  //     async closeNav() {
  //       //Wait for animation for emiting false to close nav
  //       await new Promise((resolve) => {
  //         this.$refs.nav.style.left = '-60vw'
  //         this.$refs.nav.style.opacity = '0'
  //         setTimeout(() => {
  //           resolve()
  //         }, 500)
  //       })
  //       return this.$emit('closeNav', false)
  //     }
  //   }
}
</script>

<template>
  <nav :class="$style.nav" ref="nav">
    <!-- <button @click="closeNav"><span class="fa-solid fa-x"></span></button> -->
    <ul>
      <li :class="$style.list" v-for="list in navList" :key="list">
        <a :href="`#${list}`">{{ list }}</a>
      </li>
    </ul>
  </nav>
</template>

<style module>
.nav {
  display: none;
}
@media (min-width: 800px) {
  .nav {
    display: flex;
    flex-flow: row nowrap;
    width: 100%;
    max-width: 800px;
    padding: 20px 0px;
  }
  .nav ul {
    display: flex;
    flex-flow: row nowrap;
    width: 100%;
    margin: 0;
    padding: 0;
    justify-content: space-between;
  }
  .list {
    list-style-type: none;
    width: 17%;
  }
  .list a {
    background: var(--lightGray);
    display: flex;
    justify-content: center;
    align-items: center;
    border: 5px solid var(--white);
    border-radius: 30px;
    width: 100%;
    padding: 0.5rem 1rem;
    font-size: 1.1rem;
    text-align: center;
    color: var(--white);
    text-decoration: none;
    font-family: sans-serif;
    transition: border 0.5s;
  }
}

.list a:hover {
  border: 5px solid var(--lightGray);
}

.list:first-child a {
  color: var(--lemonGreen);
  border-color: var(--lightGray);
}

/* @keyframes slide {
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
  border: 1px solid rgb(146, 141, 141);
}
.nav span {
  font-size: 1.5rem;
  color: red;
}
.list {
  list-style-type: none;
  font-size: 1.5rem;
  width: 100%;
  padding: 1rem 5px;
  border-bottom: 1px solid white;
}
.list:last-child {
  border-bottom: none;
}
.list a {
  text-decoration: none;
  color: white;
} */
</style>
