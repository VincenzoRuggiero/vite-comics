<script>
import DcHeader from "./components/DcHeader.vue";
import MainVue from "./components/MainVue.vue";
import MainFooter from "./components/MainFooter.vue";

export default {
  components: {
    DcHeader,
    MainVue,
    MainFooter,
  },
};
</script>

<template>
  <header>
    <DcHeader />
  </header>

  <main>
    <MainVue />
  </main>
  <footer>
    <MainFooter />
  </footer>
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
@use "./styles/partials/variables" as *;

main {
  background-color: $black-bg;
}

footer {
  background-color: $sub-footer-bg;
}
</style>
