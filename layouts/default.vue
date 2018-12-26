<template>
  <div>
    <Navigation />
    <nuxt/>
    <Footer />
  </div>
</template>

<script>
import Navigation from '~/components/Navigation'
import Footer from '~/components/Footer'

export default {
  components: {
    Navigation,
    Footer
  }
}
</script>


<style>
html {
  font-family: 'Poppins', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

body {
  background-color: #F4F4F4;
  color: #62697F;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

a,
a:not(last-child) {
  font-size: 18px;
  color: #62697F;
  text-decoration: none;
  padding-right: 40px;
}

a:hover {
  text-decoration: none;
  color: #393939;
}

a.nuxt-link-active {
  color: #393939;
}

a.nuxt-link-active::after {
  content: '';
  border-bottom: 2px solid #393939;
  top: 80px;
  left: 80px;
}

.h1 {
  font-size: 35px;
  font-family: futura-pt-bold, sans-serif;
  font-weight: 700;
  font-style: normal;
}

.h3 {
  font-size: 22px;
  font-family: futura-pt, sans-serif;
  font-weight: 500;
  font-style: normal;
}

.text-shadow {
  text-shadow: 5px 9px 0 rgba(0,0,0,.15);
  font-size: 45px;
  font-family: futura-pt-bold, sans-serif;
  font-weight: 700;
  font-style: normal;
}
</style>
