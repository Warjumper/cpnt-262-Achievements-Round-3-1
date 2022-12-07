<script setup lang="ts">
const { data: pokemons } = useFetch(() => `api/pokemon`);
</script>

<template>
  <div class="grid grid-cols-5 gap-8 mx-auto container">
    <div
      v-for="pokemon of pokemons"
      :key="pokemon.name"
      class="p-4 border-1 rounded border-gray-200"
    >
      <!-- <img 
      :src="pokemon.sprite" 
      alt="pokemon"
      class="w-full h-64 object-cover" 
      /> -->
      <div class="mt-2">
        <h2 class="text-xl font-bold">
        {{ pokemon.name.english }}
        </h2>
        <p class="text-gray-600">
          ID = {{ pokemon.id }}
        </p>
      </div>
    </div>
  </div>
</template>
