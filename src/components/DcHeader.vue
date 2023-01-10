<template>
  <div class="container">
    <div class="nav-wrapper">
      <img src="../assets/img/dc-logo.png" alt="DC Logo" />
      <ul>
        <li v-for:="item in menuItems">
          <a href="#">
            {{ item.text }}
          </a>
        </li>
      </ul>
    </div>
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

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/general.scss" as *;

div.nav-wrapper {
  display: flex;
  justify-content: space-between;
  align-content: center;
  padding: 1rem;

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
      position: relative;

      a {
        text-decoration: none;
        color: black;

        &:hover {
          color: $accent-color;
        }
      }

      &:hover::before {
        content: "";
        position: absolute;
        left: 25%;
        bottom: 0;
        top: 42px;
        width: 50%;
        border-bottom: 5px solid $accent-color;
      }
    }
  }
}
</style>
