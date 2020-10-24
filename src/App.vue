<template >
  <div class="main-container">
<Nav />
<Header />
  </div>
</template>

<script>
import Nav from './components/nav/nav';
import Header from './components/header/header';
  export default {
    name: 'App',
components: {
  Nav, Header
},
  }
</script>

<style lang="scss"  src="./assets/scss/index.scss" >

</style>