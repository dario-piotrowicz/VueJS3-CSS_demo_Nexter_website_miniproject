<template>
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

#app {
}
</style>
