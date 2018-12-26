<template>
  <div class="about-page">
    <About />
    <Feels />
    <Help />
    <Work />
  </div>
</template>

<script>
import About from '~/components/About/About'
import Feels from '~/components/About/Feels'
import Help from '~/components/About/Help'
import Work from '~/components/About/Work'

  export default {
    components: {
      About,
      Feels,
      Help,
      Work
    }
  }
</script>

<style scoped>
.about-page {
  padding-top: 150px;
}
</style>
