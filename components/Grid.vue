<template>
  <div v-editable="blok" class="grid">
    <component :key="blok._uid" v-for="blok in blok.columns" :blok="blok" :is="blok.component | dashify"></component>
  </div>
</template>

<script>
export default {
  props: ['blok']
}
</script>

<style lang="scss">
.grid {
  display: flex;
  padding: 2rem;
  background: #7c86c0;
}
</style>
