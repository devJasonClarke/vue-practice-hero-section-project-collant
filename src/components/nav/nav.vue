<template>
  <nav>
    <p class="logo">Collant</p>
    <NavLinks />
    <a href="#" class="login">Sign up / Login</a>
  </nav>
</template>

<script>
import NavLinks from "./nav-links";
export default {
  name: "Nav",
  components: {
    NavLinks,
  },
};
</script>

<style lang="scss" src="../../assets/scss/nav/nav.scss" scoped>

</style>
