<template>
  <section
    v-if="isLoading || randomPokemon?.id === null"
    class="flex flex-col justify-center items-center w-screen h-screen"
  >
    <h1 className="text-3xl font-bold">Espere por favor</h1>
    <h3 className="animate-pulse">Estamos cargando los pokemons...</h3>
  </section>

  <section v-else class="flex flex-col justify-center items-center w-screen h-screen">
    <h1 class="m-5">Quien es este pokemon?</h1>
    <div class="h-20">
      <button
        class="bg-blue-500 text-white shadow-md rounded-lg p-2 cursor-pointer transition-all hover:bg-blue-800"
        v-if="gameStatus !== GameStatus.Playing"
        @click="getNextRound(4)"
      >
        Jugar de nuevo?
      </button>
    </div>

    <!-- Pokemon picture -->
    <PokemonPicture
      v-if="randomPokemon"
      :pokemon-id="randomPokemon.id"
      :show-pokemon="gameStatus !== GameStatus.Playing"
    />

    <!-- Pokemon options -->
    <PokemonOptions
      :options="options"
      :block-selection="gameStatus !== GameStatus.Playing"
      :correct-answer="randomPokemon?.id ?? 0"
      @selectedOptions="checkAnswer"
    />
  </section>
</template>

<script setup lang="ts">
import PokemonPicture from '../components/PokemonPicture.vue'
import PokemonOptions from '../components/PokemonOptions.vue'
import { usePokemonGame } from '../composables/usePokemonGame.ts'
import { GameStatus } from '../interfaces'

const {
  isLoading,
  randomPokemon,
  gameStatus,
  pokemonOptions: options,
  checkAnswer,
  getNextRound,
} = usePokemonGame()
</script>
