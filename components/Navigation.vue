<template>
  <b-navbar toggleable="lg">

    <b-navbar-brand>
      <nuxt-link to="/" exact>
        <img src="~assets/img/logo.png" alt="">
      </nuxt-link>
    </b-navbar-brand>

    <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>

    <b-collapse is-nav id="nav_collapse" class="text-center">

      <b-navbar-nav>
        <b-nav-item >
          <nuxt-link to="/about">About</nuxt-link>
        </b-nav-item>

        <b-nav-item >
          <nuxt-link to="/studio">Studio</nuxt-link>
        </b-nav-item>

        <b-nav-item >
          <nuxt-link to="/contact">Contact</nuxt-link>
        </b-nav-item>

        <b-nav-item >
          <nuxt-link to="/start-project">
            <Button
            button="Start a project" />
          </nuxt-link>
        </b-nav-item>
      </b-navbar-nav>

    </b-collapse>
  </b-navbar>
</template>

<script>
  import Button from './Button'
  export default {
    name: 'Navigation',
    components: {
      Button
    }
  }
</script>

<style scoped>
.navbar-brand img {
  height: 50px;
  margin-right: 110px;
}
</style>
