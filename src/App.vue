<template>
  <div class="container">
    <NavBar/>
    <Card v-for="food in foods"  
            v-bind:key="food._id"
            v-bind:price="food.price" 
            v-bind:product="food.product"
            v-bind:manufacturer="food.manufacturer" 
            v-bind:rating="food.rating"/>

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
    return {
      foods,
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
