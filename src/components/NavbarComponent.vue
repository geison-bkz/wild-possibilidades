<template>
  <nav class="navbar navbar-expand-lg custom-nav fixed-top">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">Minha Marca</a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link custom-nav-link" href="#about-us">Sobre Nós</a>
          </li>
          <li class="nav-item">
            <a class="nav-link custom-nav-link" href="#services">Serviços</a>
          </li>
          <li class="nav-item">
            <a class="nav-link custom-nav-link" href="#our-team">Nosso Time</a>
          </li>
          <li class="nav-item">
            <a class="nav-link custom-nav-link" href="#portfolio">Portfólio</a>
          </li>
          <li class="nav-item">
            <a class="nav-link custom-nav-link" href="#contacts">Contatos</a>
          </li>
          <li class="nav-item">
            <a class="nav-link custom-nav-link call-to-action" href="#call-to-action"
              >Solicitar Orçamento</a
            >
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<style scoped>
.custom-nav {
  background-color: var(--vt-c-white-soft);
  padding: 1rem;
}

.custom-nav-link {
  color: var(--navbar-link-color);
  padding: 0.5rem 1.5rem; /* Aumenta o espaçamento entre os links */
  transition:
    background-color 0.3s,
    color 0.3s;
}

.custom-nav-link:hover {
  color: var(--vt-c-primary-pink);
}

.call-to-action {
  color: var(--vt-c-primary-pink);
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
    background-color: var(--vt-c-primary-pink);
    transform-origin: bottom right;
    transition: transform 0.3s ease-out;
  }

  &:hover::after {
    transform: scaleX(1);
    transform-origin: bottom left;
  }
}
</style>
