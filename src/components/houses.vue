<template>
  <section class="houses">
    <div v-for="house of houses" :key="house.name" class="house">
      <img
        :src="house.imgSrc"
        :alt="`Picture of '${house.name}'`"
        class="house__image"
      />
      <h5 class="house__name">{{ house.name }}</h5>
      <div class="house__location">
        <svg class="house__location-icon">
          <use :xlink:href="`#icon-map-pin`"></use>
        </svg>
        <p class="house__location-text">{{ house.location }}</p>
      </div>
      <div class="house__rooms">
        <svg class="house__rooms-icon">
          <use :xlink:href="`#icon-profile-male`"></use>
        </svg>
        <p class="house__rooms-text">{{ house.rooms }} rooms</p>
      </div>
      <div class="house__area">
        <svg class="house__area-icon">
          <use :xlink:href="`#icon-expand`"></use>
        </svg>
        <p class="house__area-text">{{ house.area }} m<sup>2</sup></p>
      </div>
      <div class="house__price">
        <svg class="house__price-icon">
          <use :xlink:href="`#icon-key`"></use>
        </svg>
        <p class="house__price-text">{{ house.price }}</p>
      </div>
      <button class="house__btn">Contact Realtor</button>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      houses: [
        {
          imgSrc: require("../assets/images/houses/house-1.jpeg"),
          name: "Beautiful Family House",
          location: "USA",
          rooms: 5,
          area: 325,
          price: "$1,200,000",
        },
        {
          imgSrc: require("../assets/images/houses/house-2.jpeg"),
          name: "Modern Glass Villa",
          location: "Canada",
          rooms: 6,
          area: 450,
          price: "$2,750,000",
        },
        {
          imgSrc: require("../assets/images/houses/house-3.jpeg"),
          name: "Cozy Country House",
          location: "UK",
          rooms: 4,
          area: 250,
          price: "$850,000",
        },
        {
          imgSrc: require("../assets/images/houses/house-4.jpeg"),
          name: "Large Rustical Villa",
          location: "Portugal",
          rooms: 6,
          area: 480,
          price: "$1,950,000",
        },
        {
          imgSrc: require("../assets/images/houses/house-5.jpeg"),
          name: "Majestic Palace House",
          location: "Germany",
          rooms: 18,
          area: 4230,
          price: "$9,500,000",
        },
        {
          imgSrc: require("../assets/images/houses/house-6.jpeg"),
          name: "Modern Familiy Apartment",
          location: "Italy",
          rooms: 3,
          area: 180,
          price: "$600,000",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "src/assets/scss/colors";

.houses {
  grid-column: center-start / center-end;

  margin: 15rem 0;

  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(25rem, 1fr));
  gap: 7rem;
}

.house {
  background-color: #f9f7f6;

  display: grid;
  grid-template-columns: repeat(2, 1fr);
  row-gap: 2.8rem;

  &__image {
    width: 100%;
    grid-row: 1 / 2;
    grid-column: 1 / -1;
  }

  &__name {
    grid-row: 1 / 2;
    grid-column: 1 / -1;
    justify-self: center;
    align-self: end;
    font-family: "Josefin Sans", sans-serif;
    font-size: 1.6rem;
    font-weight: 400;
    text-align: center;
    padding: 1.25rem;
    color: #fff;
    background-color: $secondary-color;
    width: 80%;
    transform: translateY(50%);
  }

  &__location,
  &__rooms {
    margin-top: 2.5rem;
  }

  &__location,
  &__rooms,
  &__area,
  &__price {
    margin-left: 2rem;
    display: flex;
    align-items: center;

    &-icon {
      fill: $primary-color;
      $size: 2rem;
      height: $size;
      width: $size;
      margin-right: 1rem;
    }

    &-text {
      font-size: 1.5rem;
    }
  }

  &__btn {
    grid-column: 1 / -1;
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
