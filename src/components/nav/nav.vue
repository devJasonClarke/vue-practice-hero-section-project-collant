<template>
  <nav>
    <p class="logo">Collant</p>
    <NavLinks />
    <SignIn />
  </nav>
</template>

<script>
import NavLinks from "./nav-links";
import SignIn from './signIn';
export default {
  name: "Nav",
  components: {
    NavLinks,
    SignIn
  },
};
</script>

<style lang="scss" src="../../assets/scss/nav/nav.scss" scoped>

</style>
