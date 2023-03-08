<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <div class="wrapper">
      <nav>
        <RouterLink to="/">HOME</RouterLink>
        <RouterLink to="/projects">PROJECTS</RouterLink>
        <RouterLink to="/contactme">CONTACT ME</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style scoped lang="scss">
.wrapper {
  display: grid;

  nav {
    justify-self: flex-end;
    a.router-link-exact-active {
      color: var(--color-text);
    }

    a.router-link-exact-active:hover {
      background-color: transparent;
    }

    a {
      padding: 0 1rem;
      font-weight: 500;
    }
  }
}

@media (min-width: 1024px) {
}
</style>
