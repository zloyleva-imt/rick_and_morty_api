<template>
  <section class="Home__HeroWrapper">
    <h1 class="Home__Title">The Rick and Morty API</h1>
    <div class="Home__SubTitleWrapper">
      <h2 class="Home__SubTitle">Hey, did you ever want to hold a Terry fold?</h2>
      <h2
        class="Home__HiddenSubTitle"
      >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;I got one right here, grab my terry flap&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</h2>
    </div>
  </section>
</template>
<script>
export default {};
</script>
<style lang="scss">
section.Home__HeroWrapper {
  display: flex;
  -webkit-box-pack: center;
  justify-content: center;
  -webkit-box-align: center;
  align-items: center;
  flex-direction: column;
  height: 40vh;
  text-align: center;
  h1.Home__Title {
    text-transform: uppercase;
    line-height: 0.75em;
    color: rgb(32, 35, 41);
    font-size: 3.75rem;
    margin: 0px;
    border-width: initial;
    border-style: none;
    border-color: initial;
	border-image: initial;
	&::selection {
        color: rgb(255, 152, 0);
        background: rgb(32, 35, 41);
      }
    @media (max-width: 48em) {
      & {
        line-height: 1;
        padding: 0px 0.75rem;
      }
    }
  }
  div.Home__SubTitleWrapper {
    transform: skew(-2deg) translateY(-6px);
    padding: 0.3125rem 0.25rem 0px;
    background: rgb(32, 35, 41);
    @media (max-width: 48em) {
      & {
        background: rgb(255, 255, 255);
      }
    }
    h2.Home__SubTitle {
      text-transform: uppercase;
      line-height: 1em;
      padding-bottom: 0.15em;
      font-size: 1.875rem;
      color: rgb(255, 152, 0);
      transform: skew(2deg);
      margin: 0px;
      border-width: initial;
      border-style: none;
      border-color: initial;
      border-image: initial;
      -moz-user-select: none;
      -webkit-user-select: none;
      -ms-user-select: none;
      user-select: none;
      -o-user-select: none;
      @media (max-width: 48em) {
        & {
          line-height: 1;
          padding: 0px 0.75rem;
        }
      }
    }
    h2.Home__HiddenSubTitle {
      text-transform: uppercase;
      line-height: 1em;
      padding-bottom: 0.15em;
      font-size: 1.875rem;
      transform: skew(2deg);
      position: absolute;
      width: 100%;
      top: 4px;
      left: 0px;
      color: transparent;
      margin: 0px;
      border-width: initial;
      border-style: none;
      border-color: initial;
      border-image: initial;
      padding: 0px 0.25rem;
      &::selection {
        color: rgb(32, 35, 41);
        background: rgb(255, 152, 0);
      }
      @media (max-width: 48em) {
        line-height: 1;
        padding: 0px 0.75rem;
      }
    }
  }
}
</style>
