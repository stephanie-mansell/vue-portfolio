<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Logo from './components/Logo.vue'
</script>

<template>
  <header>
    <div class="wrapper">
      <RouterLink to="/" class="logo-link">
        <Logo />
      </RouterLink>
      <nav>
        <RouterLink to="/">HOME</RouterLink>
        <RouterLink to="/aboutme">ABOUT ME</RouterLink>
        <RouterLink to="/projects">PROJECTS</RouterLink>
        <RouterLink to="/contactme">CONTACT ME</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style scoped lang="scss">
.wrapper {
  display: flex;
  align-items: center;

  .logo-link {
    text-decoration: none;
    color: white;
    flex: 1;
  }

  nav {
    justify-self: flex-end;

    a {
      font-size: 18px;
      margin-left: 2rem;
      padding: 0 5px;
      color: #4bc0d9;

      text-transform: lowercase;
      letter-spacing: 0.08rem;
    }
  }
}

@media (min-width: 1024px) {
}
</style>
