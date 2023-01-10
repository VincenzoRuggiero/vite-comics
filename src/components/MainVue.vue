<template>
  <div class="jumbotron"></div>
  <div class="container">
    <div class="banner">CURRENT SERIES</div>
    <div class="comicsList">
      <ComicsComp
        v-for="item in items"
        :imgPath="item.thumb"
        :price="item.price"
        :series="item.series" />
      <a href="#">Load More</a>
    </div>
  </div>
</template>

<script>
import ComicsComp from "./ComicsComp.vue";
import jsonData from "../assets/dc-comics.json";

export default {
  name: "MainVue",
  components: {
    ComicsComp,
  },
  data() {
    return {
      items: jsonData,
    };
  },
  components: {
    ComicsComp,
  },
};
</script>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/general" as *;

.jumbotron {
  background-image: url(../assets/img/jumbotron.jpg);
  background-size: cover;
  height: 40vh;
}

.container {
  position: relative;

  .banner {
    color: white;
    background-color: $accent-color;
    font-weight: 500;
    display: inline-block;
    padding: 0.5rem 1.5rem;
    position: absolute;
    top: -20px;
  }
}

div.comicsList {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  padding: 1.5rem 0;

  a {
    margin-bottom: 1.5rem;
    display: inline-block;
    background-color: $accent-color;
    color: white;
    text-decoration: none;
    font-weight: 700;
    text-transform: uppercase;
    padding: 0.8rem 2rem;
  }
}
</style>
