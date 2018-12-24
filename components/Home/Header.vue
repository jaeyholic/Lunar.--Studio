<template>
  <b-container>
    <b-row class="d-flex">
      <b-col cols="12" md="12" sm="12" xs="12" lg="6" order="2" order-sm="2" order-md="2" order-lg="1">
        <div class="heading-left">
          <h1 class="h1">We use the latest technology to help people grow in whatever they are best at.</h1>
          <p class="lead">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
          <nuxt-link to="/start-project" class="btn-link">
            <Button
            button="Start a project"/>
          </nuxt-link>
        </div>
      </b-col>

      <b-col cols="12" md="12" sm="12" xs="12" lg="6" order="1" order-sm="1" order-md="1" order-lg="2">
        <div class="heading-right">
          <img src="~assets/svg/home-right.svg" alt="">
        </div>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import Button from '~/components/Button'
  export default {
    name: 'Header',
    components: {
    Button
    }
  }
</script>

<style scoped>
.heading-left,
.heading-right {
  padding-top: 150px;
}

.lead {
  padding-top: 20px;
  padding-bottom: 20px;
}

/***************************
      Media Queries
***************************/
@media only screen and (min-width: 400px) {
  .heading-left {
    padding-top: 50px;
  }

  .heading-right {
    padding-top: 80px;
  }
}

@media only screen and (min-width: 576px) {
  .heading-left {
    padding-top: 50px;
  }

  .heading-right {
    padding-top: 80px;
  }
}

@media (min-width: 768px) {
  .heading-left {
    padding-top: 50px;
  }

  .heading-right {
    padding-top: 80px;
  }
}

@media (min-width: 992px) {
  .heading-left {
    padding-top: 150px;
  }

  .heading-right {
    padding-top: 150px;
  }
}
</style>
