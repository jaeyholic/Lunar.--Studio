<template>
  <div class="work">
    <b-container>
      <b-row>
        <b-col cols="12" sm="12" md="12" lg="4" v-for="work in works" :key="work.title">
          <div class="h3" v-html="work.title"></div>
          <p class="pb-4">{{ work.content }}</p>
        </b-col>

        <b-col>

        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
  export default {
    name: "Work",
    data() {
      return {
        works: [
          {title: "UI/UX & Graphic <br>Designs", content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua."},
          {title: "Website/Web App <br>Developments", content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua."},
          {title: "Android & iOS <br>Developments", content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua."}
        ]
      }
    }
  }
</script>

<style scoped>
  .work {
    margin-top: 100px;
    padding: 50px 45px 0;
  }
</style>
