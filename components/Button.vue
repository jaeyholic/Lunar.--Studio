<template>
  <div class="btn btn-success text-center">{{ button }}</div>
</template>

<script>
  export default {
    name: 'Button',
    props: ['button']
  }
</script>

<style scoped>

  .btn-success {
    all: unset;
    padding: 20px 70px;
    color: #fff;
    background-image: linear-gradient(to right, #23A393, #369D5F);
  }

  .btn-success:hover,
  .btn-success:active {
    background-color: #35495e;
  }
</style>
