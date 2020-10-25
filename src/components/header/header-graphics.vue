<template>
  <div class="h-graphics-container">
    <img :src="img" alt="" srcset="" />
    <div class="h-testimony">
      <p>
        “Far far away, behind the word mountains, far from the countries Vokalia
        and Consonantia, there live the blind texts. Separated they live in
        Bookmarksgrove.”
      </p>
      <p class="title">Daniel Haughton <br> CEO at DH Clothing LTD </p>
    </div>
      <div class="bg-shape"></div>
  </div>

</template>

<script>
import heroPic from "../../assets/images/hero_1.jpg";
export default {
  name: "HeaderGraphics",
  data() {
    return {
      img: heroPic,
    };
  },
};
</script>

<style lang="scss" src="../../assets/scss/header/header-graphics.scss" scoped></style>
