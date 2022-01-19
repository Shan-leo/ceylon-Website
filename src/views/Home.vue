<template>
  <div class="home">
    <Welcome />
    <h1>Explore Places</h1>
    <div class="container">
      <ProvinceCard
        :post="post" 
        v-for="(post, index) in provinces"
        :key="index"
      />
    </div>
  </div>
</template>

<script>
import Welcome from "../components/Welcome.vue";
import ProvinceCard from "../components/ProvinceCard.vue";

export default {
  name: "Home",
  components: {
    Welcome,
    ProvinceCard,
  },

  data() {
    return {
      provinces: [
        {
          title: "Central Province",
          image: "central.jpeg",
          path:'/central'
        },
        {
          title: "Eastern Province",
          image: "eastern.jpg",
          path:'Eastern'
        },
        {
          title: "North Central",
          image: "northcentral.jpg",
          path:'Northcentral'
        },
        {
          title: "Nothern Province",
          image: "northern.jpg",
          path:'Nothern'
        },
        {
          title: "North Western",
          image: "northwestern.jpg",
          path:'Northwestern'
        },
        {
          title: "Sabaragamuwa",
          image: "sabaragamuwa.jpg",
          path:'Sabaragamuwa'
        },
        {
          title: "Southern",
          image: "southern.jpg",
          path:'Southern'
        },
        {
          title: "Uva Province",
          image: "uva.jpg",
          path:'Uva'
        },
        {
          title: "Western",
          image: "western.jpg",
          path:'Western'
        },
      ],
    };
  },
};
</script>

<style scoped>
.container {
  justify-items: center;
  align-items: center;
  margin-top: 1rem;
  display: grid;
  grid-template-columns: auto auto auto;
  padding: 0 10%;
}

@media (max-width: 1080px) {
  .container {
    justify-items: center;
    margin-top: 1rem;
    display: grid;
    grid-template-columns: auto auto;
    padding: 0 10%;
  }
}
@media (max-width: 750px) {
  .container {
    justify-items: center;
    margin-top: 1rem;
    display: grid;
    grid-template-columns: auto;
    padding: 0 10%;
  }
}
</style>
