<script>
import ntechLogo from '@/assets/images/ntechmultiverse-logo.png'
import NavList from './NavList.vue'
import NavListBiggerScreens from './NavListBiggerScreens.vue'

export default {
  components: {
    NavList,
    NavListBiggerScreens
  },
  data: () => ({
    ntechLogo,
    showNavList: false
  }),
  methods: {
    toggleShowNavList() {
      this.showNavList = !this.showNavList
    },
    closeShowNavList(close) {
      this.showNavList = close
    }
  }
}
</script>

<template>
  <header>
    <div :class="$style.img">
      <button @click="toggleShowNavList"><span class="fa-solid fa-bars"></span></button>
      <img :class="$style['ntech-logo']" :src="ntechLogo" alt="ntech-logo" />
    </div>
    <div :class="$style.contact">
      <p>
        You make the contact, <br />
        we take care of the rest
      </p>
      <div :class="$style.address">
        <div>
          <span class="fa-solid fa-phone"></span>
          <span class="fa-solid fa-envelope"></span>
        </div>
        <address>
          Address: Sheraton Hotel,<br />
          Ladikwali Way, Wuse Zone 4, <br />Abuja, Nigeria.
        </address>
      </div>
    </div>
  </header>
  <NavList v-if="showNavList" @closeNav="closeShowNavList" />
  <NavListBiggerScreens />
</template>

<style module>
header {
  display: flex;
  flex-flow: column nowrap;
  gap: 0.5rem;
  width: 100%;
  max-width: 800px;
  padding: 1.5rem 1rem;
}
header .img {
  display: flex;
  justify-content: center;
  gap: 10%;
  width: 100%;
  font-size: 1.5rem;
}
header .img button span {
  font-size: 1.5rem;
}

.img button {
  display: flex;
  justify-content: center;
  padding: 1rem;
  height: 10px;
  width: 10px;
  border: none;
  background: transparent;
}

.img span {
  color: var(--green);
}

header .ntech-logo {
  object-fit: contain;
  width: 70%;
}
header .contact {
  display: flex;
  flex-flow: column nowrap;
  align-items: center;
}
.contact p {
  font-size: 1.5rem;
  font-family: Georgia, 'Times New Roman', Times, serif;
  color: var(--white);
}
.address {
  color: var(--lightYellow);
  display: flex;
  flex-flow: row nowrap;
  justify-content: space-around;
  align-items: center;
  width: 100%;
}
.address div span {
  font-size: 1.5rem;
  color: var(--white);
}
.address div {
  display: flex;
  flex-flow: column nowrap;
  gap: 1rem;
}

/* Bigger Screens */
@media (min-width: 800px) {
  header {
    display: flex;
    flex-flow: row nowrap;
    justify-content: space-between;
    padding: 1.5rem 0rem;
  }
  header .img {
    width: 40%;
  }

  .img button {
    display: none;
  }

  header .ntech-logo {
    object-fit: contain;
    width: 100%;
    height: 150px;
    margin: auto;
  }
  .address {
    gap: 1rem;
  }
}
</style>
