<template>
  <div class="selectors">
    <b-container>
      <b-row>
        <b-col cols="12">
          <div class="h1 pb-2 text-center">Start Your Order</div>
          <p class="lead text-center pb-5">No upfront payment is required at this stage. We will get back to you in the fastest possible way.</p>
          <Cards v-for="item in titles" :key="item.title"
          :name="item.title"
          :img="item.img"
          :image="item.image"
          :caret="item.caret"
          :card="item.cardName"
          :active-order="activeOrder"
          @updateOrder="onUpdateOrder"/>
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
        titles: [
          {title: 'HTML', img: 'img', image: 'img-1', caret: 'caret', cardName: 'card-p1'},
          {title: 'PHP', img: 'img', image: 'img-2', caret: 'caret', cardName: 'card-p2'},
          {title: 'WORDPRESS', img: 'img', image: 'img-3', caret: 'caret', cardName: 'card-p3'},
          {title: 'WEB APP', img: 'img', image: 'img-4', caret: 'caret', cardName: 'card-p4'},
          {title: 'MOBILE APP', img: 'img', image: 'img-5', caret: 'caret', cardName: 'card-p5'},
          {title: 'DESIGNS', img: 'img', image: 'img-6', caret: 'caret', cardName: 'card-p6'}
          ],
        activeOrder: ''
      }
    },
    methods: {
      onUpdateOrder(order) {
        this.activeOrder = order;
      }
    }
  }
</script>

<style scoped>
.selectors {
  padding-bottom: 100px;
}
</style>
