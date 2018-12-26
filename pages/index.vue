<template>
  <section class="container">
    <Home />
  </section>
</template>

<script>
import Home from './Home'

export default {
  components: {
    Home
  }
}
</script>

<style>
  .page-enter-active,
  .page-leave-active {
    transition: all 0.5s;
  }

  .page-enter,
  .page-leave-active {
    opacity: 0;
    transform: scale(0);
  }
</style>
