<script>
export default {
  name: "ComicsComp",
  props: {
    imgPath: String,
    price: String,
    series: String,
  },
  data() {
    return {
      active: false,
    };
  },
};
</script>

<template>
  <div class="card" @mouseover="active = true" @mouseleave="active = false">
    <img :src="imgPath" alt="" />
    <span v-show="active">{{ price }}</span>
    <p>{{ series }}</p>
  </div>
</template>

<style lang="scss">
@use "../styles/partials/variables" as *;
@use "../styles/general" as *;

div.card {
  color: #fff;
  width: 196px;
  padding: 1rem 0.5rem;
  position: relative;

  span {
    position: absolute;
    background-color: rgb(251, 202, 6);
    color: red;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-size: 1.2rem;
    padding: 0.5rem;
  }

  img {
    width: 100%;
    height: 196px;
    object-fit: cover;
    object-position: top;
  }
  p {
    text-align: left;
  }
}
</style>
