<template>
  <div id="app">
    <Navigation></Navigation>
	<Teaser></Teaser>
	<CharactersList></CharactersList>
  </div>
</template>

<script>
import Navigation from './components/Navigation.vue';
import Teaser from './components/Teaser.vue';
import CharactersList from './components/CharactersList.vue';
import style from './asserts/style.css';
export default {
  name: 'app',
  components: {
    Navigation, Teaser, CharactersList
  }
}
</script>

<style>

</style>
