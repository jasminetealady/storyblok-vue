<template>
  <div v-editable="blok" class="hero">
    <div class="wrapper">
      <div class="call-to-action">
        <p>{{blok.call_to_action_text}}</p>
        <a :href="blok.call_to_action_button">Call To Action</a>
      </div>
      <img :src="blok.call_to_action_image" />
    </div>
  </div>
</template>

<script>
export default {
  props: ['blok'],
  mounted(){
    console.log(this.blok)
  },
  methods: {
    doThis(){
      alert('Meow!')
    }
  }
}
</script>

<style lang="scss">
$purple: #7c86c0;

.hero {
  display: flex;
  justify-content: center;
  padding: 2rem;
  width: 100%;
  padding-bottom: 8rem;
  // border: solid 1px black;

  .wrapper {
    display: flex;
    justify-content: space-between;
    // border: solid 1px black;
    max-width: 800px;
  }

  .call-to-action {
    display: flex;
    flex-direction: column;
    width: 40%;

    p {
      line-height: 1.5rem;
    }
  }

  img {
    height: 300px;
  }

  a {
    padding: 1rem 2rem;
    text-decoration-line: none;
    background: #7c86c0;
    color: #fff;
    border-radius: 5px;
    margin-top: 2rem;
    width: auto;
  }
}
</style>
