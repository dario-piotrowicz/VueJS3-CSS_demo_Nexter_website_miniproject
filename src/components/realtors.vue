<template>
  <section class="realtors">
    <h3 class="realtors__title">Top 3 realtors</h3>
    <div class="realtors__content">
      <template v-for="realtor of realtors" :key="realtor.name">
        <img :src="realtor.pictureSrc" alt="" class="realtors__picture" />
        <div class="realtors__details">
          <h4 class="realtors__name">{{ realtor.name }}</h4>
          <p class="realtors__sold-text">
            {{ realtor.housesSold }} houses sold
          </p>
        </div>
      </template>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      realtors: [
        {
          name: "Erik Fainman",
          housesSold: 245,
          pictureSrc: require("../assets/images/realtors/1.jpeg"),
        },
        {
          name: "Kim Brown",
          housesSold: 212,
          pictureSrc: require("../assets/images/realtors/2.jpeg"),
        },
        {
          name: "Toby Ramsey",
          housesSold: 198,
          pictureSrc: require("../assets/images/realtors/3.jpeg"),
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "src/assets/scss/colors";

.realtors {
  grid-column: col-start 7 / content-end;

  @media only screen and (max-width: 850px) {
    grid-column: 1 / -1;
  }

  background-color: $secondary-color;
  padding: 3rem;
  display: grid;
  align-content: center;
  justify-content: center;
  row-gap: 2rem;

  &__title {
    font-family: "Josefin Sans", sans-serif;
    font-size: 1.6rem;
    color: $primary-color;
    font-weight: 400;
    text-transform: uppercase;
    text-align: center;
  }

  &__content {
    display: grid;
    grid-template-columns: min-content max-content;
    column-gap: 2rem;
    row-gap: 5vh;
    align-items: center;

    @media only screen and (max-width: 850px) {
      grid-template-columns: repeat(3, min-content max-content);
    }
  }

  &__picture {
    width: 7rem;
    border-radius: 50%;

    &:not(:first-of-type) {
      @media only screen and (max-width: 850px) {
        margin-left: 1.5rem;
      }
    }
  }

  &__name {
    font-family: "Josefin Sans", sans-serif;
    font-weight: 400;
    font-size: 1.9rem;
    color: #f9f7f6;
  }

  &__sold-text {
    color: #aaa;
    text-transform: uppercase;
    margin-top: -3px;
  }
}
</style>
