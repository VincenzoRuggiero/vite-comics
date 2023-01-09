<template>
  <div class="nav-wrapper">
    <img src="../assets/img/dc-logo.png" alt="DC Logo" />
    <ul>
      <li v-for:="item in menuItems">
        {{ item.text }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      menuItems: [
        {
          text: "characters",
        },
        {
          text: "comics",
        },
        {
          text: "movies",
        },
        {
          text: "tv",
        },
        {
          text: "games",
        },
        {
          text: "collectibles",
        },
        {
          text: "videos",
        },
        {
          text: "fans",
        },
        {
          text: "news",
        },
        {
          text: "shop",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@use "../styles/partials/variables" as *;

div.nav-wrapper {
  display: flex;
  justify-content: space-between;
  align-content: center;
  padding: 2rem 0.4rem;

  img {
    width: 3rem;
  }

  ul {
    list-style-type: none;
    display: flex;
    align-self: center;

    li {
      padding: 0 0.7rem;
      text-transform: uppercase;
      font-size: 0.7rem;
      font-weight: 500;

      &:hover {
        color: $accent-color;
      }
    }
  }
}
</style>
