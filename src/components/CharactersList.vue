<template>
  <section class="Home__ShowcaseWrapper">
    <div class="Home__ShowcaseInner">
      <CharacterItem v-for="character in charasterArray" :key="character.id" :character="character"></CharacterItem>
    </div>
  </section>
</template>
<script>
import CharacterItem from "./CharacterItem";
export default {
  components: {
    CharacterItem
  },
  props: {
    charasterArray: {
      type: Array,
      required: true
    }
  }
};
</script>
<style lang="scss">
section.Home__ShowcaseWrapper {
  display: flex;
  -webkit-box-pack: center;
  justify-content: center;
  -webkit-box-align: center;
  align-items: center;
  min-height: calc(60vh - 5rem);
  padding: 1.875rem;
  background: rgb(32, 35, 41);
  .Home__ShowcaseInner {
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    max-width: 1260px;
    min-height: 40vh;
  }
}
</style>
