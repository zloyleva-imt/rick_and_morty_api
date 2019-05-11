<template>
  <header>
    <nav class="Header__Nav">
      <ul class="Header__List">
        <li>
          <a href="#" class="Header__Link active">Home</a>
        </li>
        <li>
          <a href="#" class="Header__Link">About</a>
        </li>
        <li>
          <a href="#" class="Header__Link">Contacts</a>
        </li>
      </ul>
    </nav>
  </header>
</template>
<script>
export default {};
</script>
<style lang="scss">
header {
  height: 5rem;
  nav.Header__Nav {
    display: flex;
    -webkit-box-pack: justify;
    justify-content: space-between;
    -webkit-box-align: center;
    align-items: center;
    max-width: 1200px;
    min-height: 80px;
    margin: 0px auto;
    padding: 0px 20px;
    ul.Header__List {
      display: flex;
      padding: 0px;
      margin: 0px;
      list-style-position: outside;
      list-style-image: none;
      li {
        margin: 0 1rem 0;
        padding-left: 0;
        list-style-type: none;
        a.Header__Link {
          color: rgb(51, 51, 51);
          transition: all 0.2s ease 0s;
          border-width: initial;
          border-style: none;
          border-color: initial;
          border-image: initial;
          text-decoration: none;
          &.active {
            color: rgb(255, 152, 0);
          }
          &:last-child {
            margin-bottom: 0;
          }
        }
      }
    }
  }
}
</style>
