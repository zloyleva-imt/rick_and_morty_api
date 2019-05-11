<template>
  <article class="CharacterCard__Wrapper">
    <div class="CharacterCard__ImgWrapper">
      <div class="card-image">
        <img :src="character.image" alt="Beta-Seven">
      </div>
      <div class="CharacterCard__Title">
        <h2 class="CharacterCard__Name">{{ character.name }}</h2>
        <p class="CharacterCard__Description">id: {{ character.id }} - created 2 years ago</p>
      </div>
    </div>
    <div class="CharacterCard__InfoWrapper">
      <div class="CharacterCard__TextWrapper">
        <span>STATUS</span>
        <p>{{ character.status }}</p>
      </div>
      <div class="CharacterCard__TextWrapper">
        <span>SPECIES</span>
        <p>
          {{ character.species }}
          <span v-if="character.type">, {{ character.type }}</span>
        </p>
      </div>
      <div class="CharacterCard__TextWrapper">
        <span>GENDER</span>
        <p>{{ character.gender }}</p>
      </div>
      <div class="CharacterCard__TextWrapper">
        <span>ORIGIN</span>
        <p>{{ character.origin.name }}</p>
      </div>
      <div class="CharacterCard__TextWrapper">
        <span>LAST LOCATION</span>
        <p>{{ character.location.name }}</p>
      </div>
    </div>
  </article>
</template>

<script>
export default {
  props: {
    character: {
      type: Object,
      required: true
    }
  }
};
</script>

<style lang="scss">
article.CharacterCard__Wrapper {
  max-width: 300px;
  margin-bottom: 0.625rem;
  box-shadow: rgba(0, 0, 0, 0.16) 0px 2px 2px 0px,
    rgba(0, 0, 0, 0.08) 0px 0px 0px 1px;
  border-radius: 0.625rem;
  overflow: hidden;
  div.CharacterCard__ImgWrapper {
    position: relative;
    max-width: 300px;
    max-height: 300px;
    div.card-image {
      width: 300px;
      height: 300px;
      background: rgb(32, 35, 41);
      img {
        margin: 0px;
        overflow: hidden;
        height: 100%;
        width: auto;
        display: block;
        max-width: 100%;
        padding-bottom: 0;
        padding-left: 0;
        padding-right: 0;
        padding-top: 0;
      }
    }
    div.CharacterCard__Title {
      width: 100%;
      opacity: 0.8;
      position: absolute;
      bottom: 0px;
      background: rgb(32, 35, 41);
      padding: 0.625rem;
      h2.CharacterCard__Name {
        color: rgb(245, 245, 245);
        font-size: 1.625rem;
        font-weight: 400;
        font-stretch: expanded;
        margin: 0px;
        padding-bottom: calc(0.40625rem - 1px);
        padding-left: 0;
        padding-right: 0;
        padding-top: 0;
      }
      p.CharacterCard__Description {
        color: rgb(187, 187, 187);
        font-size: 0.875rem;
        margin: 0px;
        padding-bottom: 0;
        padding-left: 0;
        padding-right: 0;
        padding-top: 0;
      }
    }
  }
  div.CharacterCard__InfoWrapper {
    height: 100%;
    color: rgb(255, 152, 0);
    padding: 1.25rem;
    background: rgb(51, 51, 51);
    div.CharacterCard__TextWrapper {
      display: flex;
      -webkit-box-pack: justify;
      justify-content: space-between;
      -webkit-box-align: center;
      align-items: center;
      flex-wrap: nowrap;
      padding: 0.75rem 0px 0.375rem;
      border-bottom: 1px solid rgb(68, 68, 68);
      span {
        font-size: 0.7rem;
        font-weight: 400;
        color: rgb(158, 158, 158);
      }
      p,
      p span {
        width: 100%;
        font-size: 0.9rem;
        font-weight: 200;
        text-align: right;
        padding: 0px;
        margin: 0px;
        color: rgb(255, 152, 0);
      }
    }
  }
}
</style>
