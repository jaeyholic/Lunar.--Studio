<template>
  <div class="container">
    <div class="py-5">
      <nuxt-link to="/">
      <div class="btn btn-success text-center">Back to home</div>
    </nuxt-link>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Error-Btn'
  }
</script>

<style scoped>
  .btn {
    text-align: center;
    border: none;
  }

  .btn-success {
    all: unset;
    padding: 20px 70px;
    color: #fff;
    background-color: #20716A;
  }

  .btn-success:hover,
  .btn-success:active {
    background-color: #35495e;
  }
</style>
