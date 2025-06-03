<script setup lang="ts">
import HeroCardComponent from './cards/HeroCardComponent.vue'
</script>

<template>
  <section class="hero">
    <div class="hero-container">
      <div class="hero-banner">
        <h1>Wild Possibilidades: Transformando Ideias em Impacto</h1>
        <p>
          Exploramos o selvagem potencial do marketing e das redes sociais para criar conexões
          reais, autênticas e estratégicas. Aqui, sua marca deixa de ser apenas uma ideia para se
          tornar uma força que inspira e transforma.
        </p>
        <strong>Vamos tirar suas ideias do papel e colocá-las no topo. </strong>
        <a href="#call-to-action">Vamos começar!</a>
      </div>
    </div>
    <div class="hero-cards">
      <HeroCardComponent />
    </div>
  </section>
</template>

<style scoped>
.hero {
  background-color: var(--vt-c-white-mute);
  height: auto;
  width: 100%;
}

.hero-container {
  align-items: center;
  display: flex;
  justify-content: center;
}

.hero-banner {
  background-color: var(--vt-c-black-soft);
  width: 100%;
  height: 80vh;
  align-items: center;
  color: var(--vt-c-white-soft);
  display: flex;
  flex-direction: column;
  justify-content: center;

  h1 {
    font-size: 2.5rem;
    font-weight: 700;
    margin-bottom: 1rem;
    text-align: center;
  }

  p {
    font-size: 1.25rem;
    margin-bottom: 1rem;
    text-align: center;
    width: 50%;
  }

  strong {
    font-size: 1.5rem;
    margin-bottom: 1rem;
    text-align: center;
  }

  a {
    color: var(--vt-c-primary-yellow);
    font-size: 1.5rem;
    position: relative;
    text-decoration: none;
    transition: color 0.3s;

    &::after {
      content: '';
      position: absolute;
      width: 100%;
      transform: scaleX(0);
      height: 2px;
      bottom: 0;
      left: 0;
      background-color: var(--vt-c-primary-yellow);
      transform-origin: bottom right;
      transition: transform 0.3s ease-out;
    }

    &:hover::after {
      transform: scaleX(1);
      transform-origin: bottom left;
    }
  }

  .hero-cards {
    display: flex;
    justify-content: center;
  }
}
</style>
