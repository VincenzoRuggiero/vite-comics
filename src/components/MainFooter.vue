<template>
  <div class="top-footer-bg">
    <div class="container">
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

        <div class="big-logo"></div>
      </div>
    </div>
  </div>

  <div class="bottom-footer-bg">
    <div class="container">
      <div class="sub-footer">
        <div class="button-div">
          <a href="#">SIGN-UP NOW!</a>
        </div>
        <div class="social">
          <p>Follow Us</p>
          <img src="../assets/img/footer-facebook.png" alt="Facebook logo" />
          <img src="../assets/img/footer-twitter.png" alt="Twitter logo" />
          <img src="../assets/img/footer-youtube.png" alt="YouTube logo" />
          <img src="../assets/img/footer-pinterest.png" alt="Pinterest logo" />
          <img src="../assets/img/footer-periscope.png" alt="Periscope logo" />
        </div>
      </div>
    </div>
  </div>
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

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/general" as *;

.top-footer-bg {
  background-image: url(../assets/img/footer-bg.jpg);

  div.footer-menu-wrapper {
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
}

.bottom-footer-bg {
  background-color: #303030;
  div.sub-footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.5rem 1rem;

    div.button-div a {
      padding: 0.7rem;
      background-color: transparent;
      color: white;
      text-decoration: none;
      border: 2px solid $accent-color;
      display: flex;
    }

    .social {
      display: flex;
      justify-content: space-around;
      align-items: center;
      flex-wrap: nowrap;

      p {
        color: $accent-color;
        text-transform: uppercase;
        font-size: 1.2rem;
        font-weight: 600;
        margin-right: 1rem;
      }

      img {
        width: 8%;
        padding: 0 0.6rem;
      }
    }
  }
}
</style>
