<template>
  <nav v-editable="blok" class="nav">
    <img :src="blok.logo" />
    <ul>
      <li :key="link._uid" v-for="link in blok.links">
        <nuxt-link :to="link.link.cached_url">{{link.link.cached_url}}</nuxt-link>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  props: ['blok'],
  mounted(){
    console.log(this.blok)
  }
}
</script>

<style lang="scss">
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 2rem 2rem;
  border-bottom: rgba(255, 255, 255, 0.1);
  font-family: "Libre Baskerville";

  img {
    height: 6rem;
    width: 6rem;
    border-radius: 50%;
  }

  ul {
    display: flex;
    list-style: none;

    li {
      margin-right: 1rem;

      a {
        text-decoration-line: none;
        color: #7C86C0;
        // font-weight: bold;
      }

      :hover {
        border-bottom: solid 1px #7C86C0;
      }
    }
  }
}
</style>
