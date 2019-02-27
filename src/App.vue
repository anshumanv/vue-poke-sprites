<template>
  <div id="app">
    <PokeSprite :pokemon="this.pokemon"></PokeSprite>
    <input v-model="pokemon" />
  </div>
</template>

<script>
import PokeSprite from "./components/PokeSprite.vue";

export default {
  name: "app",
  components: {
    PokeSprite
  },
  data() {
    return {
      pokemon: 10
    };
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
