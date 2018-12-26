<template>
  <div>
    <b-row>
      <b-col cols="12">
        <b-card
          tag="article"
          style="max-width: 10rem;"
          class="mb-2 p-2"
          @click="updateOrder">
          <p :class="['card-text', 'text-center', card]">
           <span :class="['img', 'caret', 'pb-4']">
             <img src="~assets/svg/success.svg">
           </span>
            <span :class="[img, image]"></span>
            {{ name }}
          </p>
        </b-card>
      </b-col>
    </b-row>
  </div>
</template>

<script>
  export default {
    props: ['name', 'img', 'image', 'caret', 'card', 'activeOrder'],
    data() {
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

.card:focus {
  border-color: rgb(54, 157, 95);
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

/* .card-text {
  font-size: 20px;
  font-weight: 700;
} */
</style>
