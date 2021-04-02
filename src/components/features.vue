<template>
  <section class="features">
    <div class="feature">feature 1</div>
    <div class="feature">feature 2</div>
    <div class="feature">feature 3</div>
    <div class="feature">feature 4</div>
    <div class="feature">feature 5</div>
    <div class="feature">feature 6</div>
  </section>
</template>

<style lang="scss" scoped>
.features {
  grid-column: center-start / center-end;

  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 6rem;

  margin: 15rem 0;
}
</style>
