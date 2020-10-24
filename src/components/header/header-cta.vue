<template>
  <div class="center">
    <div class="header-cta-container">
      <h1 class="header-text-large">
       Your brand is our business.
      </h1>
      <p>
        Far far away, behind the word mountains, far from the countries Vokalia
        and Consonantia, there live the blind texts. Separated they live in
        Bookmarksgrove right at the coast of the Semantics, a large language
        ocean.
      </p>
      <a href="#stats" class="login">Learn More</a>
    </div>
    <div class="header-info-container">
      <HeaderInfo />
    </div>
  </div>
</template>

<script>
//import image from '../../assets/images/globe-americas.svg';

import HeaderInfo from "./header-info";
export default {
  name: "HeaderCta",
  components: {
    HeaderInfo,
  }
};
</script>

<style lang="scss" src="../../assets/scss/header/header-cta.scss" scoped></style>
