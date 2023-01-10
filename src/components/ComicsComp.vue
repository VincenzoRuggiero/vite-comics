<script>
export default {
  name: "ComicsComp",
  props: {
    imgPath: String,
    price: String,
    series: String,
  },
};
</script>

<template>
  <div class="card">
    {{ imgPath }} -- {{ price }} -- {{ series }}
    <!-- <img :src="imgPath" alt="" />
    <p>{{}}</p>
    <p>{{}}</p> -->
  </div>
</template>

<style lang="scss">
@use "../styles/partials/variables" as *;

div.card {
  color: #fff;
}
</style>
