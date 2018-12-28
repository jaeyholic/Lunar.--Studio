<template>
  <b-card
    tag="article"
    style="max-width: 12rem;"
    class="mb-3"
    :class="bgcolor"
    @click="updateOrder">
    <p :class="['card-text', 'text-center']">
      <span :class="[img, 'caret', 'm-0', 'p-0']"
      v-if="this.activeOrder === this.name">
        <img src="~assets/svg/success.svg">
      </span>
      <span :class="[img, image, 'mt-3']"></span>
      {{ name }}
    </p>
  </b-card>
</template>

<script>
  export default {
    props: ['name', 'img', 'image', 'caret', 'card', 'bgcolor', 'imgchanger', 'activeOrder'],
    data(){
      return {

      }
    },
    methods: {
      updateOrder() {
        this.$emit('updateOrder', this.name)
      }
    }
  }
</script>

<style scoped>
.card:hover {
  cursor: pointer;
  border-color:rgba(54, 157, 95, 0.384);
}

/***********************
    Img and Hover
***********************/
.img {
  display: block;
}

.img-1,
.img-2,
.img-3,
.img-4,
.img-5,
.img-6 {
  background-repeat: no-repeat;
  background-size: 40px;
  height: 40px;
  margin-bottom: 10px;
  background-position: center;
}


/***********************
  Card Border Colors
***********************/
.bgcolor-1 {
  border-color: #FC490B;
}

.bgcolor-2 {
  border-color: #2170A6;
}

.bgcolor-3 {
  border-color: #01579B;
}

.bgcolor-4 {
  border-color: #FFC107;
}
.bgcolor-5{
  border-color: #7CB342;
}

.bgcolor-6 {
  border-color: #FF4081;
}

.card:hover .img-1,
.card:hover .img-2,
.card:hover .img-3,
.card:hover .img-4,
.card:hover .img-5,
.card:hover .img-6 {
  background-repeat: no-repeat;
  background-size: 40px;
  height: 40px;
  margin-bottom: 10px;
}

.caret img {
  height: 20px;
}

.img-1 {
  background-image: url('~assets/svg/cards/html-dark.svg');
}

.img-1 {
  background-image: url('~assets/svg/cards/html-color.svg');
}

.img-2 {
  background-image: url('~assets/svg/cards/php-dark.svg');
}

.img-2-2 {
  background-image: url('~assets/svg/cards/php-color.svg');
}

.img-3 {
  background-image: url('~assets/svg/cards/wordpress-dark.svg');
}

.img-3-3 {
  background-image: url('~assets/svg/cards/wordpress-color.svg');
}

.img-4 {
  background-image: url('~assets/svg/cards/web-dark.svg');
}

.img-4-4 {
  background-image: url('~assets/svg/cards/web-color.svg');
}

.img-5 {
  background-image: url('~assets/svg/cards/android-dark.svg');
}

.img-5-5 {
  background-image: url('~assets/svg/cards/android-color.svg');
}

.img-6 {
  background-image: url('~assets/svg/cards/design-dark.svg');
}

.img-6-6 {
  background-image: url('~assets/svg/cards/design-color.svg');
}


/***********************
  Card Hover Color
***********************/
.card:hover .card-p1 {
  color: #FC490B;
}

.card:hover .card-p2 {
  color: #2170A6;
}

.card:hover .card-p3 {
  color: #01579B;
}

.card:hover .card-p4 {
  color: #FFC107;
}

.card:hover .card-p5 {
  color: #7CB342;
}

.card:hover .card-p6 {
  color: #FF4081;
}


</style>
