<template>
  <reviewList :reviews="reviews"></reviewList>
  <reviewFrom @review-submitted="addReview"></reviewFrom>
  
</template>

<script>

import reviewFrom from "./components/reviewFrom.vue"
import reviewList from "./components/reviewList.vue"
export default {
  name: 'App',
  components: {
    reviewFrom,
    reviewList
  },
  data() {
    return {
      reviews : []
    }
  },
  methods: {
    addReview(review) {
      this.reviews.push(review)
    }
  }
}
</script>


<style>
    .review-form {
  display: flex;
  flex-direction: column;
  width: 425px;
  padding: 20px;
  margin: 40px;
  border: 2px solid #d8d8d8;
  background-color: white;
  -webkit-box-shadow: 0px 2px 15px -12px rgba(0, 0, 0, 0.57);
  -moz-box-shadow: 0px 2px 15px -12px rgba(0, 0, 0, 0.57);
  box-shadow: 2px 15px -12px rgba(0, 0, 0, 0.57);
}
.review-form .button {
  display: block;
  margin: 30px auto;
}
textarea {
  width: 95%;
  height: 70px;
  padding: 10px;
  font-size: 20px;
  margin-bottom: 20px;
}
.review-container {
  width: 425px;
  padding: 20px;
  background-color: white;
  -webkit-box-shadow: 0px 2px 20px -12px rgba(0, 0, 0, 0.57);
  -moz-box-shadow: 0px 2px 20px -12px rgba(0, 0, 0, 0.57);
  box-shadow: 2px 20px -12px rgba(0, 0, 0, 0.57);
  margin-left: 40px;
  border: 2px solid #d8d8d8;
} 



</style>