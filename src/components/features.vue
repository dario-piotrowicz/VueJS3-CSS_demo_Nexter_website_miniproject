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
@import "src/assets/scss/colors";

.features {
  grid-column: center-start / center-end;

  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(25rem, 1fr));
  gap: 6rem;
  align-items: start;

  margin: 15rem 0;
}

.feature {
  display: grid;
  grid-template-columns: min-content 1fr;
  row-gap: 1.5rem;
  column-gap: 2.5rem;

  &__icon {
    fill: $primary-color;
    $size: 4.5rem;
    width: $size;
    height: $size;
    grid-row: 1 / span 2;
    transform: translateY(-1rem);
  }

  &__title {
    font-family: "Josefin Sans", sans-serif;
    font-weight: 400;
    font-size: 1.9rem;
    color: #54483a;
  }

  &__text {
    font-size: 1.7rem;
  }
}
</style>
