<template>
  <div id="app">
    <Header @selectChange="setGenre" />
    <ListSongs :filterGenre="selectGenre" />
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
  data: function(){
    return{
      selectGenre: "NaN"
    }
  },
  methods: {
    setGenre: function(genre){
      this.selectGenre = genre
    }
  }
};
</script>

<style lang="scss">
// reset
@import './style/general.scss';

</style>