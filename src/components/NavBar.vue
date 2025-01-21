<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const header = ref(null);

const rolagem = () => {
  if (window.scrollY > 0) {
    header.value.classList.add('rolagem');
  } else {
    header.value.classList.remove('rolagem');
  }
};

onMounted(() => {
  window.addEventListener('scroll', rolagem);
});

onUnmounted(() => {
  window.removeEventListener('scroll', rolagem);
});
</script>

<template>
  <nav ref="header" class="navbar navbar-expand-lg fixed-top navbar-light">
    <div class="container">
      <span class="blur"></span>
      <div class="logo d-flex justify-content-center align-content-center mx-4 pt-1">
        <h1><a href="#home" class="text-decoration-none">A</a></h1>
      </div>

      <button class="navbar-toggler" type="button" data-bs-toggle="offcanvas" data-bs-target="#offcanvasNavbar"
        aria-controls="offcanvasNavbar" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="offcanvas offcanvas-end" tabindex="-1" id="offcanvasNavbar" aria-labelledby="offcanvasNavbarLabel">
        <div class="offcanvas-header">
          <button type="button" class="btn-close text-reset text-light" data-bs-dismiss="offcanvas"
            aria-label="Close"></button>
        </div>
        <div class="offcanvas-body">
          <ul class="navbar-nav justify-content-end flex-grow-1 pe-3">
            <li class="nav-item overflow-hidden">
              <a class="nav-link" href="#home">Home</a>
            </li>
            <li class="nav-item overflow-hidden">
              <a class="nav-link" href="#sobre">Sobre</a>
            </li>
            <li class="nav-item overflow-hidden">
              <a class="nav-link" href="#habilidades">Habilidades</a>
            </li>
            <li class="nav-item overflow-hidden">
              <a class="nav-link" href="#projetos">Projetos</a>
            </li>
            <li class="nav-item overflow-hidden">
              <a class="nav-link" href="#contato">Contato</a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </nav>
</template>

<style scoped>
nav {
  background-color: var(--cor-2);
}

.navbar.rolagem {
  background-color: var(--cor-2);
  box-shadow: 0px 0px 5px 10px rgba(0, 0, 0, 0.2);
}

.navbar-toggler {
  border-color: var(--cor-10);
}

.navbar-toggler:focus {
  color: transparent;
}

.navbar-toggler-icon {
  filter: brightness(0) invert(1);
}

.offcanvas.show {
  width: 300px;
}

.logo h1 {
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--cor-10);
  border-radius: 50%;
  font-size: 2.4rem;
  height: 3.6rem;
  width: 3.6rem;
  border: 6px solid var(--cor-10);
}

.logo h1 a {
  color: var(--cor-10);
}

ul a::after {
  content: "";
  display: block;
  width: 0;
  height: 2px;
  background: linear-gradient(90deg, #400851, #9c27a9);
  transition: all .5s ease;
}

ul a:hover::after {
  width: 100%;
}

.nav-link {
  text-decoration: none;
  font-size: 1.1rem;
  color: var(--cor-10);
  font-weight: 600;
}

ul a:hover {
  color: var(--cor-9);
}

.navbar-brand .brand-logo {
  height: 40px;
  width: auto;
}

.offcanvas-title {
  font-size: 1.25rem;
  font-weight: bold;
}

.offcanvas-body,
.offcanvas-header {
  background-color: var(--cor-2);
}

.offcanvas-header .btn-close {
  background-color: var(--cor-10);
}
</style>