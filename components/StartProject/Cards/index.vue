<template>
  <div>
    <b-row>
      <b-col cols="2" v-for="item in titles" :key="item.title">
        <b-card
          tag="article"
          style="max-width: 10rem;"
          class="mb-2 p-2"
          v-model="activeOrder"
          @click="updateOrder">
          <p :class="['card-text', 'text-center', 'cardName']">
           <span :class="['img', 'caret', 'pb-4']">
             <img src="~assets/svg/success.svg">
           </span>
            <span class="{'img', 'image'}"></span>
            {{ item.title }}
          </p>
        </b-card>
      </b-col>

      <!-- <b-col cols="2">
        <b-card
          tag="article"
          style="max-width: 10rem;"
          class="mb-2 p-2"
          v-model="activeOrder"
          @click="updateOrder">
          <p class="card-text text-center card-p2">
           <span class="img caret pb-4">
             <img src="~assets/svg/success.svg">
           </span>
            <span class="img img-2"></span>
            {{ titles.php }}
          </p>
        </b-card>
      </b-col>

      <b-col cols="2">
        <b-card
          tag="article"
          style="max-width: 10rem;"
          class="mb-2 p-2">
          <p class="card-text text-center card-p3">
            <span class="img caret pb-4">
             <img src="~assets/svg/success.svg">
           </span>
            <span class="img img-3"></span>
            {{ titles.word }}
          </p>
        </b-card>
      </b-col>

      <b-col cols="2">
        <b-card
          tag="article"
          style="max-width: 10rem;"
          class="mb-2 p-2">
          <p class="card-text text-center card-p4">
            <span class="img caret pb-4">
             <img src="~assets/svg/success.svg">
           </span>
            <span class="img img-4"></span>
            {{ titles.web }}
          </p>
        </b-card>
      </b-col>

      <b-col cols="2">
        <b-card
          tag="article"
          style="max-width: 10rem;"
          class="mb-2 p-2">
          <p class="card-text text-center card-p5">
            <span class="img caret pb-4">
             <img src="~assets/svg/success.svg">
           </span>
            <span class="img img-5"></span>
            {{ titles.app }}
          </p>
        </b-card>
      </b-col>

      <b-col cols="2">
        <b-card
          tag="article"
          style="max-width: 10rem;"
          class="mb-2 p-2">
          <p class="card-text text-center card-p6">
            <span class="img caret pb-4">
             <img src="~assets/svg/success.svg">
           </span>
            <span class="img img-6"></span>
            {{ titles.design }}
          </p>
        </b-card>

        <b-card
          tag="article"
          style="max-width: 10rem;"
          class="mb-2 p-2">
          <p class="card-text text-center">
           {{ activeOrder }}
          </p>
        </b-card> -->
      </b-col>
    </b-row>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        titles: [
          {title: 'HTML',img: 'img', image: 'img-1', caret: 'caret', cardName: 'card-p1'},
          {title: 'PHP',img: 'img', image: 'img-2', caret: 'caret', cardName: 'card-p2'},
          {title: 'WORDPRESS',img: 'img', image: 'img-3', caret: 'caret', cardName: 'card-p3'},
          {title: 'WEB APP',img: 'img', image: 'img-4', caret: 'caret', cardName: 'card-p4'},
          {title: 'MOBILE APP',img: 'img', image: 'img-5', caret: 'caret', cardName: 'card-p5'},
          {title: 'DESIGNS',img: 'img', image: 'img-6', caret: 'caret', cardName: 'card-p6'}
          ],
        activeOrder: ''
      }
    },
    methods: {
      updateOrder() {
        this.activeOrder = this.titles
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
