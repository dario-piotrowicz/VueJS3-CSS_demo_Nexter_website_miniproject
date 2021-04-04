<template>
  <div class="hero">
    <img src="../assets/images/logo.png" alt="Nexter logo" class="hero__logo" />
    <h3 class="hero__sub-title">Your own home:</h3>
    <h1 class="hero__title">The ultimate personal freedom</h1>
    <button class="hero__btn">View our properties</button>
    <div class="hero__as-seen-on-text">As seen on</div>
    <div class="hero__as-seen-on-logos">
      <img
        src="../assets/images/hero/as_seen_on/logo-bbc.png"
        alt="BBC logo"
        class="hero__as-seen-on-logo"
      />
      <img
        src="../assets/images/hero/as_seen_on/logo-forbes.png"
        alt="Forbes logo"
        class="hero__as-seen-on-logo"
      />
      <img
        src="../assets/images/hero/as_seen_on/logo-techcrunch.png"
        alt="TechCrunch logo"
        class="hero__as-seen-on-logo"
      />
      <img
        src="../assets/images/hero/as_seen_on/logo-bi.png"
        alt="Business Insider logo"
        class="hero__as-seen-on-logo"
      />
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import "src/assets/scss/colors";

.hero {
  grid-column: content-start / col-end 6;

  @media only screen and (max-width: 850px) {
    grid-column: 1 / -1;
  }

  background-image: linear-gradient(
      transparentize($secondary-color, 0.07),
      transparentize($secondary-color, 0.07)
    ),
    url("../assets/images/hero/background.jpeg");
  background-size: cover;
  background-position: center;

  padding: 8rem;
  padding-top: 4rem;

  display: grid;
  grid-template-rows: 1fr min-content minmax(6rem, min-content) 1fr;
  grid-template-columns: minmax(min-content, max-content);
  row-gap: 1.5rem;
  justify-content: center;

  &__logo {
    height: 3rem;
    justify-self: center;
  }

  &__sub-title {
    font-family: "Josefin Sans", sans-serif;
    font-size: 1.6rem;
    color: $primary-color;
    font-weight: 400;
    text-transform: uppercase;
  }

  &__title {
    font-family: "Josefin Sans", sans-serif;
    font-size: 4.5rem;
    color: #f9f7f6;
    line-height: 1;
    font-weight: 400;
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
    justify-self: start;
    align-self: start;

    &:hover {
      background-color: #b28451;
    }
  }

  &__as-seen-on-text {
    font-size: 1.6rem;
    color: #aaa;

    &::before,
    &::after {
      content: "";
      height: 1px;
      display: block;
      background-color: currentColor;
    }

    display: grid;
    grid-template-columns: 1fr max-content 1fr;
    align-items: center;
    column-gap: 1.5rem;
  }

  &__as-seen-on-logos {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    column-gap: 3rem;
    justify-items: center;
    align-items: center;
  }

  &__as-seen-on-logo {
    max-height: 2.5rem;
    max-width: 100%;
    filter: brightness(70%);
  }
}
</style>
