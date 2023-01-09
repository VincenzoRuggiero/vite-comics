<template>
  <div class="footer-menu-wrapper">
    <div class="footer-nav">
      <ul>
        <h3>DC COMICS</h3>
        <li v-for:="items in comicsItems">
          {{ items.text }}
        </li>

        <h3>SHOP</h3>
        <li v-for:="items in shopItems">
          {{ items.text }}
        </li>
      </ul>
      <ul>
        <h3>DC</h3>
        <li v-for:="items in dcItems">
          {{ items.text }}
        </li>
      </ul>
      <ul>
        <h3>SITES</h3>
        <li v-for:="items in sitesItems">
          {{ items.text }}
        </li>
      </ul>
    </div>

    <div class="big-logo">
      <!-- <img src="../assets/img/dc-logo-bg.png" alt="DC Logo" /> -->
    </div>
  </div>

  <div class="sub-footer"></div>
</template>

<script>
export default {
  data() {
    return {
      comicsItems: [
        {
          text: "Characters",
        },
        {
          text: "Comics",
        },
        {
          text: "Movies",
        },
        {
          text: "TV",
        },
        {
          text: "Games",
        },
        {
          text: "Videos",
        },
        {
          text: "News",
        },
      ],
      shopItems: [
        {
          text: "Shop DC",
        },
        {
          text: "Shop DC Collectibles",
        },
      ],
      dcItems: [
        {
          text: "Terms Of Use",
        },
        {
          text: "Privacy policy (New)",
        },
        {
          text: "Ad Choices",
        },
        {
          text: "Advertising",
        },
        {
          text: "Jobs",
        },
        {
          text: "Subscriptions",
        },
        {
          text: "Talent Workshops",
        },
        {
          text: "CPSC Certificates",
        },
        {
          text: "Ratings",
        },
        {
          text: "Shop Help",
        },
        {
          text: "Contact Us",
        },
      ],
      sitesItems: [
        {
          text: "DC",
        },
        {
          text: "MAD Magazine",
        },
        {
          text: "DC Kids",
        },
        {
          text: "DC Universe",
        },
        {
          text: "DC Power Visa",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@use "../styles/partials/variables" as *;

div.footer-menu-wrapper {
  background-image: url(../assets/img/footer-bg.jpg);
  z-index: 1;
  padding: 0 1rem;
  display: flex;
  justify-content: space-between;

  .footer-nav {
    display: flex;

    h3 {
      color: white;
      margin: 1rem 0 0.6rem;
    }

    ul {
      list-style-type: none;
      margin-bottom: 20px;
      margin-right: 30px;
    }

    li {
      color: gray;
      line-height: 1.2rem;
      font-size: 0.8rem;
    }
  }

  .big-logo {
    width: 50%;
    background-position: center;
    background-image: url(../assets/img/dc-logo-bg.png);
    background-size: 400px;
    background-repeat: no-repeat;
  }
}

div.sub-footer {
  height: 10vh;
  background-color: darkorange;
}
</style>
