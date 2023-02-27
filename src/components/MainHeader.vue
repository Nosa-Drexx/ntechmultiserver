<script>
import ntechLogo from '@/assets/images/ntechmultiverse-logo.png'
export default {
  data: () => ({
    ntechLogo
  })
}
</script>

<template>
  <header>
    <div :class="$style.img">
      <span class="fa-solid fa-bars"></span>
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
}
.address {
  color: rgb(211, 211, 25);
  display: flex;
  flex-flow: row nowrap;
  justify-content: space-around;
  align-items: center;
  width: 100%;
}
.address div span {
  font-size: 1.5rem;
  color: black;
}
.address div {
  display: flex;
  flex-flow: column nowrap;
}
</style>
