<template>
  <div class="hero-card-container">
    <div v-for="hero in heroes" :key="hero.id" class="hero-card">
      <img :src="hero.image" class="hero-card-img" alt="Hero Image" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      heroes: [],
    }
  },
  created() {
    fetch('/data/heroes.json')
      .then((response) => response.json())
      .then((data) => {
        this.heroes = data
      })
      .catch((error) => {
        console.error('Error loading heroes:', error)
      })
  },
}
</script>

<style scoped>
.hero-card-container {
  display: flex;
  justify-content: center;
  gap: 4rem;
  padding: 4rem 0;
}

.hero-card {
  width: calc(
    45% - 1rem
  ); /* Ajusta a largura dos cartões para ocupar 3 por linha com espaçamento */
  max-width: 100%;
}

.hero-card-img {
  width: 100%;
  height: 99%;
  object-fit: cover;
}
</style>
