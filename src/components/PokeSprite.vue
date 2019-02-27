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
      const { pokemon } = this;
      const name =
        typeof pokemon === "string" ? pokemon : pokemonNumberToName[pokemon];
      let url = "";
      try {
        url = pokemonGif(name);
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
