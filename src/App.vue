<template>
  <div class="container">
    <NavBar></NavBar>
    <Card v-for="food in foods" 
            :key="food.product" 
            :price="food.price" 
            :productname="food.product"
            :manufacturer="food.manufacturer" 
            :rating="food.rating"></Card>

  </div>
</template>

<script>
import NavBar from "./components/NavBar.vue";
import Card from "./components/Card.vue";
import * as foods from "./assets/foods.json";

export default {
  components: {
    NavBar,
    Card,
  },
    setup: {
    foods,
    }
}

// let cart = [];


</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.container {
  margin: 3rem;
  display: grid;
  grid-template-columns: auto;
  column-gap: 1rem;
  row-gap: 0.1rem;
  background-color: red;
}
</style>
