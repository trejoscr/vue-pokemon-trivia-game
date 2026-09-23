<template>
  <section>
    <img v-if="!showPokemon" :src="pokemonImageUrl" alt="Pokemon" class="brightness-0 h-50" />
    <img v-else :src="pokemonImageUrl" alt="Pokemon" class="fade-in h-50" />
  </section>
</template>

<script setup lang="ts">
import { computed } from 'vue'

interface Props {
  pokemonId: number
  showPokemon?: boolean
}

const props = withDefaults(defineProps<Props>(), {
  showPokemon: false,
})

const pokemonImageUrl = computed(() => {
  return `https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/other/dream-world/${props.pokemonId}.svg`
})
</script>

<style scoped>
img {
  user-select: none;
  -moz-user-select: none;
  -webkit-user-select: none;
  -ms-user-select: none;
  -webkit-user-drag: none;
}
</style>
