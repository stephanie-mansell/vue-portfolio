<script setup></script>

<template>
  <div class="logo">
    S
    <span></span>
    M
  </div>
</template>

<style scoped lang="scss">
.logo {
  animation: up 2s;
  font-size: 35px;
  display: flex;
  align-items: center;
  flex: 1;
  font-weight: 700;

  span {
    margin: 0 15px;
    width: 8px;
    height: 8px;
    background: #15f4ee;
    transform: rotate(45deg);
    animation-timing-function: ease-in;
    animation: rotation 1.5s;
    animation-delay: 4s;
  }

  @keyframes up {
    0% {
      opacity: 0;
      transform: translateY(80px);
    }

    50% {
      opacity: 0;
    }

    100% {
      opacity: 1;
      transform: none;
    }
  }

  @keyframes rotation {
    0% {
      transform: rotate(45deg);
    }
    30% {
      transform: rotate(0deg);
    }
    100% {
      transform: rotate(315deg);
    }
  }
}
</style>
