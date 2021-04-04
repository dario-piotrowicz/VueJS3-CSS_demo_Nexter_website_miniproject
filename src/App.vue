<template>
  <svg-definitions></svg-definitions>
  <div class="app-container">
    <side-bar></side-bar>
    <hero></hero>
    <realtors></realtors>
    <features></features>
    <story></story>
    <houses></houses>
    <gallery></gallery>
    <app-footer></app-footer>
  </div>
</template>

<script>
import SvgDefs from "./SvgDefs";
import "./assets/fonts/fonts.css";

import Hero from "./components/hero";
import SideBar from "./components/sidebar";
import Realtors from "./components/realtors";
import Features from "./components/features";
import Story from "./components/story";
import Houses from "./components/houses";
import Gallery from "./components/gallery";
import Footer from "./components/footer";

export default {
  name: "App",
  components: {
    "svg-definitions": SvgDefs,
    hero: Hero,
    "side-bar": SideBar,
    realtors: Realtors,
    features: Features,
    story: Story,
    houses: Houses,
    gallery: Gallery,
    "app-footer": Footer,
  },
};
</script>

<style lang="scss">
html {
  box-sizing: border-box;
  font-size: 62.5%;

  @media only screen and (max-width: 1200px) {
    font-size: 50%;
  }
}

* {
  margin: 0;
  padding: 0;
  box-sizing: inherit;
}

body {
  font-family: "Nunito", sans-serif;
  color: #6d5d4b;
  font-weight: 300;
  line-height: 1.6;
}

.app-container {
  display: grid;
  grid-auto-flow: row;
  grid-template-rows: 80vh min-content 40vw repeat(3, min-content);
  grid-template-columns:
    [sidebar-start] 8rem [sidebar-end content-start] minmax(6rem, 1fr)
    [center-start] repeat(8, [col-start] minmax(min-content, 14rem) [col-end])
    [center-end] minmax(6rem, 1fr) [content-end];

  @media only screen and (max-width: 1000px) {
    grid-template-rows: 6rem 80vh min-content 40vw repeat(3, min-content);
    grid-template-columns:
      [content-start] minmax(6rem, 1fr)
      [center-start] repeat(8, [col-start] minmax(min-content, 14rem) [col-end])
      [center-end] minmax(6rem, 1fr) [content-end];
  }
}
</style>
