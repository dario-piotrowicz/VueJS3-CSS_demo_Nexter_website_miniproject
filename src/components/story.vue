<template>
  <section class="story">
    <div class="story__pictures">
      <img
        src="../assets/images/story/couple.jpeg"
        alt="Couple"
        class="story__picture-couple"
      />
      <img
        src="../assets/images/story/house.jpeg"
        alt="House"
        class="story__picture-house"
      />
    </div>
    <div class="story__content">
      <h3 class="story__subtitle">Happy Customers</h3>
      <h2 class="story__title">&ldquo;The best decision of our lives&rdquo;</h2>
      <p class="story__text">
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Tenetur
        distinctio necessitatibus pariatur voluptatibus. Quidem consequatur
        harum volupta!
      </p>
      <button class="story__btn">Find your own home</button>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@import "src/assets/scss/colors";

.story {
  grid-column: content-start / content-end;

  display: flex;

  &__pictures {
    flex: 0 0 50%;
    background-image: linear-gradient(
        rgba($primary-color, 0.5),
        rgba($primary-color, 0.5)
      ),
      url("../assets/images/story/background.jpg");

    display: grid;
    grid-template-columns: repeat(6, 1fr);
    grid-template-rows: repeat(6, 1fr);
    align-items: center;
  }

  &__picture-couple {
    width: 100%;
    grid-row: 2 / 6;
    grid-column: 2 / 6;
    box-shadow: 0 2rem 5rem transparentize(#000, 0.9);
  }

  &__picture-house {
    width: 115%;
    grid-row: 4 / 6;
    grid-column: 4 / 7;
    z-index: 2;
    box-shadow: 0 2rem 5rem transparentize(#000, 0.8);
  }

  &__content {
    flex: 0 0 50%;
    background-color: #f9f7f6;
    padding: 6rem 8vw;

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
  }

  &__subtitle {
    font-family: "Josefin Sans", sans-serif;
    font-weight: 400;
    font-size: 1.6rem;
    color: $primary-color;
    text-transform: uppercase;
    margin-bottom: 2rem;
  }

  &__title {
    font-family: "Josefin Sans", sans-serif;
    font-weight: 400;
    font-size: 4rem;
    font-style: italic;
    color: #54483a;
    line-height: 1;
    margin-bottom: 3rem;
  }

  &__text {
    font-size: 1.5rem;
    font-style: italic;
    margin-bottom: 4rem;
  }

  &__btn {
    background-color: $primary-color;
    color: #fff;
    border: none;
    border-radius: 0;
    outline: none;
    font-family: "Josefin Sans", sans-serif;
    font-size: 1.5rem;
    text-transform: uppercase;
    padding: 1.8rem 3rem;
    cursor: pointer;
    transition: background-color 0.2s;

    &:hover {
      background-color: #b28451;
    }
  }
}
</style>
