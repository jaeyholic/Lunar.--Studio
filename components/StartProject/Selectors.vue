<template>
  <div class="selectors">
    <b-container>
      <b-row>
        <b-col cols="12">
          <div class="h1 pb-2 text-center">Start Your Order</div>
          <p class="lead text-center pb-5">No upfront payment is required at this stage. We will get back to you in the fastest possible way.</p>
          <Cards />
        </b-col>
      </b-row>
    </b-container>
    <input type="radio" id="one" value="One" v-model="picked">
    <label for="one">One</label>
    <br>
    <input type="radio" id="two" value="Two" v-model="picked">
    <label for="two">Two</label>
    <br>
    <span>Picked: {{ picked }}</span>
      </div>
    </template>

<script>
import Cards from './Cards'
  export default {
    components: {
      Cards
    },
    data() {
      return {
        picked: '',
      }
    },
  }
</script>

<style scoped>
.selectors {
  padding-bottom: 100px;
}
</style>
