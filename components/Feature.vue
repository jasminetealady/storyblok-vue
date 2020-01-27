<template>
  <div v-editable="blok" class="column feature">
    {{ blok.name }}
    <p>{{blok.text}}</p>
  </div>
</template>

<script>
export default {
  props: ['blok']
}
</script>

<style lang="scss">

.feature{
  padding: 6rem 0;
  font-size: 1.5rem;
  text-align: center;
  border: solid 1px #7C86C0;
  border-radius: 5px;
  margin: 10px 5px;
  flex: 1;
  color: #fff;

  p {
    margin-top: 2rem;
    font-size: 1rem;
    padding: 0 2rem;
    line-height: 2;
    font-family: "Avenir";
  }
}
</style>
