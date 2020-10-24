<template>
  <section class="header-stats-container">
    <div v-for="stat in stats" :key="stat.title" class="stats-container">
      <p class="percent">{{stat.percent}}</p>
      <p class="rating">{{stat.title}}</p>
      <p class="description">{{stat.description}}</p>
    </div>
  </section>
</template>

<script>
export default {
  name: "HeaderStats",
  data() {
    return {
      stats: [
             {
          percent: "1,100+",
          title: "Happy Clients",
          description: "A short description of the product.",
        },
        {
          percent: "92%",
          title: "Clients rate us 4.5+ starts ",
          description: "A short description of the product.",
        },
             {
          percent: "24/7",
          title: "Support available",
          description: "A short description of the product.",
        },
             {
          percent: "1M",
          title: "People reached",
          description: "A short description of the product.",
        }
      ],
    };
  },
};
</script>

<style
  lang="scss"
  src="../../assets/scss/header/header-stats.scss"
  scoped
></style>
