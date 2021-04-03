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
.houses {
  grid-column: center-start / center-end;

  margin: 15rem 0;

  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(25rem, 1fr));
  gap: 7rem;
}

.house {
  background-color: #f9f7f6;

  &__image {
    width: 100%;
  }
}
</style>
