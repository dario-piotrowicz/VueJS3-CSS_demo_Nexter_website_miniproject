<template>
  <section class="gallery">
    <div class="gallery__item--01">
      <img
        src="../assets/images/gallery/01.jpeg"
        alt="gallery item 1"
        class="gallery__image"
      />
    </div>
    <div class="gallery__item--02">
      <img
        src="../assets/images/gallery/02.jpeg"
        alt="gallery item 2"
        class="gallery__image"
      />
    </div>
    <div class="gallery__item--03">
      <img
        src="../assets/images/gallery/03.jpeg"
        alt="gallery item 3"
        class="gallery__image"
      />
    </div>
    <div class="gallery__item--04">
      <img
        src="../assets/images/gallery/04.jpeg"
        alt="gallery item 4"
        class="gallery__image"
      />
    </div>
    <div class="gallery__item--05">
      <img
        src="../assets/images/gallery/05.jpeg"
        alt="gallery item 5"
        class="gallery__image"
      />
    </div>
    <div class="gallery__item--06">
      <img
        src="../assets/images/gallery/06.jpeg"
        alt="gallery item 6"
        class="gallery__image"
      />
    </div>
    <div class="gallery__item--07">
      <img
        src="../assets/images/gallery/07.jpeg"
        alt="gallery item 7"
        class="gallery__image"
      />
    </div>
    <div class="gallery__item--08">
      <img
        src="../assets/images/gallery/08.jpeg"
        alt="gallery item 8"
        class="gallery__image"
      />
    </div>
    <div class="gallery__item--09">
      <img
        src="../assets/images/gallery/09.jpeg"
        alt="gallery item 9"
        class="gallery__image"
      />
    </div>
    <div class="gallery__item--10">
      <img
        src="../assets/images/gallery/10.jpeg"
        alt="gallery item 10"
        class="gallery__image"
      />
    </div>
    <div class="gallery__item--11">
      <img
        src="../assets/images/gallery/11.jpeg"
        alt="gallery item 11"
        class="gallery__image"
      />
    </div>
    <div class="gallery__item--12">
      <img
        src="../assets/images/gallery/12.jpeg"
        alt="gallery item 12"
        class="gallery__image"
      />
    </div>
    <div class="gallery__item--13">
      <img
        src="../assets/images/gallery/13.jpeg"
        alt="gallery item 13"
        class="gallery__image"
      />
    </div>
    <div class="gallery__item--14">
      <img
        src="../assets/images/gallery/14.jpeg"
        alt="gallery item 14"
        class="gallery__image"
      />
    </div>
  </section>
</template>

<style lang="scss" scoped>
.gallery {
  background-color: #f9f7f6;
  grid-column: content-start / content-end;

  display: grid;
  grid-template-columns: repeat(8, 1fr);
  grid-template-rows: repeat(7, 5vw);
  gap: 1.5rem;
  padding: 1.5rem;

  &__item {
    &--01 {
      grid-row: 1 / span 2;
      grid-column: 1 / span 2;
    }
    &--02 {
      grid-row: 1 / span 3;
      grid-column: 3 / span 3;
    }
    &--03 {
      grid-row: 1 / span 2;
      grid-column: 6 / span 1;
    }
    &--04 {
      grid-row: 1 / span 2;
      grid-column: 7 / span 2;
    }
    &--05 {
      grid-row: 3 / span 3;
      grid-column: 1 / span 2;
    }
    &--06 {
      grid-row: 4 / span 2;
      grid-column: 3 / span 2;
    }
    &--07 {
      grid-row: 4 / span 1;
      grid-column: 5 / span 1;
    }
    &--08 {
      grid-row: 3 / span 2;
      grid-column: 6 / span 2;
    }
    &--09 {
      grid-row: 3 / span 3;
      grid-column: 8 / span 1;
    }
    &--10 {
      grid-row: 6 / span 2;
      grid-column: 1 / span 1;
    }
    &--11 {
      grid-row: 6 / span 2;
      grid-column: 2 / span 2;
    }
    &--12 {
      grid-row: 6 / span 2;
      grid-column: 4 / span 1;
    }
    &--13 {
      grid-row: 5 / span 3;
      grid-column: 5 / span 3;
    }
    &--14 {
      grid-row: 6 / span 2;
      grid-column: 8 / span 1;
    }
  }

  &__image {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
}
</style>
