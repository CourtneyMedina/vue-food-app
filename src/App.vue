<template>
  <div class="container">
    <NavBar/>
    <Card v-for="food in foods"  
            :key="food._id"
            :price="food.price" 
            :product="food.product"
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
    setup() {
      // console.log(foods.default)     // If objects are being imported as modules, check for properties
    return {
      foods: foods.default,
    };
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
  background-color: red;
}

.container {
  margin: 3rem;
  display: grid;
  grid-template-columns: auto auto auto;
  column-gap: 1rem;
  row-gap: 0.1rem;
}


</style>
