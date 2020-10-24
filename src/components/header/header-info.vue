<template>
  <div v-for="(info, index) in info" :key="index" class="header-info-component">
    <img :src="info.icon" class="header-icon" alt="info.title" />
    <p class="h-sub-title">{{ info.title }}</p>
    <p>{{ info.description }}</p>
  </div>
</template>

<script>
import icon1 from "../../assets/images/sketch.svg";
import icon2 from "../../assets/images/team.svg";
export default {
  name: "HeaderInfo",
  data() {
    return {
      info: [
        {
          icon: icon1,
          title: "Tailored Approach",
          description:
            "Far far away, behind the word mountains, far from the countries",
        },
        {
          icon: icon2,
          title: "Professional Team",
          description:
            "Far far away, behind the word mountains, far from the countries",
        },
      ],
    };
  },
};
</script>

<style lang="scss" src="../../assets/scss/header/header-cta.scss" scoped></style>
