<template>
  <div class="error-bg">
    <div class="container">
      <Error />
      <div class="row text-center">
        <div class="col-md-12 col-sm-12 col-lg-12 pt-4">
          <h1 class="error-headline ml-5">404</h1>
        </div>
        <div class="col-md-12 col-sm-12 col-lg-12">
          <h3 class="error-text">oops.... who designed <br>this page....?</h3>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import Error from '~/components/Error-btn'
  export default {
    components: {
      Error
    },
  }
</script>

<style scoped>
  .error-bg {
    height: 100vh;
    width: 100vw;
    background-color: rgba(32, 113, 106, 0.719);
    background-image: url(~assets/img/error.png);
    background-repeat: no-repeat;
    background-size: 100%;
    background-position: center;
    color: #fff;
  }

  .error-headline {
    font-size: 80px;
    font-family: futura-pt-bold, sans-serif;
    font-weight: 700;
    font-style: normal;
  }

  .error-text {
    font-size: 35px;
    font-family: futura-pt, sans-serif;
    font-weight: 500;
    font-style: normal;
  }
</style>
