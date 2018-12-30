<template>
  <b-row align-h="end" class="page-selector">
    <b-col cols="12" md="6" lg="4">
    <div class="text-center">
      <div class="h1 mb-5">Number of Pages</div>
      <p class="mr-4 left-indicator" @click="decrease">-</p>
      <b-form-input type="number" v-model="number" min="1"></b-form-input>
      <p class="ml-4 right-indicator" @click="increase">+</p>
      <div class="mt-3 mr-4">
        1 Homepage + {{ this.number - 1 }} inner pages
      </div>
    </div>
    </b-col>


    <b-col cols="12" md="6" lg="4" class="ml-7">
     <b-card no-body
          style="max-width: 15rem;"
          img-top>
        <h4 slot="header">{{ this.imgcolor }} {{ this.titles }}</h4>
        <b-card-body>
            <p class="card-text">
              Hello There
            </p>
        </b-card-body>
        <b-list-group flush>
            <b-list-group-item>{{ this.number }} Page{{ this.number > 1 ? 's' : ''}} = {{ amount }}</b-list-group-item>
            <b-list-group-item>Dapibus ac facilisis in</b-list-group-item>
            <b-list-group-item>Vestibulum at eros</b-list-group-item>
        </b-list-group>
        <b-card-footer>Total: </b-card-footer>
      </b-card>
    </b-col>
  </b-row>
</template>

<script>
  export default {
    props: ['imgcolor', 'titles'],
    data() {
      return {
        number: 1
      }
    },
    methods: {
      increase() {
        this.number++;
      },
      decrease() {
        this.number--;
      }
    }
  }
</script>

<style scoped>
  .page-selector {
    margin-top: 60px;
  }

  input {
    all: unset;
    width: 50px;
    height: 30px;
    border: 2px solid #62697F;
    padding: 20px;
    text-align: center;
    border-radius: 5px;
  }

  .left-indicator,
  .right-indicator {
    font-size: 30px;
    cursor: pointer;
    display: inline-block;
  }

  .card {
    border: none;
  }
</style>
