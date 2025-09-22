<script setup>
const pokemon = defineProps(["name", "urlBaseSvg"]);
</script>

<template>
  <div class="col-4">
    <div class="card p-2 mb-3 cardListPokemon">
      <p class="text-center">{{ pokemon.name }}</p>
      <img height="80" :src="urlBaseSvg" class="card-img-top" alt="imagem do pokemon" />
    </div>
  </div>
</template>

<style scoped>
.cardListPokemon {
  background: RGB(243, 17, 142);
  background: radial-gradient(
    circle,
    rgba(243, 17, 142, 0.49) 39%,
    rgba(13, 110, 253, 1) 100%
  );
  cursor: pointer;
}

.cardListPokemon:hover {
  background: #3f5efb;
  background: radial-gradient(circle, rgb(248, 0, 124), #3502c0);
}

.cardListPokemon img:hover {
  padding: 0.2rem;
}
</style>
