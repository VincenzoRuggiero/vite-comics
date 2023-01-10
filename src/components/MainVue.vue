<template>
  <div class="comicsList">
    <ComicsComp
      v-for="item in items"
      :imgPath="item.thumb"
      :price="item.price"
      :series="item.series" />
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

div.comicsList {
  background-color: $black-bg;
}
</style>
