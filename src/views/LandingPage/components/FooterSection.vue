<script></script>

<template>
  <footer :class="$style.footer">
    <a :class="$style.facebook" href="#">
      <span class="fa-brands fa-facebook-f" :class="$style['facebook-icon']"></span>
    </a>
    <p :class="$style.p">&copy; 2018 Proudly created by Ntech Multiserve Limited.</p>
  </footer>
</template>

<style module>
.footer {
  background: var(--blue);
  width: 100%;
  display: flex;
  flex-flow: column nowrap;
  justify-content: center;
  align-items: center;
  gap: 2rem;
  border: none;
}
.p {
  font-size: 1.2rem;
  color: var(--white);
}
.facebook {
  display: block;
}
.facebook-icon {
  font-size: 3rem;
  color: var(--white);
}
</style>
