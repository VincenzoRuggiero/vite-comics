<script>
import DcHeader from "./components/DcHeader.vue";
import MainVue from "./components/MainVue.vue";

export default {
  components: {
    DcHeader,
    MainVue,
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
  <footer></footer>
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
@use "./styles/partials/variables" as *;
</style>
