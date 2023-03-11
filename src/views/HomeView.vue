<script setup></script>

<template>
  <main>
    <section>
      <h1 class="intro">
        Hello! My name's <span class="underline">Steph</span>,<br />and I'm a
        <span class="underline">Software Developer</span>.
      </h1>
    </section>
    <section class="image"><img src="/assets/yung-steph.png" alt="" /></section>
  </main>
</template>

<style scoped lang="scss">
@keyframes opac {
  0% {
    opacity: 0;
  }

  100% {
    opacity: 1;
  }
}

main {
  animation: opac 2s;
  width: 1100px;
  margin: 0 auto;
  display: flex;
  align-items: center;
  gap: 50px;

  .intro {
    font-size: 50px;
    text-align: right;
  }

  img {
    border-radius: 50%;
  }

  .underline {
    &::after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 0;

      width: 100%;
      height: 0.1em;
      animation: underline 1.5s forwards;
      animation-delay: 1s;
    }
  }

  @keyframes underline {
    0% {
      opacity: 0;
      background-color: #4bc0d9;

      transform: translate3d(-30%, 0, 0);
    }

    40% {
      opacity: 0;
      background-color: #4bc0d9;
    }

    100% {
      opacity: 1;
      background-color: #4bc0d9;
      transform: translate3d(0, 0, 0);
    }
  }

  h1 {
    font-size: 30px;

    &::selection {
      background-color: #4bc0d9;
    }
  }
}
</style>
