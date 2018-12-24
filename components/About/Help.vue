<template>
  <div class="help">
    <b-container>
      <b-row>
        <b-col cols="12" md="12" sm="12" xs="12" lg="6" order="2" order-sm="2" order-md="2" order-lg="1" align-self="center">
          <div class="help-left">
            <h1 class="h1">Bringing people and design<br> together is our kind of thing</h1>
            <p class="h3">Lets design together and bring your ideas to life through meaningful digital products.</p>
          </div>
        </b-col>

        <b-col cols="12" md="12" sm="12" xs="12" lg="6" order="1" order-sm="1" order-md="1" order-lg="2">
          <div class="help-right">
            <img src="~assets/svg/about.svg" alt="">
          </div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
  export default {

  }
</script>

<style scoped>
  .help {
    margin-top: 100px;
    background-color: #fff;
    padding: 100px 0;
  }


/***************************
      Media Queries
***************************/
@media only screen and (min-width: 400px) {
  .help-left {
    padding-top: 50px;
  }

  .h1 {
    font-size: 30px;
  }
}
</style>
