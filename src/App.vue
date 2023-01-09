<script>
import DcHeader from "./components/DcHeader.vue";

export default {
  components: {
    DcHeader,
  },
};
</script>

<template>
  <header>
    <DcHeader />
  </header>

  <main></main>
  <footer></footer>
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
@use "./styles/partials/variables" as *;
</style>
