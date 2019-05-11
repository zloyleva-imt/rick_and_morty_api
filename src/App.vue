<template>
  <div id="app">
    <Navigation></Navigation>
    <Teaser></Teaser>
    <CharactersList :charasterArray="charasterArray"></CharactersList>
  </div>
</template>

<script>
import Navigation from "./components/Navigation.vue";
import Teaser from "./components/Teaser.vue";
import CharactersList from "./components/CharactersList.vue";
import "./asserts/style.css";
export default {
  name: "app",
  components: {
    Navigation,
    Teaser,
    CharactersList
  },
  data() {
    return {
      charasterArray: [],
      info: {},
      getCharastersUrl: "https://rickandmortyapi.com/api/character/"
    };
  },
  mounted() {
    console.log("mounted");
    this.axios.get(this.getCharastersUrl).then(res => {
      this.charasterArray = res.data.results;
    });
  }
};
</script>

<style>
</style>
