<p align="center">
  <img src="http://www.pokestadium.com/sprites/xy/charizard.gif" align="center" width="150">
</p>

<h1 align="center"> vue-poke-sprites </h1>
<p align="center">
<img src="https://img.shields.io/npm/v/vue-poke-sprites.svg?style=for-the-badge" align="center">

<img src="https://img.shields.io/npm/dt/vue-poke-sprites.svg?style=for-the-badge" align="center">

<img src="https://img.shields.io/github/license/anshumanv/vue-poke-sprites.svg?style=for-the-badge" align="center">

</p>

<p align="center">A vue component that renders animated pokemon sprites.</p>

## Demo

Visit - [Link](https://vue-poke-sprites.netlify.com)


### Usage

1. Install the package

```sh
$ yarn add --save vue-poke-sprites
```

2. Import the component

```js
import PokeSprite from "./components/PokeSprite.vue";
.
.
export default {
  .
  .
  components: {
    PokeSprite
  }
  .
  .
}
```

3. Use it

```js
  <PokeSprite pokemon="lugia" spriteClass="pokemon-lugia"></PokeSprite>
```


### Props

* **pokemon** - Pass the name or the ID of the pokemon.

* **spriteClass** - Pass in a class name to modify as you see fit.


## Related

* A corresponding React component is [here](https://github.com/anshumanv/react-poke-sprites)


## Author

[Anshuman Verma](https://github.com/anshumanv)

[<img src="https://image.flaticon.com/icons/svg/185/185961.svg" width="35" padding="10">](https://twitter.com/Anshumaniac12)
[<img src="https://image.flaticon.com/icons/svg/185/185964.svg" width="35" padding="10">](https://linkedin.com/in/anshumanv12)
[<img src="https://image.flaticon.com/icons/svg/185/185981.svg" width="35" padding="10">](https://www.facebook.com/anshumanv12)


## Contribute

Found a bug? please [create an issue](https://github.com/anshumanv/vue-poke-sprites/issues/new)