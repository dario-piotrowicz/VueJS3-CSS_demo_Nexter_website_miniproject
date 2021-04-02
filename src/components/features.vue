<template>
  <section class="features">
    <div v-for="feature of features" :key="feature.title" class="feature">
      <svg class="feature__icon">
        <use :xlink:href="`#${feature.iconId}`"></use>
      </svg>
      <h4 class="feature__title">{{ feature.title }}</h4>
      <p class="feature__text">{{ feature.text }}</p>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      features: [
        {
          iconId: "icon-global",
          title: "World's best luxury homes",
          text:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Tenetur distinctio necessitatibus pariatur voluptatibus.",
        },
        {
          iconId: "icon-trophy",
          title: "Only the best properties",
          text:
            "Voluptatum mollitia quae. Vero ipsum sapiente molestias accusamus rerum sed a eligendi aut quia.",
        },
        {
          iconId: "icon-map-pin",
          title: "All homes in top locations",
          text:
            "Tenetur distinctio necessitatibus pariatur voluptatibus quidem consequatur harum.",
        },
        {
          iconId: "icon-key",
          title: "New home in one week",
          text:
            "Vero ipsum sapiente molestias accusamus rerum. Lorem, ipsum dolor sit amet consectetur adipisicing elit.",
        },
        {
          iconId: "icon-presentation",
          title: "Top 1% realtors",
          text:
            "Quidem consequatur harum, voluptatum mollitia quae. Tenetur distinctio necessitatibus pariatur voluptatibus.",
        },
        {
          iconId: "icon-lock",
          title: "Secure payments on Nexter",
          text:
            "Pariatur voluptatibus quidem consequatur harum, voluptatum mollitia quae.",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.features {
  grid-column: center-start / center-end;

  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 6rem;

  margin: 15rem 0;
}
</style>
