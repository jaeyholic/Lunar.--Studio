<template>
  <b-row>
    <b-col cols="2">
      <b-card
        tag="article"
        style="max-width: 10rem;"
        :class="['mb-2', 'p-2', bgColor]"
        @click="updateOrder">
        <p :class="['card-text', 'text-center', card]">
          <span :class="['img', 'caret']" v-if="this.activeOrder === this.name">
            <img src="~assets/svg/success.svg">
          </span>
          <span :class="[img, image, 'mt-5']"></span>
          {{ name }}
        </p>
      </b-card>
    </b-col>
  </b-row>
</template>

<script>
  export default {
    props: ['name', 'img', 'image', 'caret', 'card', 'bgColor', 'activeOrder'],
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
  background-size: 50px;
  height: 50px;
  margin-bottom: 15px;
  background-position: center;
}


/***********************
  Card Border Colors
***********************/
.card .bgColor-1 {
  border-color: #FC490B;
}

.card .bgColor-2 {
  border-color: #2170A6;
}

.card .bgColor-3 {
  border-color: #01579B;
}

.card .bgColor-4 {
  border-color: #FFC107;
}

.card .bgColor-5{
  border-color: #7CB342;
}

.card .bgColor-6 {
  border-color: #FF4081;
}

.card:hover .img-1,
.card:hover .img-2,
.card:hover .img-3,
.card:hover .img-4,
.card:hover .img-5,
.card:hover .img-6 {
  background-repeat: no-repeat;
  background-size: 50px;
  height: 50px;
  margin-bottom: 15px;
}

.caret img {
  height: 20px;
}

.img-1 {
  background-image: url('~assets/svg/cards/html-dark.svg');
}

.card:hover .img-1 {
  background-image: url('~assets/svg/cards/html-color.svg');
}

.img-2 {
  background-image: url('~assets/svg/cards/php-dark.svg');
}

.card:hover .img-2 {
  background-image: url('~assets/svg/cards/php-color.svg');
}

.img-3 {
  background-image: url('~assets/svg/cards/wordpress-dark.svg');
}

.card:hover .img-3 {
  background-image: url('~assets/svg/cards/wordpress-color.svg');
}

.img-4 {
  background-image: url('~assets/svg/cards/web-dark.svg');
}

.card:hover .img-4 {
  background-image: url('~assets/svg/cards/web-color.svg');
}

.img-5 {
  background-image: url('~assets/svg/cards/android-dark.svg');
}

.card:hover .img-5 {
  background-image: url('~assets/svg/cards/android-color.svg');
}

.img-6 {
  background-image: url('~assets/svg/cards/design-dark.svg');
}

.card:hover .img-6 {
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
