<template>
  <footer class="footer">
    <ul class="footer__nav">
      <li class="footer__nav-item">
        <a href="#" class="footer__nav-link">Find your dream home</a>
      </li>
      <li class="footer__nav-item">
        <a href="#" class="footer__nav-link">Request proposal</a>
      </li>
      <li class="footer__nav-item">
        <a href="#" class="footer__nav-link">Download home planner</a>
      </li>
      <li class="footer__nav-item">
        <a href="#" class="footer__nav-link">Contact us</a>
      </li>
      <li class="footer__nav-item">
        <a href="#" class="footer__nav-link">Submit your property</a>
      </li>
      <li class="footer__nav-item">
        <a href="#" class="footer__nav-link">Where to find us</a>
      </li>
    </ul>
    <p class="footer__copyright">
      &copy; Copyright 2021 by Dario Piotrowicz following Jonas Schmedtmann
      design. Feel free to use this project for your own purposes. This does NOT
      apply if you plan to produce your own course or tutorials based on this
      project.
    </p>
  </footer>
</template>

<style lang="scss" scoped>
@import "src/assets/scss/colors";

.footer {
  grid-column: content-start / content-end;

  background-color: $secondary-color;
  padding: 8rem;

  &__nav {
    list-style: none;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(15rem, 1fr));
    gap: 2rem;
    align-items: center;

    @media only screen and (max-width: 1000px) {
      grid-template-columns: repeat(auto-fit, minmax(25vw, 1fr));
    }

    &-link {
      &:link,
      &:visited {
        font-size: 1.4rem;
        color: #fff;
        text-decoration: none;
        text-transform: uppercase;
        font-family: "Josefin Sans", sans-serif;
        text-align: center;
        padding: 1.5rem;
        display: block;
        transition: background-color 0.2s, transform 0.2s;
      }

      &:hover,
      &:active {
        background-color: transparentize(#fff, 0.95);
        transform: translateY(-3px);
      }
    }
  }

  &__copyright {
    color: #aaa;
    font-size: 1.4rem;
    margin: auto;
    margin-top: 6rem;
    text-align: center;
    width: 70%;
  }
}
</style>
