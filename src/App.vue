<template>
  <div id="app">
    <PokeSprite :pokemon="this.pokemon" spriteClass="new-pokemon"></PokeSprite>
    <input v-model="pokemon" class="poke-input" />
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
      pokemon: "charizard"
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
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  flex-direction: column;
}
</style>
