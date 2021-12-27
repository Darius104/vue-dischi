<template>
  <div id="app">
    <Header />
    <ListSongs />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import ListSongs from "./components/ListSongs.vue";

export default {
  name: "App",
  components: {
    Header,
    ListSongs
  },
};
</script>

<style lang="scss">
// reset
@import './style/general.scss';

</style>