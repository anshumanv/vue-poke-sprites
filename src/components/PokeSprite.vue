<template>
  <img :src="getGifUrl()" :alt="getName()" :class="this.spriteClass" />
</template>

<script>
import pokemonGif from "pokemon-gif";
import pokemonNumberToName from "pokemon-gif/lib/pokedex-number-to-name";

export default {
  name: "PokeSprite",
  props: ["pokemon", "spriteClass"],
  created() {
    console.log(this.getGifUrl(this.pokemon));
  },
  methods: {
    getGifUrl() {
      let { pokemon } = this;
      pokemon = isNaN(pokemon) ? pokemon : parseInt(pokemon);
      const name =
        typeof pokemon === "string" ? pokemon : pokemonNumberToName[pokemon];
      let url = "";
      console.log(pokemon, name);
      try {
        url = pokemonGif(name);
        console.log(pokemon, name);
      } catch (e) {
        console.log(e);
        url = "";
      }
      console.log(url);
      return url;
    },
    getName() {
      const { pokemon } = this;
      return typeof pokemon === "string"
        ? pokemon
        : pokemonNumberToName[pokemon];
    }
  }
};
</script>

<style scoped></style>
