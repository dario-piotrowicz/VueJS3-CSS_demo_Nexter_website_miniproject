<template>
  <div class="side-bar"></div>
</template>

<style lang="scss" scoped>
@import "src/assets/scss/colors";

.side-bar {
  background-color: $primary-color;
  grid-column: sidebar-start / sidebar-end;
  grid-row: 1 / -1;
}
</style>
