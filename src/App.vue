<script>
import MainHeader from './components/MainHeader.vue'
export default {
  components: {
    MainHeader
  }
}
</script>

<template>
  <div class="main-container"><MainHeader /></div>
</template>

<style>
*,
*::before,
*::after {
  box-sizing: border-box;
}
html {
  box-sizing: border-box;
}
body {
  margin: 0;
  padding: 0;
  background: white;
}

.main-container {
  display: flex;
  justify-content: center;
  /* align-items: center; */
  width: 100vw;
  height: 100vh;
}
</style>
