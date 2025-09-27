<script setup>
const pokemon = defineProps(["name", "xp", "height", "img", "loading"]);
</script>

<template>
  <div
    class="card cardPokemonSelected"
    :class="loading ? '' : 'animate__animated animate__flipInY'"
  >
    <img 
    v-if="pokemon.name"
      :src="pokemon.img" 
      class="card-img-top pt-3" 
      :alt="pokemon.name" 
    />

    <img 
    v-else
      src="../assets/egg_pokemon.svg" 
      height="250" 
      class="card-img-top pt-3" 
      alt="???" 
    />
    <div class="card-body">
      <h5 class="card-titler text-center">{{ pokemon.name  || '???'}}</h5>
      <hr />
      <div class="row text-center">
        <section class="col">
          <strong>XP:</strong>
          <span>{{ pokemon.xp }}</span>
        </section>

        <section class="col">
          <strong>Height:</strong>
          <span>{{ pokemon.height }}</span>
        </section>
      </div>
    </div>
  </div>
</template>

<style scoped>
.cardPokemonSelected {
  height: 75vh;
  background: RGB(243, 17, 142);
  background: radial-gradient(
    circle,
    rgba(243, 17, 142, 0.49)39%,
    rgba(13, 110, 253, 1) 100%
  );
}

.cardPokemonSelected img{
  height: 250px;
}

@media screen and (max-width: 768px) {
  .cardPokemonSelected {
    height: 30vh;
    width: 40%;
    margin: 0 auto 10px auto;
  }

  .cardPokemonSelected img{
    height: 100px;
  }
}
</style>
