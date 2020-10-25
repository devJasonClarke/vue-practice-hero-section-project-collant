<template>
  <div class="main-container">
    <Nav />
    <Header />
    <HowItWorks />
  </div>
</template>

<script>
import Nav from "./components/nav/nav";
import Header from "./components/header/header";
import HowItWorks from './components/how-it-works/sec-1';
export default {
  name: "App",
  components: {
    Nav,
    Header,
    HowItWorks
  },
};
</script>

<style lang="scss" src="./assets/scss/index.scss"></style>
